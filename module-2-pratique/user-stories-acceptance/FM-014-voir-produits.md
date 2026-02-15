# US-FM-014 : Voir tous les produits disponibles (Template EPIC 3)

## Type
- [x] Fonctionnelle
- [ ] Technique

## Description
En tant que **client**,
Je veux **voir tous les produits disponibles**,
Afin de **découvrir l'offre**.

## Complexité estimée
**Story Points** : 5 pts

## Critères d'acceptation

### ☑️ Critère 1 : Page catalogue accessible
- **Catégorie** : _Aucune_
- **Valeur du dé** : 🎲 **1**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Une page "/produits" ou "/catalogue" est accessible publiquement (pas besoin d'être connecté).

---

### ☑️ Critère 2 : API de récupération des produits
- **Catégorie** : _Aucune_
- **Valeur du dé** : 🎲 **4**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Une API GET retourne la liste de tous les produits avec leurs informations (nom, prix, image, artisan).

---

### ☑️ Critère 3 : Affichage en grille responsive
- **Catégorie** : _Aucune_
- **Valeur du dé** : 🎲 **2**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Les produits sont affichés en grille (cards) adaptative mobile/desktop. Chaque card montre : photo, nom, prix, nom artisan.

---

### ☑️ Critère 4 : Pagination ou scroll infini
- **Catégorie** : _Aucune_
- **Valeur du dé** : 🎲 **5**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Si > 20 produits, un système de pagination ou scroll infini est implémenté pour éviter de charger tous les produits d'un coup.

---

### ☑️ Critère 5 : Performance de chargement
- **Catégorie** : `[PERF]`
- **Valeur du dé** : 🎲 **6**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : La page se charge en < 2 secondes. Les images sont optimisées (lazy loading, compression). Temps de réponse API < 500ms.

---

### ☑️ Critère 6 : Tests E2E du parcours
- **Catégorie** : `[TESTS]`
- **Valeur du dé** : 🎲 **3**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non (✅ Oui si bonus `[TESTS]` actif)

**Description** : Tests end-to-end (Playwright, Cypress) vérifient : accès à la page, affichage des produits, clic sur un produit.

---

## Notes

### Dépendances
- [x] FM-7 : Ajouter un produit (sinon catalogue vide !)

### Bonus débloqué
_Aucun (US fonctionnelle)_

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
- [ ] Tous les critères d'acceptation sont validés (6/6)
- [ ] Code reviewé et mergé
- [ ] Tests unitaires passent
- [ ] Démo préparée pour la revue de sprint

---

## Note pour l'enseignant

📋 **Template EPIC 3 : Catalogue & Recherche (Client)**

Toutes les US de l'EPIC 3 (FM-14 à FM-19) partagent ces mêmes critères d'acceptation. Seuls changent :
- Le titre de l'US
- La description ("En tant que...")
- L'estimation en story points
