# US-TECH-003 : Optimiser les tests unitaires (< 3 minutes)

## Type
- [ ] Fonctionnelle
- [x] Technique

## Description
En tant qu'**équipe de développement**,
Je veux **que mes tests unitaires s'exécutent en moins de 3 minutes**,
Afin de **maintenir un feedback rapide et une boucle de développement efficace**.

## Complexité estimée
**Story Points** : 5 pts

## Critères d'acceptation

### ☑️ Critère 1 : Suite de tests complète < 3 min
- **Catégorie** : `[TESTS]`
- **Valeur du dé** : 🎲 **5**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non (✅ Oui si bonus `[TESTS]` actif)

**Description** : L'ensemble des tests unitaires s'exécute en moins de 3 minutes en local et dans le CI.

---

### ☑️ Critère 2 : Tests parallélisés
- **Catégorie** : `[TESTS]`
- **Valeur du dé** : 🎲 **4**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non (✅ Oui si bonus `[TESTS]` actif)

**Description** : Les tests s'exécutent en parallèle pour optimiser la vitesse (via Jest --maxWorkers ou équivalent).

---

### ☑️ Critère 3 : Mocks et stubs pour les dépendances externes
- **Catégorie** : `[TESTS]`
- **Valeur du dé** : 🎲 **3**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non (✅ Oui si bonus `[TESTS]` actif)

**Description** : Les appels API, base de données et services externes sont mockés pour accélérer les tests.

---

### ☑️ Critère 4 : Rapport de temps d'exécution
- **Catégorie** : `[PERF]`
- **Valeur du dé** : 🎲 **2**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Un rapport affiche les tests les plus lents pour identifier les points d'optimisation (`jest --verbose`).

---

## Notes

### Dépendances
- Recommandé : avoir déjà quelques tests unitaires en place

### Bonus débloqué (US technique)
🎁 **🔒 Critères `[TESTS]` permanents** : Une fois cette US complétée, tous les critères marqués `[TESTS]` validés dans d'autres stories **ne doivent plus être rejoués** !

Cela signifie que tout ce qui concerne les tests unitaires, couverture et validation sera "acquis" définitivement.

### Historique des tentatives

| Sprint | Dés lancés | Critères validés | Statut |
|--------|------------|------------------|--------|
| - | - | - | ⏳ Pas encore jouée |

---

## Définition of Done (DoD)
- [ ] Tous les critères d'acceptation sont validés (4/4)
- [ ] Tests exécutés et chronométrés (< 3 min)
- [ ] Documentation des mocks disponible
- [ ] Démo technique préparée pour la revue de sprint

---

## Conseil stratégique

✅ **Impact qualité** : Cette US améliore la confiance dans le code ET accélère le développement. Les développeurs peuvent relancer les tests fréquemment sans attendre.
