# BUG-007 : Dégradation performance BDD (mauvais choix d'architecture)

## Type
- [ ] Fonctionnelle
- [ ] Technique
- [x] **Bug** - 🟠 Haute (Performance + Dette technique)

## Description
**Problème détecté** : L'application devient **très lente** (temps de réponse > 10 secondes) dès qu'il y a plus de 1000 produits en base. L'investigation révèle que :
1. Les requêtes n'ont **pas d'index** sur les colonnes souvent filtrées (catégorie, prix)
2. Le schéma de BDD est **dénormalisé** de manière inefficace
3. Certaines requêtes font des **N+1 queries** (charger 100 produits = 101 requêtes SQL)

**Cause racine** : Choix d'architecture précipité au Sprint 1 sans penser à la scalabilité.

**Impact** : 🟠 Haute - Expérience utilisateur dégradée, risque de perte de clients, impossible de passer à l'échelle.

## Complexité estimée
**Story Points** : 13 pts (refactoring majeur de BDD + migrations + tests)

## Critères d'acceptation (Fix du bug)

### ☑️ Critère 1 : Audit de performance de la BDD
- **Catégorie** : `[PERF]`
- **Valeur du dé** : 🎲 **2**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Analyse complète avec outils de profiling (EXPLAIN ANALYZE, pg_stat_statements, slow query log). Identifier toutes les requêtes lentes (> 500ms).

---

### ☑️ Critère 2 : Ajout des index manquants
- **Catégorie** : `[PERF]`
- **Valeur du dé** : 🎲 **4**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Création d'index sur : `products.category_id`, `products.price`, `orders.user_id`, `orders.created_at`. Vérification que les requêtes utilisent bien les index.

---

### ☑️ Critère 3 : Correction des requêtes N+1
- **Catégorie** : `[ARCHI]`
- **Valeur du dé** : 🎲 **5**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non (✅ Oui si bonus `[ARCHI]` actif)

**Description** : Refactoring du code pour utiliser des **JOIN** ou **eager loading** au lieu de N+1 queries. Exemple : charger produits + artisans en 1 requête au lieu de 1+N.

---

### ☑️ Critère 4 : Optimisation du schéma (migrations)
- **Catégorie** : `[ARCHI]`
- **Valeur du dé** : 🎲 **6**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non (✅ Oui si bonus `[ARCHI]` actif)

**Description** : Migrations pour normaliser/dénormaliser intelligemment. Exemple : ajouter une colonne `orders.total_amount` calculée pour éviter de re-calculer à chaque fois.

---

### ☑️ Critère 5 : Mise en place de cache (Redis)
- **Catégorie** : `[PERF]`
- **Valeur du dé** : 🎲 **3**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Implémentation d'une couche de cache (Redis, Memcached) pour les données fréquemment lues : liste des produits, détails produit, profils artisans.

---

### ☑️ Critère 6 : Tests de charge (load testing)
- **Catégorie** : `[TESTS]`
- **Valeur du dé** : 🎲 **1**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non (✅ Oui si bonus `[TESTS]` actif)

**Description** : Tests de charge avec 10 000 produits, 1000 utilisateurs simultanés (k6, JMeter, Artillery). Vérifier que temps de réponse < 500ms pour 95% des requêtes.

---

### ☑️ Critère 7 : Monitoring de performance en prod
- **Catégorie** : `[DEVOPS]`
- **Valeur du dé** : 🎲 **4**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Monitoring des temps de réponse BDD en production (APM : New Relic, Datadog). Alertes si temps de requête > 1s ou augmentation soudaine.

---

## Notes

### Dépendances
- Apparaît pendant : Sprint 4 ou 5 (quand le catalogue grossit)
- Bloque : Scalabilité de l'application, acquisition de nouveaux artisans

### Priorité
🟠 **Haute** - Pas bloquant immédiatement mais **critique pour la croissance**

⚠️ **Dilemme** :
- Option A : Fix rapide (index seulement) → 3-5 pts, amélioration partielle
- Option B : Refactoring complet (tous les critères) → 13 pts, solution pérenne

### Impact sur la vélocité
💥 **Ce bug est coûteux** : 13 points = presque tout un sprint. Mais ne pas le fixer condamne le projet à long terme.

### Bonus débloqué
_Aucun (c'est un bug)_

### Historique des tentatives

| Sprint | Dés lancés | Critères validés | Statut |
|--------|------------|------------------|--------|
|  | - | - | ⏳ Pas encore jouée |
|   |   |   |  - |
|   |   |   |  - |
|   |   |   |  - |
|   |   |   |  - |
|   |   |   |  - |

---

## Définition of Done (DoD)
- [ ] Tous les critères d'acceptation sont validés (7/7)
- [ ] Temps de réponse < 500ms validé par tests de charge
- [ ] Déployé en production avec monitoring actif
- [ ] Documentation de l'architecture BDD mise à jour

---

## Note pédagogique

💡 **Dette technique vs vélocité court terme** :

Ce bug illustre un dilemme classique en Agile :

**Sprint 1** : L'équipe a choisi d'aller vite pour livrer des features
→ Pas d'index, architecture simple, pas de cache
→ ✅ Vélocité élevée à court terme

**Sprint 4-5** : Le produit grossit, les performances s'effondrent
→ 🔴 Dette technique qui coûte 13 points à rembourser

**Questions pour l'équipe** :
1. Aurait-il fallu investir dans une US `[PERF]` ou `[ARCHI]` dès le Sprint 1-2 ?
2. Est-il acceptable de sacrifier la qualité pour la vitesse au début ?
3. Comment gérer ce bug s'il arrive pendant le Sprint 5 alors qu'il faut livrer le MVP ?

**Propositions de négociation** :
- **MVP du fix** : Seulement critères 1, 2, 6 (index + tests) = ~5 pts
- **Fix complet** : Tous les critères = 13 pts, mais solution pérenne

**Référence réelle** : Stack Overflow en 2008 avec SQL Server → Migration vers architecture optimisée. Twitter "fail whale" (2008-2011) → Refactoring massif de la BDD et architecture. 🐋
