# BUG-005 : Pipeline CI/CD échoue (scripts mal configurés)

## Type
- [ ] Fonctionnelle
- [ ] Technique
- [x] **Bug** - Haute

## Description
**Problème détecté** : Le pipeline CI/CD échoue systématiquement depuis 2 jours. Les builds ne passent plus, empêchant tout déploiement. Investigation révèle que des scripts de migration de BDD et des variables d'environnement ont été mal configurés.

**Comportement attendu** : Le pipeline doit passer avec succès et déployer automatiquement en staging.

**Impact** : 🟠 Haute - Bloque tous les déploiements, l'équipe ne peut plus livrer de nouvelles features.

## Complexité estimée
**Story Points** : 5 pts (investigation + correction multi-fichiers)

## Critères d'acceptation (Fix du bug)

### ☑️ Critère 1 : Investigation et diagnostic
- **Catégorie** : `[DEVOPS]`
- **Valeur du dé** : 🎲 **2**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Analyse des logs CI/CD pour identifier tous les points de défaillance : scripts de migration, variables d'environnement manquantes, permissions, chemins de fichiers.

---

### ☑️ Critère 2 : Correction des scripts de migration
- **Catégorie** : `[CI/CD]`
- **Valeur du dé** : 🎲 **4**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non (✅ Oui si bonus `[CI/CD]` actif)

**Description** : Les scripts de migration BDD sont corrigés avec les bons chemins, ordres d'exécution, et gestion d'erreurs. Rollback possible en cas d'échec.

---

### ☑️ Critère 3 : Variables d'environnement validées
- **Catégorie** : `[CI/CD]`
- **Valeur du dé** : 🎲 **3**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non (✅ Oui si bonus `[CI/CD]` actif)

**Description** : Toutes les variables d'environnement nécessaires sont documentées et configurées dans le CI (GitHub Secrets, GitLab CI Variables). Un script de validation vérifie leur présence au début du pipeline.

---

### ☑️ Critère 4 : Tests du pipeline en environnement de test
- **Catégorie** : `[TESTS]`
- **Valeur du dé** : 🎲 **5**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non (✅ Oui si bonus `[TESTS]` actif)

**Description** : Le pipeline est testé de bout en bout sur une branche de test avant d'être mergé sur main. Build + tests + déploiement staging passent.

---

### ☑️ Critère 5 : Documentation et post-mortem
- **Catégorie** : `[DOC]`
- **Valeur du dé** : 🎲 **1**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Un document post-mortem explique : ce qui a cassé, pourquoi, comment c'est corrigé, et comment éviter ce problème à l'avenir (checklist de validation).

---

### ☑️ Critère 6 : Alerting sur échec pipeline
- **Catégorie** : `[DEVOPS]`
- **Valeur du dé** : 🎲 **6**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Des alertes automatiques (Slack, email) notifient l'équipe immédiatement en cas d'échec du pipeline pour éviter qu'il reste cassé 2 jours sans que personne ne s'en aperçoive.

---

## Notes

### Dépendances
- Bloque : TOUTES les US qui nécessitent un déploiement
- Apparaît pendant : Sprint 3 ou 4

### Priorité
🟠 **Haute** - À traiter en urgence. Sans CI/CD fonctionnel, impossible de livrer quoi que ce soit.

### Impact sur la vélocité
⚠️ **Attention** : Ce bug a probablement **déjà fait perdre 2 jours** à l'équipe. Cela réduit la vélocité effective du sprint.

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
- [ ] Tous les critères d'acceptation sont validés (6/6)
- [ ] Pipeline CI/CD fonctionne de nouveau
- [ ] Au moins 1 déploiement réussi en staging
- [ ] Post-mortem rédigé et partagé avec l'équipe

---

## Note pédagogique

💡 **Leçon apprise** :

Ce bug illustre l'importance de :
1. **Tester le pipeline** comme on teste le code
2. **Documenter la configuration** (variables, secrets, scripts)
3. **Monitorer le CI/CD** pour détecter les pannes rapidement
4. **Avoir une US technique CI/CD** en amont aurait pu éviter ce problème (bonus `[CI/CD]` permanent !)

**Question pour l'équipe** : Auriez-vous dû prioriser TECH-002 (Pipeline CI/CD) plus tôt dans les sprints ? 🤔
