

# La Fin de l'Application : Vers l'Ère du Logiciel Éphémère et Sur-Mesure

_Article de prospective — Février 2026_

---

Il y a quelques jours, un entrepreneur de la Silicon Valley publiait un post qui, sous des dehors anecdotiques, révèle peut-être l'une des ruptures les plus profondes de l'histoire du logiciel. En une heure, il avait demandé à un agent d'IA de construire un tableau de bord personnalisé pour suivre une expérience cardio très précise — faire baisser sa fréquence cardiaque au repos de 50 à 45 bpm en huit semaines, en combinant Zone 2 et HIIT. L'agent avait rétro-ingénierié une API propriétaire, traité les données brutes, déboggué des erreurs de conversion métrique, et livré une interface web fonctionnelle. Une heure. Et pourtant, l'auteur du post n'était pas impressionné par l'heure. Il était intrigué par ce que représente cette heure : un artefact logiciel unique, généré à la demande, pour un besoin qui n'existera peut-être plus dans neuf semaines.

Ce moment mérite qu'on s'y attarde. Il annonce la fin d'un paradigme vieux de quarante ans.

---

## L'App Store comme fossile de l'ère industrielle du logiciel

L'économie des applications telle que nous la connaissons — App Store, Google Play, catalogues SaaS — repose sur une logique industrielle classique : des ingénieurs identifient un besoin générique, produisent une solution standardisée, et la distribuent à grande échelle. Ce modèle a généré des fortunes colossales et structuré notre rapport au numérique depuis l'iPhone de 2007. Mais il repose sur une prémisse implicite : le coût de production d'un logiciel est trop élevé pour être personnalisé à l'individu.

Cette prémisse est en train de s'effondrer.

Marc Andreessen, cofondateur de a16z et auteur du célèbre manifeste _Why Software Is Eating the World_, a récemment reformulé sa vision : dans les prochaines années, chaque personne pourrait disposer d'un "staff" d'agents IA capables de produire, à la volée, les outils dont elle a besoin. L'application n'est plus un produit que l'on choisit dans un catalogue ; elle devient une réponse contextuelle à une intention exprimée.

Le post en question illustre cela avec une acuité rare. Il n'existe pas — et ne devrait pas exister — d'application "Cardio Experiment Tracker" sur l'App Store. Ce serait absurde. Le besoin est trop spécifique, trop temporaire, trop personnel. Et pourtant, ce besoin est réel, légitime, et méritait un outil. Dans l'ancien monde, il n'aurait pas eu d'outil. Dans le nouveau, il l'a eu en une heure.

---

## Le logiciel devient un acte de langage

Le philosophe John Searle distinguait les actes de langage qui _décrivent_ le monde de ceux qui le _transforment_. Dire "la fenêtre est ouverte" est une description. Dire "je vous déclare mariés" est une transformation — la parole crée la réalité.

Nous entrons dans une ère où l'intention exprimée en langage naturel _génère_ directement l'outil logiciel correspondant. Le logiciel cesse d'être une infrastructure que l'on installe, configure et maintient. Il devient un acte de langage à part entière.

Andrej Karpathy, ancien directeur de l'IA chez Tesla et figure intellectuelle centrale de l'écosystème IA, a popularisé le terme _vibe coding_ pour décrire cette pratique : l'humain formule une intention, une ambiance, un objectif — et l'agent traduit cela en code fonctionnel. La compétence clé n'est plus de savoir programmer, mais de savoir _spécifier_ avec précision ce que l'on veut. C'est un changement anthropologique autant que technique.

Sam Altman, PDG d'OpenAI, va plus loin en affirmant que nous approchons du moment où "un agent IA pourrait faire le travail d'une startup entière". Ce n'est pas une hyperbole marketing — c'est une reformulation de la même rupture : la chute du coût marginal de production du logiciel vers zéro.

---

## Capteurs, actionneurs et le problème de l'infrastructure agent-native

Mais l'auteur du post pointe une friction cruciale qui ralentit cette transformation : 99% des services et appareils connectés ne sont toujours pas conçus pour être utilisés par des agents. Ils maintiennent des interfaces graphiques pensées pour des humains, des documentations HTML dont la structure suppose que c'est un être humain qui va la lire, cliquer, naviguer.

Son tapis de course Woodway est un capteur. Il transforme un état physique — effort, fréquence cardiaque, allure — en donnée numérique. Mais il expose cette donnée derrière un frontend applicatif conçu pour un utilisateur humain, pas pour un agent. L'agent a dû _rétro-ingénierer_ l'API cloud pour accéder aux données brutes. C'est un symptôme d'une inadéquation profonde entre l'infrastructure existante et l'usage émergent.

Kevin Kelly, cofondateur de _Wired_ et penseur de la technologie à long terme, décrit depuis des années la convergence vers ce qu'il appelle le "flux" : les objets physiques deviennent des nœuds d'un réseau continu de données et d'actions. Mais le flux suppose des interfaces standardisées, ouvertes, lisibles par des machines. Nous n'y sommes pas encore.

La vision prospective que dessine ce post est celle d'une infrastructure radicalement différente : chaque service, chaque appareil, chaque source de données expose une API ou une CLI _agent-native_ — structurée non pour la lisibilité humaine, mais pour l'orchestration automatique. Le tapis de course ne vous affiche pas un graphique ; il répond à des requêtes structurées de votre agent. Votre agenda n'est pas une interface à cliquer ; c'est un actionneur que votre agent pilote directement.

---

## L'orchestration comme nouvelle couche de valeur

Dans ce modèle, la valeur se déplace. Elle ne réside plus dans l'application elle-même — qui devient éphémère, générée à la demande, jetée après usage — mais dans deux couches distinctes :

**La couche des données** : capteurs, bases de connaissances personnelles, historiques d'usage, contexte accumulé. Celui qui contrôle le contexte personnel — santé, finances, habitudes, préférences — contrôle la pertinence de ce que l'agent peut produire.

**La couche d'orchestration** : la capacité de l'agent à composer, en temps réel, des services hétérogènes en une solution cohérente. C'est le "glue LLM" que décrit le post — l'intelligence de liaison entre des capteurs et des actionneurs.

Jensen Huang, PDG de Nvidia, a formulé cela à sa manière lors du CES 2025 : "Les agents physiques et logiciels vont transformer chaque industrie. L'infrastructure que nous construisons n'est pas pour des applications — elle est pour des orchestrateurs." C'est une déclaration stratégique autant qu'une observation technique. Nvidia ne vend pas des GPU pour faire tourner des apps. Il vend l'infrastructure sur laquelle des agents font tourner des apps pour vous.

---

## De l'heure à la minute : ce qui manque encore

L'auteur du post formule une question précise et exigeante : ce qui a pris une heure devrait prendre une minute. Qu'est-ce qui manque pour y arriver ?

Il identifie lui-même les pièces manquantes : un contexte personnel riche et déjà disponible (l'agent vous connaît), des bibliothèques de compétences référençables (l'agent sait déjà comment interroger telle catégorie d'API), et une infrastructure de services réellement agent-native.

On peut y ajouter une dimension que le post n'aborde qu'implicitement : la **confiance et la gouvernance**. Un agent qui orchestre des données de santé, accède à des APIs propriétaires, génère et exécute du code en temps réel — cet agent opère dans un espace où les questions de sécurité, de propriété des données et de responsabilité deviennent critiques. Yuval Noah Harari, dans _Homo Deus_, anticipait le risque d'une humanité déléguant ses décisions à des algorithmes sans en comprendre les mécanismes. La version optimiste de cette transformation suppose une transparence et une contrôlabilité que les architectures actuelles d'agents ne garantissent pas encore.

---

## Implications stratégiques : qui gagne, qui perd

Pour les entreprises, cette trajectoire a des implications considérables et peu confortables.

Les éditeurs de logiciels verticaux — ceux qui ont bâti leur modèle sur un produit SaaS standardisé répondant à un besoin métier précis — se retrouvent dans la position des fabricants de cartes routières papier face à Google Maps. Leur valeur n'est pas dans l'interface, ni même dans la logique applicative. Elle est dans les données qu'ils ont accumulées et dans les intégrations qu'ils maintiennent. Ceux qui ne l'auront pas compris à temps produiront des artefacts que des agents remplaceront en quelques secondes.

Les entreprises qui prospèrent dans ce paradigme seront celles qui auront su exposer leurs services en mode agent-native — des API claires, documentées pour des machines, avec des modèles de données stables et des capacités d'action réelles. Ce sont elles qui deviendront les "actionneurs" dans l'écosystème que décrit le post.

Pour les DSI et architectes d'entreprise, la question n'est plus "quelle application choisit-on ?" mais "comment notre stack expose-t-elle ses capacités à des agents externes ou internes ?" C'est un renversement complet de la logique de sélection et d'intégration logicielle.

---

## Conclusion : le logiciel comme service de moment

Il y a quelque chose de presque poétique dans l'image du tableau de bord cardio généré en une heure pour une expérience de huit semaines. Dans neuf semaines, il n'existera plus. Il n'avait pas vocation à exister au-delà de l'expérience qu'il servait. C'est peut-être cela, la définition du logiciel de demain : non plus un produit que l'on possède, mais un **service de moment** — une réponse précise à une intention précise, dans un contexte précis, qui disparaît quand l'intention est satisfaite.

Nassim Taleb, dans _Antifragile_, défend l'idée que les systèmes les plus robustes sont ceux qui s'adaptent à leur environnement plutôt que ceux qui cherchent à le standardiser. Le logiciel éphémère, sur-mesure, généré à la demande, est peut-être la forme la plus antifragile que le code ait jamais prise.

Nous n'y sommes pas encore. L'infrastructure agent-native est en retard. La plupart des services pensent encore en termes de frontends humains. Les questions de gouvernance et de sécurité restent ouvertes. Mais la direction est claire, et elle est irréversible.

L'App Store n'est pas mort. Il est en train de devenir anachronique.

---

_La prochaine fois que vous téléchargez une application pour répondre à un besoin très spécifique, demandez-vous : est-ce que j'aurais pu simplement demander à mon agent de me construire exactement ce dont j'ai besoin ? Dans quelques années, la réponse sera presque toujours oui._