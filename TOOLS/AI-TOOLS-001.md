---
id: AI-TOOLS-001
type: tools
title: "Les Claws : agents IA autonomes auto-hébergés"
version: 1.0
status: draft
created: 2026-02-21
updated: 2026-02-21
---

# Les Claws : agents IA autonomes auto-hébergés

## Résumé

Les Claws représentent une nouvelle catégorie d'agents IA qui dépasse le simple chatbot conversationnel. Là où un agent classique répond à une requête ponctuelle, un Claw agit dans la durée : il s'exécute localement, gère des processus planifiés, conserve une mémoire persistante et interagit directement avec le système d'exploitation, le réseau et les objets connectés. OpenClaw, projet open source lancé fin 2025, incarne cette évolution vers des agents véritablement autonomes et auto-hébergés.

## Présentation générale

Un Claw est un agent d'intelligence artificielle open source et auto-hébergé qui s'exécute localement sur un ordinateur ou un serveur pour automatiser des tâches réelles. Il s'intègre à des messageries comme WhatsApp, Telegram, Slack ou Discord, et utilise des modèles d'IA externes (Claude, GPT, modèles locaux) pour interpréter des instructions en langage naturel et agir en conséquence.

La différence fondamentale avec un assistant conversationnel classique tient en une phrase : un agent pense, un Claw agit dans la durée.

## Historique d'OpenClaw

### Origines

OpenClaw a été développé par l'Autrichien Peter Steinberger, qualifié de "vibe coder". Le projet dérive de Clawd (devenu Molty), un assistant virtuel inspiré du chatbot Claude d'Anthropic. Publié initialement en novembre 2025 sous le nom Clawdbot sur GitHub, il visait à créer un agent IA local exécutant des tâches réelles via messageries.

### Croissance virale

Les 24-26 janvier 2026, après un lancement public élargi, le projet explose : 60 000 étoiles GitHub en trois jours, puis 100 000 à 140 000 en deux mois, aidé par Moltbook (réseau social pour agents IA de Matt Schlicht). Le projet fut renommé Moltbot (27 janvier) puis OpenClaw (30 janvier) suite aux plaintes d'Anthropic sur la marque. Il a séduit les développeurs en Silicon Valley et en Chine.

### Évolution récente

Le 14 février 2026, Steinberger a rejoint OpenAI. Le projet est passé sous une fondation open source soutenue par Sam Altman, restant libre tout en gagnant en structure.

## Fonctionnalités clés

### Accès multicanal

Les Claws se connectent à WhatsApp, Telegram, Discord, Slack, iMessage ou Signal pour recevoir des instructions en langage naturel et envoyer des réponses ou alertes. Ils supportent les médias (images, audio, documents) et permettent un routage multi-agents pour isoler sessions ou espaces de travail.

### Automatisation système et shell

Un Claw exécute des commandes shell, gère des fichiers, lance des scripts PowerShell ou Python, surveille des répertoires et déclenche des tâches planifiées (backups, vérifications quotidiennes, maintenance système).

### Contrôle navigateur avancé

Via le protocole CDP Chrome, un Claw pilote la navigation web : snapshots intelligents d'éléments sans sélecteurs CSS, remplissage de formulaires, scraping, captures d'écran ou export PDF, et actions complexes (clics, glisser-déposer) dans un environnement isolé.

### Skills et mémoire

Plus de 100 compétences communautaires sont disponibles via ClawdHub : domotique, intégration d'APIs, outils de productivité. Le système génère automatiquement de nouvelles skills. La mémoire conversationnelle est stockée en Markdown pour un contexte long-terme, et les modèles d'IA sont interchangeables.

## Les dix principes fondamentaux des Claws

### 1. Orchestration persistante

Un agent classique répond à une requête. Un Claw gère des processus longs, planifiés, multi-étapes, avec un état conservé dans le temps.

### 2. Scheduling natif

L'exécution peut être déclenchée par des horaires, des événements ou des changements d'état. On passe du modèle "prompt-réponse" à un système réactif permanent.

### 3. Mémoire structurée

Au-delà du simple contexte textuel : stockage d'état, logs, artefacts intermédiaires, mémoire durable versionnée.

### 4. Toolchain systémique

Les outils ne sont plus des appels ponctuels. Ils forment un écosystème coordonné : APIs, système de fichiers, réseau, containers, services locaux.

### 5. Isolation par défaut

Exécution en containers ou sandbox. Une architecture sécurisée d'agent, pas un simple wrapper autour d'un LLM.

### 6. Skills as Code

La configuration devient transformation du code. Un skill modifie le système lui-même. On passe des fichiers YAML à une méta-programmation pilotée par IA.

### 7. Forkabilité maximale

Le dépôt devient un générateur d'agents personnalisés. On ne configure pas, on forke et spécialise. Un paradigme plus proche de Git que d'un SaaS.

### 8. Agent auto-modifiant

Capacité à éditer son propre code, installer des capacités, ajuster son orchestration. Une forme d'évolution contrôlée.

### 9. Infrastructure locale programmable

Connexion directe au réseau domestique, aux objets connectés, aux machines physiques. On dépasse le cloud-agent pour aller vers un agent incarné.

### 10. Stack multi-couche

LLM, puis Agent, puis Claw. Le Claw ajoute persistance, orchestration, gouvernance et gestion d'état. C'est une couche d'exécution durable, pas seulement une couche d'intelligence.

## Avantages et risques

### Avantages

- Contrôle total des données sans dépendance aux clouds tiers
- Automatisation puissante via chat pour les développeurs et professionnels IT
- Flexibilité maximale grâce au modèle open source et forkable
- Écosystème de skills communautaires en croissance rapide
- Modèles d'IA interchangeables selon les besoins

### Risques

- L'accès système profond pose des risques de sécurité significatifs
- Alertes signalées sur des malwares via skills malveillantes dans l'écosystème communautaire
- Nécessite une expertise technique pour une utilisation sécurisée
- Débats en cours sur la cybersécurité et la gouvernance du projet

## À retenir

- Les Claws représentent une évolution majeure : des agents qui agissent dans la durée plutôt que de simplement répondre à des requêtes.
- OpenClaw incarne ce nouveau paradigme avec une croissance fulgurante (100 000+ étoiles GitHub en deux mois).
- L'architecture repose sur dix principes fondamentaux : persistance, scheduling, mémoire structurée, isolation, auto-modification.
- Le modèle "Skills as Code" et la forkabilité maximale rapprochent l'écosystème d'une logique Git plutôt que SaaS.
- Les risques de sécurité liés à l'accès système profond restent un sujet de préoccupation majeur.

## Sources

- [Documentation OpenClaw](https://docs.openclaw.ai)
- [Dépôt GitHub OpenClaw](https://github.com/openclaw/openclaw)
- [ClawHub - marketplace de skills communautaires](https://clawhub.ai)
