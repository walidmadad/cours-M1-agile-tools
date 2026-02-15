# US-TECH-001 : Mettre en place une infrastructure de test

## Type
- [ ] Fonctionnelle
- [x] Technique

## Description
En tant qu'**équipe de développement**,
Je veux **disposer d'une infrastructure de test dédiée**,
Afin de **valider mes développements sans impacter la production**.

## Complexité estimée
**Story Points** : 5 pts

## Critères d'acceptation

### ☑️ Critère 1 : Environnement de test isolé
- **Catégorie** : `[INFRA_TEST]`
- **Valeur du dé** : 🎲 **3**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Un environnement de test est configuré (serveur staging, Docker Compose local, ou environnement cloud) complètement isolé de la production.

---

### ☑️ Critère 2 : Base de données de test dédiée
- **Catégorie** : `[INFRA_TEST]`
- **Valeur du dé** : 🎲 **5**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Une base de données de test est créée avec des données de seed automatiques (artisans, produits, clients factices).

---

### ☑️ Critère 3 : Scripts de reset automatique
- **Catégorie** : `[INFRA_TEST]`
- **Valeur du dé** : 🎲 **2**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Un script permet de réinitialiser l'environnement de test à son état initial en une commande (`npm run test:reset`).

---

### ☑️ Critère 4 : Documentation de l'infrastructure
- **Catégorie** : `[DOC]`
- **Valeur du dé** : 🎲 **1**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Un fichier README décrit comment démarrer l'environnement de test, avec les variables d'environnement nécessaires.

---

## Notes

### Dépendances
- Aucune (peut être faite dès le Sprint 1)

### Bonus débloqué (US technique)
🎁 **🎲 Dé supplémentaire** : Une fois cette US complétée, l'équipe peut lancer **2 dés** au lieu d'1 pour tous les sprints suivants !

### Historique des tentatives

| Sprint | Dés lancés | Critères validés | Statut |
|--------|------------|------------------|--------|
| - | - | - | ⏳ Pas encore jouée |

---

## Définition of Done (DoD)
- [ ] Tous les critères d'acceptation sont validés (4/4)
- [ ] Infrastructure testée et validée par l'équipe
- [ ] Documentation à jour
- [ ] Démo technique préparée pour la revue de sprint

---

## Conseil stratégique

⚠️ **US stratégique !** Cette User Story devrait être priorisée dans les premiers sprints car elle débloque le bonus le plus puissant du jeu : **le 2ème dé**. Cela double vos chances de valider les critères d'acceptation dans les sprints suivants.
