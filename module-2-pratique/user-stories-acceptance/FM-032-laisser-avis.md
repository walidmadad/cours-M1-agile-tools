# US-FM-032 : Laisser un avis sur un produit (Template EPIC 6)

## Type
- [x] Fonctionnelle
- [ ] Technique

## Description
En tant que **client**,
Je veux **laisser un avis sur un produit**,
Afin de **partager mon expérience**.

## Complexité estimée
**Story Points** : 5 pts

## Critères d'acceptation

### ☑️ Critère 1 : Formulaire d'avis accessible
- **Catégorie** : _Aucune_
- **Valeur du dé** : 🎲 **4**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Sur la page produit, un formulaire permet de laisser : note (1-5 étoiles), commentaire texte (max 500 caractères).

---

### ☑️ Critère 2 : Validation métier des avis
- **Catégorie** : _Aucune_
- **Valeur du dé** : 🎲 **2**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Seuls les clients connectés ayant commandé le produit peuvent laisser un avis. Pas de doublon (1 avis par client/produit).

---

### ☑️ Critère 3 : Stockage et affichage des avis
- **Catégorie** : _Aucune_
- **Valeur du dé** : 🎲 **5**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Les avis sont enregistrés en base avec : client, produit, note, commentaire, date. Affichage sous le produit avec moyenne des notes.

---

### ☑️ Critère 4 : Modération anti-spam
- **Catégorie** : `[SECU]`
- **Valeur du dé** : 🎲 **6**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non (✅ Oui si bonus `[SECU]` actif)

**Description** : Filtrage basique anti-spam : détection de mots interdits, limitation à 3 avis/jour par utilisateur. Possibilité pour l'admin de supprimer un avis.

---

### ☑️ Critère 5 : Calcul de la note moyenne en temps réel
- **Catégorie** : `[PERF]`
- **Valeur du dé** : 🎲 **3**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : La note moyenne du produit se met à jour automatiquement (via trigger BDD ou cache) sans latence visible pour l'utilisateur.

---

### ☑️ Critère 6 : Notification à l'artisan
- **Catégorie** : `[DEVOPS]`
- **Valeur du dé** : 🎲 **1**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : L'artisan reçoit une notification (email ou dans l'app) lorsqu'un nouveau avis est posté sur un de ses produits.

---

### ☑️ Critère 7 : Analytics des avis
- **Catégorie** : `[ARCHI]`
- **Valeur du dé** : 🎲 **4**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non (✅ Oui si bonus `[ARCHI]` actif)

**Description** : Un dashboard artisan affiche : nombre d'avis reçus, note moyenne globale, tendance (amélioration/dégradation), produits les mieux notés.

---

## Notes

### Dépendances
- [x] FM-24 : Passer commande (pour vérifier achat)
- [x] FM-15 : Voir le détail d'un produit

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
- [ ] Tous les critères d'acceptation sont validés (7/7)
- [ ] Code reviewé et mergé
- [ ] Tests unitaires passent
- [ ] Démo préparée pour la revue de sprint

---

## Note pour l'enseignant

📋 **Template EPIC 6 : Fonctionnalités Bonus (Nice to Have)**

Toutes les US de l'EPIC 6 (FM-32 à FM-40) partagent ces mêmes critères d'acceptation. Seuls changent :
- Le titre de l'US
- La description ("En tant que...")
- L'estimation en story points

⚠️ **Particularité EPIC 6** : Ces US ont **7 critères** au lieu de 4-6, rendant leur complétion plus difficile. Elles sont "nice to have" et ne doivent être priorisées qu'après le MVP.
