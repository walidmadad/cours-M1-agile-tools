# US-FM-020 : Ajouter un produit au panier

## Type
- [x] Fonctionnelle
- [ ] Technique

## Description
En tant que **client**,
Je veux **ajouter un produit au panier**,
Afin de **préparer ma commande**.

## Complexité estimée
**Story Points** : 3 pts

## Critères d'acceptation

### ☑️ Critère 1 : Bouton "Ajouter au panier" visible
- **Catégorie** : _Aucune_
- **Valeur du dé** : 🎲 **2**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Un bouton "Ajouter au panier" est affiché sur la page détail du produit et est cliquable.

---

### ☑️ Critère 2 : Produit ajouté au panier côté serveur
- **Catégorie** : _Aucune_
- **Valeur du dé** : 🎲 **5**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Lors du clic, une requête API ajoute le produit au panier de l'utilisateur connecté. Le panier est persisté en base de données.

---

### ☑️ Critère 3 : Vérification du stock disponible
- **Catégorie** : _Aucune_
- **Valeur du dé** : 🎲 **4**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Avant ajout, le système vérifie que le stock est > 0. Sinon, un message d'erreur s'affiche ("Produit en rupture de stock").

---

### ☑️ Critère 4 : Feedback visuel immédiat
- **Catégorie** : _Aucune_
- **Valeur du dé** : 🎲 **1**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Un message de confirmation s'affiche ("Produit ajouté au panier ✓") et l'icône panier se met à jour avec le nombre d'articles.

---

### ☑️ Critère 5 : Tests unitaires pour la logique métier
- **Catégorie** : `[TESTS]`
- **Valeur du dé** : 🎲 **6**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non (✅ Oui si bonus `[TESTS]` actif)

**Description** : Tests unitaires couvrent les cas : ajout normal, stock insuffisant, utilisateur non connecté.

---

## Notes

### Dépendances
- [x] FM-14 : Voir tous les produits disponibles
- [x] FM-15 : Voir le détail d'un produit
- [x] FM-6 : Se connecter (client)

### Bonus débloqué
_Aucun (US fonctionnelle)_

### Historique des tentatives

| Sprint | Dés lancés | Critères validés | Statut |
|--------|------------|------------------|--------|
| - | - | - | ⏳ Pas encore jouée |

---

## Définition of Done (DoD)
- [ ] Tous les critères d'acceptation sont validés (5/5)
- [ ] Code reviewé et mergé
- [ ] Tests unitaires passent
- [ ] Démo préparée pour la revue de sprint
