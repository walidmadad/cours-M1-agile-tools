# US-TECH-002 : Mettre en place un pipeline CI/CD

## Type
- [ ] Fonctionnelle
- [x] Technique

## Description
En tant qu'**équipe de développement**,
Je veux **disposer d'un pipeline CI/CD automatisé**,
Afin de **déployer rapidement et en toute confiance**.

## Complexité estimée
**Story Points** : 8 pts

## Critères d'acceptation

### ☑️ Critère 1 : Build automatique sur chaque commit
- **Catégorie** : `[CI/CD]`
- **Valeur du dé** : 🎲 **4**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non (✅ Oui si bonus `[CI/CD]` actif)

**Description** : Un pipeline (GitHub Actions, GitLab CI, Jenkins) compile automatiquement le code à chaque push sur la branche principale.

---

### ☑️ Critère 2 : Tests automatiques dans le pipeline
- **Catégorie** : `[CI/CD]`
- **Valeur du dé** : 🎲 **3**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non (✅ Oui si bonus `[CI/CD]` actif)

**Description** : Le pipeline exécute automatiquement les tests unitaires et d'intégration. Le build échoue si les tests ne passent pas.

---

### ☑️ Critère 3 : Déploiement automatique en staging
- **Catégorie** : `[CI/CD]`
- **Valeur du dé** : 🎲 **6**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non (✅ Oui si bonus `[CI/CD]` actif)

**Description** : Si le build et les tests passent, l'application est automatiquement déployée sur l'environnement de staging.

---

### ☑️ Critère 4 : Notifications de statut
- **Catégorie** : `[DEVOPS]`
- **Valeur du dé** : 🎲 **2**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : L'équipe reçoit une notification (Slack, email, Discord) en cas de succès ou d'échec du pipeline.

---

### ☑️ Critère 5 : Badge de statut dans le README
- **Catégorie** : `[DOC]`
- **Valeur du dé** : 🎲 **1**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Un badge indiquant le statut du build (passing/failing) est affiché dans le README.md du projet.

---

## Notes

### Dépendances
- [ ] TECH-001 : Infrastructure de test (recommandé mais pas bloquant)

### Bonus débloqué (US technique)
🎁 **🔒 Critères `[CI/CD]` permanents** : Une fois cette US complétée, tous les critères marqués `[CI/CD]` validés dans d'autres stories **ne doivent plus être rejoués** !

Cela signifie que tout ce qui touche au build, tests automatiques et déploiement sera "acquis" définitivement.

### Historique des tentatives

| Sprint | Dés lancés | Critères validés | Statut |
|--------|------------|------------------|--------|
| - | - | - | ⏳ Pas encore jouée |

---

## Définition of Done (DoD)
- [ ] Tous les critères d'acceptation sont validés (5/5)
- [ ] Pipeline testé avec un vrai commit
- [ ] Documentation du pipeline disponible
- [ ] Démo technique préparée pour la revue de sprint

---

## Conseil stratégique

⚠️ **US à forte valeur !** Cette US est complexe (8 pts) mais débloque un bonus permanent très puissant. Tous les aspects CI/CD validés une fois ne seront plus à rejouer, ce qui sécurise vos déploiements futurs.
