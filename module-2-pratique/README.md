# Module 2 - Serious Game : FlowMaster (3h)

## Objectifs pédagogiques

À la fin de ce module, les étudiants seront capables de :

1. **Maîtriser Jira** : Créer, estimer, prioriser et faire progresser des stories
2. **Expérimenter Push vs Pull** : Comprendre la différence entre flux poussé (Scrum) et flux tiré (Kanban)
3. **Gérer l'imprévu** : S'adapter aux changements de priorités, bugs, et contraintes
4. **Mesurer le flux** : Utiliser les métriques (vélocité, lead time, throughput)
5. **Livrer de la valeur** : Comprendre l'importance de livrer régulièrement

---

## Scénario du jeu : FlowMaster E-Commerce

### Contexte

Vous êtes l'équipe de développement de **FlowMaster**, une startup qui lance une plateforme e-commerce de vente de produits artisanaux.

**Objectif business :** Lancer une beta publique fonctionnelle dans **6 sprints** (= 6 tours de jeu).

**Contraintes réalistes :**
- Budget limité (vélocité limitée)
- Changements de priorités (clients, concurrence)
- Bugs imprévus
- Dépendances techniques
- Deadlines marketing

---

## Structure du jeu

### Durée totale : 3h

**Répartition :**
- Introduction + Setup Jira : 20 min
- **Phase 1 : Scrum (flux poussé)** : 60 min (3 sprints × 20 min)
- Débriefing Phase 1 : 10 min
- **Phase 2 : Kanban (flux tiré)** : 60 min (3 sprints × 20 min)
- Débriefing Phase 2 : 10 min
- Comparaison et conclusion : 20 min

---

## Organisation des équipes

**Équipes de 4-5 personnes**

**Rôles à distribuer :**

1. **Product Owner** (1 personne)
   - Priorise le backlog
   - Valide les stories (vérifie la DoD)
   - Décide des compromis

2. **Scrum Master / Facilitateur** (1 personne)
   - Gère le board Jira
   - Note les dés tirés
   - Présente les métriques

3. **Développeurs** (2-3 personnes)
   - Réalisent les stories (tirent les dés)
   - Estiment les stories
   - Signalent les blocages

**Important :** Les rôles tournent entre Phase 1 et Phase 2 pour que chacun expérimente différents rôles.

---

## Fichiers du module

### 📚 Documentation principale
1. **backlog-initial.md** : Backlog de départ (40 User Stories fonctionnelles)
2. **regles-du-jeu.md** : Règles complètes, DoD, système de dés 🎲
3. **systeme-de-scoring.md** : Documentation complète du système de scoring par dés
4. **categories-techniques.md** : Référence des catégories techniques et bonus

### 🎴 Cartes User Stories
5. **user-stories/TEMPLATE.md** : Template vierge pour créer de nouvelles cartes
6. **user-stories/FM-*.md** : Templates de critères par EPIC (1 à 6)
7. **user-stories/TECH-*.md** : User Stories techniques (débloquent des bonus)
8. **user-stories/BUG-*.md** : Bugs à gérer pendant le jeu
9. **user-stories/FEAT-*.md** : Features urgentes (changements de priorité)

### 📊 Utilitaires
1. **guide-animateur.md** : Instructions pour l'enseignant
2. **setup-jira.md** : Guide de configuration Jira
3. **fiche-metriques.md** : Tableau de suivi des métriques

---

## Système de jeu ( Dés) 🎲

### Principe
- Chaque User Story a des **critères d'acceptation** avec une valeur de dé (1 à 6)
- L'équipe dispose d'un **temps limité** (5 min par sprint) pour lancer les dés
- Un critère est validé si le dé obtient **exactement sa valeur**
- Une US est **terminée** si **tous ses critères** sont validés

### Bonus techniques
Les User Stories techniques débloquent des bonus permanents :
- 🎲 **+1 dé** (`[INFRA_TEST]`) - Lancer 2 dés au lieu d'1
- 🔒 **Critères permanents** (`[CI/CD]`, `[TESTS]`, `[SECU]`, `[ARCHI]`) - Ne plus rejouer certains critères
- 🔄 **Relancer 1 dé/sprint** (`[DEVOPS]`)
- ⏱️ **+30 secondes** (`[PERF]`)

**Stratégie gagnante :** Prioriser les US techniques tôt pour débloquer les bonus !

---

## Prochaines étapes

1. Lire **regles-du-jeu.md** (focus sur Option C 🎲)
2. Consulter **systeme-de-scoring.md** pour comprendre les mécaniques
3. Parcourir les templates dans **user-stories/**
4. Setup Jira (suivre **setup-jira.md**)
5. Préparer des dés à 6 faces (2 par équipe)
6. C'est parti ! 🚀
