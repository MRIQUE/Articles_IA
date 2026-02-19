---
id: AI-ACTOR-004
type: actor
title: "Simon Willison, prototypeur compulsif et vigie des LLM"
version: 1.0
status: draft
created: 2026-02-19
updated: 2026-02-19
---

# Simon Willison, prototypeur compulsif et vigie des LLM

## Résumé

Simon Willison est un développeur britannique, co-créateur du framework Django et créateur de Datasette. Depuis 2022, il s'est imposé comme l'un des observateurs les plus influents de l'écosystème des grands modèles de langage. Son blog, actif depuis 2002, est devenu une référence pour quiconque veut comprendre les capacités réelles, les limites et les risques des LLM. Ni évangéliste béat ni technophobe, il incarne une posture rare : celle du praticien enthousiaste qui documente ses expérimentations tout en alertant sur les dérives systémiques. Il se définit lui-même comme un "compulsive prototyper".

## Biographie

Simon Willison a commencé à bloguer sur le développement web en 2002. En 2005, alors journaliste développeur au Lawrence Journal-World (Kansas), il co-crée avec Adrian Holovaty le framework web Django, qui deviendra l'un des piliers de l'écosystème Python.

En 2010, il co-fonde Lanyrd, une plateforme de découverte de conférences, financée par Y Combinator. L'entreprise est rachetée par Eventbrite en 2013, où il occupe ensuite le poste de directeur technique.

Depuis 2017, il travaille en indépendant sur des projets open source, principalement autour de Datasette, un outil d'exploration et de publication de données basé sur SQLite. Il est membre du conseil d'administration de la Python Software Foundation et GitHub Star.

Il réside en Californie avec sa famille. Une partie de son travail sur Datasette Cloud est sponsorisée par Fly.io. Il reçoit régulièrement des accès anticipés aux nouveaux modèles d'OpenAI, Anthropic, Google et Mistral, souvent sous embargo, mais affirme n'accepter aucune compensation éditoriale.

## Thèses et positions

### Le vibe coding : programmer par l'intention

Simon Willison est l'un des promoteurs du "vibe coding", une approche où le développeur guide un agent IA par des instructions en langage naturel plutôt que par l'écriture directe de code. Il crée désormais des outils complets sur son téléphone pendant ses promenades, en dictant ses intentions à des agents comme Claude Code. Il va jusqu'à faire tourner six agents en parallèle dans six terminaux différents, une pratique qu'il qualifie lui-même de "delirium d'agent parallèle".

Cette approche repose sur une conviction : le coût du code ayant drastiquement chuté, il est désormais plus efficace de tenter des expérimentations pendant deux jours que de passer des mois en phase de conception.

### La dette cognitive : le risque majeur du code généré

Malgré son enthousiasme, Willison lance des alertes claires. Sa principale inquiétude porte sur la "dette cognitive" : l'utilisation excessive de code généré par IA sans revue approfondie fait perdre au développeur son modèle mental du projet. Sans cette compréhension intime du système, les décisions futures deviennent plus difficiles et plus risquées. Le développeur devient étranger à son propre code.

### Le Deep Blue : l'angoisse existentielle des développeurs

Il a contribué à forger le terme "Deep Blue" pour décrire le malaise psychologique des développeurs face à la puissance des LLM : un mélange d'ennui, d'effroi existentiel et de remise en question professionnelle. Ce sentiment survient quand un modèle accomplit en quelques secondes ce qui aurait demandé des heures de travail humain.

### Le prompt injection : une vulnérabilité structurelle

Willison est l'un des experts les plus documentés sur le prompt injection, cette technique qui permet à un attaquant d'injecter des instructions malveillantes dans le contexte d'un LLM. Il documente inlassablement les nouvelles variantes de cette attaque et considère qu'elle reste un problème fondamentalement non résolu.

### La fin du persona prompting

Il estime qu'il faut cesser de demander à l'IA d'"agir comme un expert". Cette approche serait moins efficace que de fournir des critères de succès clairs et de préciser l'audience cible. Le modèle n'a pas besoin d'un rôle à jouer, il a besoin de contraintes explicites.

### Vérifiabilité plutôt que confiance

Pour Willison, si une tâche est vérifiable (par des tests unitaires, par exemple), elle est optimisable par l'IA. La compétence clé du développeur moderne n'est plus de mémoriser la syntaxe, mais de savoir vérifier et valider le code produit. Il crée des dépôts de "recherche" où des agents mènent des expériences de manière autonome, guidés par des suites de tests.

### Standards ouverts contre verrouillage

Il milite pour des protocoles ouverts qui empêchent le verrouillage par les grands laboratoires : le MCP (Model Context Protocol) d'Anthropic pour connecter les modèles à des sources externes, et l'API Open Responses pour standardiser les formats de réponse entre fournisseurs.

### La prolifération du "slop"

Il dénonce la pollution du web par le "slop", ces contenus générés par IA de faible qualité qui envahissent les communications et les résultats de recherche. Il cite en exemple les emails automatisés envoyés à des figures techniques respectées, manifestement produits sans supervision humaine.

## Signatures et marottes

### Le benchmark du pélican à bicyclette

Simon Willison utilise une méthode récurrente et personnelle pour évaluer les capacités des nouveaux modèles : leur demander de générer un SVG représentant un pélican brun de Californie faisant du vélo. Ce test, devenu une signature de son blog, révèle les capacités de raisonnement spatial, de suivi d'instructions complexes et de rendu technique. C'est pour lui l'épreuve ultime de créativité non-textuelle.

### La sécurité des agents : les drapeaux dangereux

Il alerte régulièrement sur les risques des modes permissifs des agents de code. Les commandes comme `--dangerously-skip-permissions` (Claude Code) ou `--yolo` (Codex) désactivent les garde-fous et peuvent conduire à des accidents graves, comme un agent tentant d'exécuter `rm -rf ~/` sur le répertoire personnel de l'utilisateur.

### La nomenclature absurde des modèles

Il se moque régulièrement de l'incapacité des laboratoires d'IA à nommer leurs produits de manière cohérente. Les appellations comme "GPT-5.2-Codex-Max" ou les versionnements erratiques sont pour lui le symptôme d'une industrie qui avance plus vite que sa capacité à communiquer clairement.

## Outils et projets

- **Datasette** : outil open source pour explorer et publier des données, construit autour de SQLite
- **LLM** : bibliothèque Python et outil CLI permettant d'interagir avec n'importe quel modèle (OpenAI, Anthropic, Google, modèles locaux) de manière unifiée
- **Showboat et Rodney** : outils permettant aux agents IA de produire des démonstrations visuelles de leurs créations

## Sources

- Blog personnel : https://simonwillison.net/
- Page "About" : https://simonwillison.net/about/
- Newsletter : https://simonw.substack.com/
- Profil GitHub : https://github.com/simonw
- Mastodon : https://fedi.simonwillison.net/@simon
- Bluesky : https://bsky.app/profile/simonwillison.net
