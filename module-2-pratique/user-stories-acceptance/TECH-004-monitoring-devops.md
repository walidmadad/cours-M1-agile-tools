# US-TECH-004 : Mettre en place monitoring et alerting

## Type
- [ ] Fonctionnelle
- [x] Technique

## Description
En tant qu'**équipe de développement**,
Je veux **disposer d'un système de monitoring et d'alerting**,
Afin de **détecter et réagir rapidement aux incidents en production**.

## Complexité estimée
**Story Points** : 8 pts

## Critères d'acceptation

### ☑️ Critère 1 : Métriques applicatives collectées
- **Catégorie** : `[DEVOPS]`
- **Valeur du dé** : 🎲 **5**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Un outil (Prometheus, Datadog, New Relic) collecte les métriques : temps de réponse, taux d'erreur, requêtes/sec.

---

### ☑️ Critère 2 : Dashboard de visualisation
- **Catégorie** : `[DEVOPS]`
- **Valeur du dé** : 🎲 **3**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Un dashboard (Grafana, Datadog UI) affiche en temps réel les métriques clés : santé de l'API, base de données, services.

---

### ☑️ Critère 3 : Logs centralisés
- **Catégorie** : `[DEVOPS]`
- **Valeur du dé** : 🎲 **6**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Les logs de l'application sont centralisés (ELK Stack, Loki, CloudWatch) et consultables avec une interface de recherche.

---

### ☑️ Critère 4 : Alertes automatiques configurées
- **Catégorie** : `[DEVOPS]`
- **Valeur du dé** : 🎲 **4**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Des alertes automatiques (Slack, PagerDuty, email) se déclenchent si : taux d'erreur > 5%, temps de réponse > 2s, service down.

---

### ☑️ Critère 5 : Runbook de réponse aux incidents
- **Catégorie** : `[DOC]`
- **Valeur du dé** : 🎲 **2**
- **Statut** : ⬜ Non validé
- **Permanent** : ❌ Non

**Description** : Un document décrit la procédure à suivre en cas d'alerte (qui contacter, quels logs vérifier, comment rollback).

---

## Notes

### Dépendances
- Recommandé : avoir une application déployée en staging/production

### Bonus débloqué (US technique)
🎁 **🔄 Relance de dé** : Une fois cette US complétée, l'équipe peut **relancer 1 dé par sprint** (choisir quel dé relancer après le jet initial).

Ce bonus permet de "corriger" un mauvais lancer et augmente significativement les chances de terminer une story.

### Historique des tentatives

| Sprint | Dés lancés | Critères validés | Statut |
|--------|------------|------------------|--------|
| - | - | - | ⏳ Pas encore jouée |

---

## Définition of Done (DoD)
- [ ] Tous les critères d'acceptation sont validés (5/5)
- [ ] Dashboard accessible et fonctionnel
- [ ] Alerte testée (simulation d'incident)
- [ ] Démo technique préparée pour la revue de sprint

---

## Conseil stratégique

🚨 **US critique pour la production** : Cette US est essentielle avant le lancement en production. Sans monitoring, l'équipe est "aveugle" face aux incidents.

Le bonus de relance est très puissant en fin de sprint quand il manque juste 1 critère pour terminer une story !
