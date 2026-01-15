---
id: AI-RISK-001
type: risk
title: "Agents Rule of Two : limiter les capacités des agents IA pour éviter les catastrophes"
version: 1.1
status: published
created: 2026-01-15
updated: 2026-01-15
---

# Agents IA : pourquoi la "règle de deux" peut éviter le pire

## Résumé

À mesure que les agents d'intelligence artificielle quittent les laboratoires pour piloter des logiciels, consulter des données sensibles ou agir sur le monde réel, une question centrale émerge : comment réduire les risques quand ces agents peuvent être manipulés par de simples instructions textuelles ?

C'est dans ce contexte — la sécurité des agents IA face aux attaques par prompt injection — qu'apparaît un principe simple et pragmatique : la Agents Rule of Two.

Proposée sur le blog de Meta et popularisée par le chercheur et développeur Simon Willison, cette règle vise moins à "corriger" l'IA qu'à concevoir des systèmes qui restent sûrs même quand l'IA se trompe.

## Le problème : une IA trop confiante

Un agent IA moderne peut :

- lire des contenus externes (emails, pages web, documents),
- appeler des outils (API, bases de données, systèmes métiers),
- prendre des décisions et agir sans validation humaine.

Or, il suffit parfois d'un texte piégé — une phrase cachée dans un PDF ou une page web — pour détourner son comportement. C'est ce qu'on appelle une attaque par prompt injection.

## La règle de deux, en une phrase

Un agent IA ne doit jamais cumuler plus de deux capacités critiques parmi trois, dans une même session autonome.

Ces trois capacités sont :

**A — Traiter des entrées non fiables**
Contenus écrits par des tiers : web, emails, fichiers utilisateurs.

**B — Accéder à des systèmes ou données sensibles**
Données personnelles, secrets d'entreprise, environnements de production.

**C — Modifier l'état ou communiquer vers l'extérieur**
Écrire dans une base, déclencher une action, envoyer des données.

A + B + C = zone de danger maximal

## Des exemples concrets

### L'assistant email trop zélé

Un agent :
- lit des emails externes (A),
- a accès à votre CRM client (B),
- peut envoyer des emails automatiquement (C).

Un email piégé peut lui ordonner d'exfiltrer la base clients.
Les trois conditions sont réunies : danger.

### L'agent analyste interne

Un agent :
- analyse des rapports internes fiables (pas A),
- accède à des données sensibles (B),
- produit un tableau de synthèse (C).

Deux conditions seulement : risque limité.

### Le chatbot public sandboxé

Un agent :
- discute avec des utilisateurs inconnus (A),
- peut répondre ou appeler une API factice (C),
- mais n'a accès à aucun système réel (pas B).

Deux conditions : acceptable si bien isolé.

## Pourquoi ne pas simplement "bloquer les attaques" ?

Parce que cela ne fonctionne pas.

Des travaux récents montrent que toutes les défenses connues contre les prompt injections finissent par céder, dès lors que l'attaquant peut tester, ajuster et recommencer.

Autrement dit :
- filtrer les prompts : inefficace
- entraîner l'IA à "refuser" : inefficace
- détecter les attaques automatiquement : inefficace

La seule stratégie robuste aujourd'hui consiste à limiter structurellement ce qu'un agent peut faire.

## Clarification : risque d'erreur vs risque de sécurité

Une objection légitime émerge souvent : un agent qui peut agir (C) et qui peut se tromper est déjà dangereux. Pourquoi trois conditions ?

La réponse tient dans une distinction fondamentale :

- **Erreur interne** = problème d'ingénierie (qualité, fiabilité)
- **Erreur provoquée** = problème de sécurité (attaque hostile)

La Rule of Two ne vise pas à empêcher les bugs, les hallucinations ou les erreurs de raisonnement. Elle vise à empêcher la **prise de contrôle hostile** par un tiers via prompt injection.

### Pourquoi une seule capacité ne suffit pas (en cybersécurité)

| Situation | Conséquence |
|-----------|-------------|
| A seul | Manipulation possible, mais sans effet |
| B seul | Accès aux données, mais aucune action |
| C seul | Erreur possible, mais pas d'adversaire ni de cible sensible |
| A + C | Sabotage possible (attaquant + action) |
| A + B | Fuite d'information passive |
| B + C | Erreur interne coûteuse |
| **A + B + C** | **Prise de contrôle active : l'attaquant accède aux données sensibles ET peut les exfiltrer** |

Un agent qui n'a que la capacité C (agir) mais sans entrées non fiables (A) ni accès sensible (B) peut bugger — mais il n'y a ni attaquant pour l'exploiter, ni cible de valeur à atteindre.

### Ce que la règle ne couvre pas

La Rule of Two est une règle de **cybersécurité**, pas de **sûreté de fonctionnement**.

Elle ne protège pas contre :
- les suppressions accidentelles de données,
- les envois de mauvais emails par hallucination,
- les décisions absurdes mais exécutées.

Ces risques relèvent de l'ingénierie classique : tests, validation, supervision humaine, rollback.

### Une position plus stricte est légitime

Pour les systèmes critiques (santé, finance, infrastructure), une approche plus conservatrice peut s'imposer : aucune action autonome sans validation humaine, quelle que soit la combinaison de capacités.

La Rule of Two est un compromis pragmatique pour les systèmes industriels déjà déployés, où l'autonomie partielle est un choix économique assumé.

## À retenir

- Les agents IA sont puissants, mais manipulables.
- Les attaques par prompt injection sont aujourd'hui inévitables.
- Ne jamais combiner A + B + C sans supervision humaine.
- Concevoir l'architecture avant de chercher la perfection du modèle.
- **Distinguer risque d'erreur (ingénierie) et risque d'exploitation (sécurité)** : la Rule of Two traite le second, pas le premier.
- Pour les systèmes critiques, une approche plus stricte reste légitime.


## Sources

- Simon Willison, "New prompt injection papers", simonwillison.net, novembre 2025
