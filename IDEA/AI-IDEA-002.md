---
id: AI-IDEA-002
type: idea
title: "Vers les logiciels éphémères et sur-mesure : la fin du paradigme applicatif"
version: 1.0
status: draft
created: 2026-02-21
updated: 2026-02-21
---

# Vers les logiciels éphémères et sur-mesure : la fin du paradigme applicatif

## Résumé

L'économie des applications telle que nous la connaissons repose sur une prémisse implicite : le coût de production d'un logiciel est trop élevé pour être personnalisé à l'individu. Cette prémisse est en train de s'effondrer. Les agents IA permettent désormais de générer des outils logiciels à la demande, pour des besoins trop spécifiques, trop temporaires ou trop personnels pour justifier une application standardisée. Le logiciel cesse d'être un produit que l'on choisit dans un catalogue pour devenir une réponse contextuelle à une intention exprimée. Cette transformation annonce la fin d'un paradigme vieux de quarante ans.

## L'App Store comme fossile de l'ère industrielle

L'économie des applications — App Store, Google Play, catalogues SaaS — repose sur une logique industrielle classique : des ingénieurs identifient un besoin générique, produisent une solution standardisée, et la distribuent à grande échelle. Ce modèle a généré des fortunes colossales et structuré notre rapport au numérique depuis l'iPhone de 2007.

Marc Andreessen, cofondateur de a16z, a récemment reformulé sa vision : dans les prochaines années, chaque personne pourrait disposer d'un "staff" d'agents IA capables de produire, à la volée, les outils dont elle a besoin. L'application n'est plus un produit que l'on choisit dans un catalogue ; elle devient une réponse contextuelle à une intention exprimée.

Prenons un exemple concret : un entrepreneur qui souhaite suivre une expérience cardio très précise — faire baisser sa fréquence cardiaque au repos de 50 à 45 bpm en huit semaines. Il n'existe pas — et ne devrait pas exister — d'application "Cardio Experiment Tracker" sur l'App Store. Ce serait absurde. Le besoin est trop spécifique, trop temporaire, trop personnel. Et pourtant, ce besoin est réel, légitime, et méritait un outil. Un agent IA peut le construire en une heure.

## Le logiciel devient un acte de langage

Le philosophe John Searle distinguait les actes de langage qui décrivent le monde de ceux qui le transforment. Dire "la fenêtre est ouverte" est une description. Dire "je vous déclare mariés" est une transformation — la parole crée la réalité.

Nous entrons dans une ère où l'intention exprimée en langage naturel génère directement l'outil logiciel correspondant. Le logiciel cesse d'être une infrastructure que l'on installe, configure et maintient. Il devient un acte de langage à part entière.

Andrej Karpathy, ancien directeur de l'IA chez Tesla, a popularisé le terme "vibe coding" pour décrire cette pratique : l'humain formule une intention, une ambiance, un objectif — et l'agent traduit cela en code fonctionnel. La compétence clé n'est plus de savoir programmer, mais de savoir spécifier avec précision ce que l'on veut. C'est un changement anthropologique autant que technique.

Sam Altman, PDG d'OpenAI, va plus loin en affirmant que nous approchons du moment où "un agent IA pourrait faire le travail d'une startup entière". Ce n'est pas une hyperbole marketing — c'est une reformulation de la même rupture : la chute du coût marginal de production du logiciel vers zéro.

## Le problème de l'infrastructure agent-native

Une friction cruciale ralentit cette transformation : 99% des services et appareils connectés ne sont toujours pas conçus pour être utilisés par des agents. Ils maintiennent des interfaces graphiques pensées pour des humains, des documentations HTML dont la structure suppose que c'est un être humain qui va la lire, cliquer, naviguer.

Kevin Kelly, cofondateur de Wired, décrit depuis des années la convergence vers ce qu'il appelle le "flux" : les objets physiques deviennent des noeuds d'un réseau continu de données et d'actions. Mais le flux suppose des interfaces standardisées, ouvertes, lisibles par des machines. Nous n'y sommes pas encore.

La vision prospective est celle d'une infrastructure radicalement différente : chaque service, chaque appareil, chaque source de données expose une API ou une CLI agent-native — structurée non pour la lisibilité humaine, mais pour l'orchestration automatique. Votre tapis de course ne vous affiche pas un graphique ; il répond à des requêtes structurées de votre agent. Votre agenda n'est pas une interface à cliquer ; c'est un actionneur que votre agent pilote directement.

## L'orchestration comme nouvelle couche de valeur

Dans ce modèle, la valeur se déplace. Elle ne réside plus dans l'application elle-même — qui devient éphémère, générée à la demande, jetée après usage — mais dans deux couches distinctes :

**La couche des données** : capteurs, bases de connaissances personnelles, historiques d'usage, contexte accumulé. Celui qui contrôle le contexte personnel — santé, finances, habitudes, préférences — contrôle la pertinence de ce que l'agent peut produire.

**La couche d'orchestration** : la capacité de l'agent à composer, en temps réel, des services hétérogènes en une solution cohérente. C'est le "glue LLM" — l'intelligence de liaison entre des capteurs et des actionneurs.

Jensen Huang, PDG de Nvidia, a formulé cela lors du CES 2025 : "Les agents physiques et logiciels vont transformer chaque industrie. L'infrastructure que nous construisons n'est pas pour des applications — elle est pour des orchestrateurs." Nvidia ne vend pas des GPU pour faire tourner des apps. Il vend l'infrastructure sur laquelle des agents font tourner des apps pour vous.

## Ce qui manque encore

Ce qui prend une heure aujourd'hui devrait prendre une minute demain. Qu'est-ce qui manque pour y arriver ?

Plusieurs pièces manquantes : un contexte personnel riche et déjà disponible (l'agent vous connaît), des bibliothèques de compétences référençables (l'agent sait déjà comment interroger telle catégorie d'API), et une infrastructure de services réellement agent-native.

Il faut y ajouter une dimension critique : la confiance et la gouvernance. Un agent qui orchestre des données de santé, accède à des APIs propriétaires, génère et exécute du code en temps réel — cet agent opère dans un espace où les questions de sécurité, de propriété des données et de responsabilité deviennent critiques. Yuval Noah Harari, dans Homo Deus, anticipait le risque d'une humanité déléguant ses décisions à des algorithmes sans en comprendre les mécanismes. La version optimiste de cette transformation suppose une transparence et une contrôlabilité que les architectures actuelles d'agents ne garantissent pas encore.

## Implications stratégiques

Pour les entreprises, cette trajectoire a des implications considérables.

Les éditeurs de logiciels verticaux — ceux qui ont bâti leur modèle sur un produit SaaS standardisé répondant à un besoin métier précis — se retrouvent dans la position des fabricants de cartes routières papier face à Google Maps. Leur valeur n'est pas dans l'interface, ni même dans la logique applicative. Elle est dans les données qu'ils ont accumulées et dans les intégrations qu'ils maintiennent.

Les entreprises qui prospèrent dans ce paradigme seront celles qui auront su exposer leurs services en mode agent-native — des API claires, documentées pour des machines, avec des modèles de données stables et des capacités d'action réelles.

Pour les DSI et architectes d'entreprise, la question n'est plus "quelle application choisit-on ?" mais "comment notre stack expose-t-elle ses capacités à des agents externes ou internes ?" C'est un renversement complet de la logique de sélection et d'intégration logicielle.

## À retenir

- Le coût de production d'un logiciel personnalisé s'effondre grâce aux agents IA, rendant obsolète le modèle de l'application standardisée.
- Le logiciel devient un "service de moment" : une réponse précise à une intention précise, qui disparaît quand l'intention est satisfaite.
- La valeur se déplace vers la couche des données personnelles et la couche d'orchestration, pas vers l'application elle-même.
- L'infrastructure actuelle est en retard : la plupart des services pensent encore en termes de frontends humains, pas d'APIs agent-native.
- Pour les entreprises, la question stratégique devient : comment exposer ses capacités à des agents, et non plus quelle application choisir.
- Les questions de gouvernance, sécurité et propriété des données restent des défis majeurs à résoudre.

## Sources

- [Marc Andreessen, "Beyond Chatbots: AI's Future"](https://podcasts.apple.com/us/podcast/beyond-chatbots-marc-andreessen-and-ben-horowitz-on/id842818711?i=1000734418965) — vision sur les agents IA comme "staff personnel"
- [Andrej Karpathy, post X sur le "vibe coding"](https://x.com/karpathy/status/1886192184808149383) — concept originel de février 2025
- [Sam Altman, "The Next $1B Startup Will Be a One-Person Company"](https://felloai.com/2025/09/sam-altman-other-ai-leaders-the-next-1b-startup-will-be-a-one-person-company/) — réflexions sur les agents capables de remplacer une startup
- [Jensen Huang, keynote CES 2025](https://blogs.nvidia.com/blog/ces-2025-jensen-huang/) — infrastructure pour orchestrateurs et "Agentic AI"
- [Kevin Kelly, "New Rules for the New Economy"](https://kk.org/newrules/newrules-8.html) — concept du "flux" et de l'infrastructure connectée
- [Yuval Noah Harari, "Homo Deus: After God and Man, Algorithms Will Make the Decisions"](https://www.ynharari.com/homo-deus-after-god-and-man-algorithms-will-make-the-decisions/) — sur la délégation algorithmique
- [John Searle, théorie des actes de langage](https://fr.wikipedia.org/wiki/Acte_de_langage) — distinction entre actes illocutoires et performatifs
- [Nassim Taleb, "Antifragile"](https://en.wikipedia.org/wiki/Antifragile_(book)) — sur l'adaptabilité des systèmes
