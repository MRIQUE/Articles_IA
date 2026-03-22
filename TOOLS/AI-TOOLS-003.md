---
id: AI-TOOLS-003
type: tools
title: "Glossaire de l'ingenierie des agents IA : les concepts cles a connaitre"
version: 1.0
status: draft
created: 2026-03-22
updated: 2026-03-22
---

# Glossaire de l'ingenierie des agents IA : les concepts cles a connaitre

## Resume

L'ingenierie des agents IA repose sur un vocabulaire technique specifique qui evolue rapidement. Ce glossaire rassemble les definitions essentielles pour comprendre l'architecture, le fonctionnement et l'evaluation des agents autonomes. Les concepts sont organises en six domaines : architecture et boucle de controle, gestion du contexte, conception des outils, memoire et persistance, evaluation et observabilite, securite et resilience.

## Architecture et boucle de controle

### Agent Loop

La boucle **perception, decision, action, feedback** qui constitue le coeur d'un agent autonome. En pratique, elle tient en moins de 20 lignes de code et reste remarquablement stable : les nouvelles capacites s'ajoutent autour de la boucle (outils, prompts, etat externe), jamais en modifiant ses mecanismes internes.

### Orchestrator-Workers

Patron multi-agent ou un agent central decompose dynamiquement les taches, les delegue a des agents specialises (workers), puis synthetise les resultats. Les workers operent dans des contextes isoles et ne remontent que des resumes, preservant ainsi le contexte principal de toute pollution.

### Evaluator-Optimizer

Patron de controle iteratif ou un **generateur** produit une sortie, un **evaluateur** fournit un retour critique, et la boucle continue jusqu'a ce que le resultat atteigne un standard de qualite defini. Particulierement adapte aux taches dont la qualite est difficile a codifier (traduction, ecriture creative).

### Director Mode et Orchestrator Mode

Deux modeles de collaboration humain-agent :

- **Director Mode** : interaction synchrone, tour par tour, entre l'humain et un seul agent. Le contexte disparait en fin de session ; la sortie est ephemere.
- **Orchestrator Mode** : delegation asynchrone. L'humain fixe l'objectif au depart, plusieurs agents travaillent en parallele, et l'humain n'intervient qu'a la fin pour valider des artefacts persistants (branches, PRs).

La valeur du multi-agent reside dans ce basculement d'une supervision humaine continue vers une revue finale de livrables concrets.

## Gestion du contexte

### Context Engineering

L'art de structurer et gerer l'information injectee dans la fenetre de contexte du modele pour maintenir la qualite des decisions. Cela inclut le decoupage en couches (permanente, a la demande, runtime, memoire), la compression, et le chargement conditionnel des connaissances.

### Context Rot

Degradation progressive de la qualite decisionnelle d'un agent lorsque du contenu non pertinent domine sa fenetre de contexte. Beaucoup de problemes attribues a tort aux limites du modele sont en realite causes par une mauvaise organisation du contexte.

### Prompt Caching

Mecanisme de reutilisation des paires Key-Value deja calculees par le Transformer lorsque le prefixe d'une requete correspond exactement a une requete precedente. La condition est un match exact : un seul token different invalide le cache. D'ou l'importance d'un prompt systeme stable et d'un chargement dynamique place en fin de contexte.

### Skill Loading

Patron ou le prompt systeme ne conserve qu'un index leger des competences disponibles, tandis que le contenu detaille de chaque skill n'est injecte dans le contexte que lorsqu'il est effectivement requis. Cela preserve le budget de tokens et protege la stabilite du prefixe pour le cache.

## Conception des outils

### ACI (Agent-Computer Interface)

Principe de conception selon lequel les outils doivent etre construits pour les objectifs de l'agent, et non comme de simples wrappers d'API. Un bon outil exprime l'action cible en un seul appel, decrit clairement quand l'utiliser et quand ne pas l'utiliser, et retourne des erreurs structurees contenant des suggestions de correction.

## Memoire et persistance

### Memory Consolidation

Processus par lequel un agent compresse et archive son historique conversationnel tout en preservant les decisions architecturales, les taches inachevees et les contraintes cles. Le mecanisme doit etre reversible : le systeme deplace un pointeur sans supprimer les messages bruts, permettant un retour a l'archive complete en cas d'echec de la consolidation.

## Evaluation et observabilite

### Pass@k et Pass^k

Deux metriques d'evaluation complementaires :

- **Pass@k** : au moins un succes sur k essais. Utilise en phase de developpement pour explorer les limites de capacite ("L'agent peut-il theoriquement reussir cette tache ?").
- **Pass^k** : tous les k essais sont des succes. Utilise en pre-production pour les tests de regression ("A-t-on casse une fonctionnalite existante ?").

Melanger les deux conduit a des erreurs de jugement.

### Grader (Code, Model, Human)

Les trois types de correcteurs pour evaluer un agent :

| Type | Methode | Certitude | Cas d'usage |
|---|---|---|---|
| **Code Grader** | Tests unitaires, matching, diffs structurels | Maximale | Reponse correcte explicite |
| **Model Grader** | Scoring LLM, comparaison A/B, consensus multi-modeles | Moyenne | Qualite semantique, style, raisonnement |
| **Human Grader** | Revue experte, files d'annotation | Fiable mais lente | Etablir les baselines, calibrer les juges automatises |

Regle : si une reponse correcte existe, toujours commencer par le Code Grader.

### Harness

Infrastructure de test, validation et contraintes construite autour d'un agent. Elle comprend au minimum : des baselines d'acceptation, des limites d'execution, des signaux de feedback et des mecanismes de repli. C'est le harness, bien plus que le modele brut, qui determine si un systeme converge de maniere stable en production.

## Securite et resilience

### Prompt Injection

Attaque consistant a glisser des instructions malveillantes dans du contenu externe (emails, pages web, documents) qu'un agent va ingerer, exploitant la confusion entre donnees et commandes. La parade repose sur le principe du moindre privilege, le marquage explicite du contenu non fiable, la confirmation obligatoire pour les operations sensibles, et la verification independante par un second LLM sur les chemins critiques.

### Provider Fallback

Mecanisme de bascule automatique entre fournisseurs de modeles (Anthropic, OpenAI, etc.) lorsqu'un provider tombe en panne ou atteint ses limites de debit (503, rate limits). L'agent tente sequentiellement chaque provider configure, garantissant la continuite de service sans intervention humaine.

## Sources

- Tw93, "You Don't Know AI Agents: Principles, Architecture, and Engineering Practices", mars 2026.
