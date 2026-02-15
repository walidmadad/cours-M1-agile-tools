# US-FM-001 : Créer un compte artisan

## Type
- [x] Fonctionnelle
- [ ] Technique

## Description
En tant qu'**artisan**,
Je veux **créer un compte**,
Afin de **pouvoir vendre mes produits**.

## Complexité estimée
**Story Points** : 3 pts

## Critères d'acceptation

### ☑️ Critère 1 : Formulaire d'inscription fonctionnel
- **Catégorie** : _Aucune_
- **Valeur du dé** : 🎲 **1**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Le formulaire contient les champs email, nom, prénom, mot de passe et confirmation mot de passe avec validation côté client.

---

### ☑️ Critère 2 : Validation des données
- **Catégorie** : `[SECU]`
- **Valeur du dé** : 🎲 **4**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non (✅ Oui si bonus `[SECU]` actif)

**Description** : L'email est unique en base, le mot de passe respecte les règles (min 8 caractères, 1 majuscule, 1 chiffre). Messages d'erreur clairs affichés.

---

### ☑️ Critère 3 : Compte créé en base de données
- **Catégorie** : _Aucune_
- **Valeur du dé** : 🎲 **3**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Les données sont enregistrées en base avec mot de passe hashé (bcrypt). L'utilisateur reçoit un message de confirmation.

---

### ☑️ Critère 4 : Email de bienvenue envoyé
- **Catégorie** : _Aucune_
- **Valeur du dé** : 🎲 **5**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Un email de bienvenue est envoyé automatiquement à l'artisan après création du compte.

---

## Notes

### Dépendances
- Aucune (première story à implémenter)

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
- [ ] Tous les critères d'acceptation sont validés (4/4)
- [ ] Code reviewé et mergé
- [ ] Tests unitaires passent
- [ ] Démo préparée pour la revue de sprint
