# US-EPIC-2-FM-009 : Ajouter un produit (Template EPIC 2)

## Type
- [x] Fonctionnelle
- [ ] Technique

## Description
En tant qu'**artisan**,
Je veux **ajouter un produit** (nom, description, prix, photo),
Afin de **le vendre**.

## Complexité estimée
**Story Points** : 5 pts (référence)

## Critères d'acceptation

### ☑️ Critère 1 : Formulaire de création produit
- **Catégorie** : _Aucune_
- **Valeur du dé** : 🎲 **2**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Le formulaire contient les champs : nom, description, prix, catégorie et upload de photo. Validation côté client fonctionnelle.

---

### ☑️ Critère 2 : Upload et stockage de l'image
- **Catégorie** : _Aucune_
- **Valeur du dé** : 🎲 **5**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : L'image est uploadée sur un service de stockage (S3, Cloudinary, local) et l'URL est enregistrée en base.

---

### ☑️ Critère 3 : Validation des données métier
- **Catégorie** : _Aucune_
- **Valeur du dé** : 🎲 **3**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Le prix est positif, le nom fait min 3 caractères, la description max 500 caractères. Messages d'erreur clairs.

---

### ☑️ Critère 4 : Produit créé et lié à l'artisan
- **Catégorie** : _Aucune_
- **Valeur du dé** : 🎲 **4**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Le produit est enregistré en base avec l'ID de l'artisan connecté. Redirection vers la liste des produits après création.

---

### ☑️ Critère 5 : Tests d'intégration API
- **Catégorie** : `[TESTS]`
- **Valeur du dé** : 🎲 **6**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non (✅ Oui si bonus `[TESTS]` actif)

**Description** : Tests d'intégration vérifient : création réussie, gestion des erreurs (prix négatif, image trop lourde), autorisation (seul l'artisan peut créer).

---

## Notes

### Dépendances
- [x] EPIC-1-FM-1 : Créer un compte artisan
- [x] EPIC-1-FM-2 : Se connecter (artisan)

### Bonus débloqué
_Aucun (US fonctionnelle)_

### Historique des tentatives

| Sprint | Dés lancés | Critères validés | Statut |
|--------|------------|------------------|--------|
| 0 | 12 | 5 | Terminé |


---

## Définition of Done (DoD)
- [ ] Tous les critères d'acceptation sont validés (5/5)
- [ ] Code reviewé et mergé
- [ ] Tests unitaires passent
- [ ] Démo préparée pour la revue de sprint

---

## Note pour l'enseignant

📋 **Template EPIC 2 : Gestion des Produits (Artisan)**

Toutes les US de l'EPIC 2 (EPIC-2-FM-9 à EPIC-2-FM-13) partagent ces mêmes critères d'acceptation. Seuls changent :
- Le titre de l'US
- La description ("En tant que...")
- L'estimation en story points
