# US-FM-027 : Voir mes commandes reçues (Template EPIC 5)

## Type
- [x] Fonctionnelle
- [ ] Technique

## Description
En tant qu'**artisan**,
Je veux **voir mes commandes reçues**,
Afin de **les préparer**.

## Complexité estimée
**Story Points** : 5 pts

## Critères d'acceptation

### ☑️ Critère 1 : Page de gestion des commandes
- **Catégorie** : _Aucune_
- **Valeur du dé** : 🎲 **3**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Une page "/mes-commandes" accessible uniquement par l'artisan connecté affiche toutes ses commandes.

---

### ☑️ Critère 2 : API de récupération des commandes
- **Catégorie** : _Aucune_
- **Valeur du dé** : 🎲 **5**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Une API GET retourne les commandes de l'artisan avec : ID, date, client, produits, statut, montant total.

---

### ☑️ Critère 3 : Affichage du statut et détails
- **Catégorie** : _Aucune_
- **Valeur du dé** : 🎲 **2**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Pour chaque commande : statut visible (en préparation, expédiée, livrée), liste des produits, adresse de livraison, montant.

---

### ☑️ Critère 4 : Filtrage par statut
- **Catégorie** : _Aucune_
- **Valeur du dé** : 🎲 **4**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : L'artisan peut filtrer les commandes par statut (toutes, en préparation, expédiées, livrées) pour mieux organiser son travail.

---

### ☑️ Critère 5 : Sécurité et autorisation
- **Catégorie** : `[SECU]`
- **Valeur du dé** : 🎲 **6**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non (✅ Oui si bonus `[SECU]` actif)

**Description** : L'artisan ne peut voir QUE ses commandes (vérification côté serveur). Toute tentative d'accès aux commandes d'un autre artisan est refusée (403).

---

### ☑️ Critère 6 : Notifications temps réel
- **Catégorie** : `[DEVOPS]`
- **Valeur du dé** : 🎲 **1**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Lorsqu'une nouvelle commande arrive, l'artisan reçoit une notification (badge, sound, ou webhook) sans avoir à rafraîchir la page.

---

## Notes

### Dépendances
- [x] FM-24 : Passer commande (sinon pas de commandes à afficher)
- [x] FM-2 : Se connecter (artisan)

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

📋 **Template EPIC 5 : Gestion des Commandes**

Toutes les US de l'EPIC 5 (FM-27 à FM-31) partagent ces mêmes critères d'acceptation. Seuls changent :
- Le titre de l'US
- La description ("En tant que...")
- L'estimation en story points
