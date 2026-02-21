

	 
## About me

Here's my most recent conference bio:

> Simon Willison is the creator of [Datasette](https://datasette.io/), an open source tool for exploring and publishing data. He currently works full-time building open source tools for data journalism, built around Datasette and SQLite.
> 
> Prior to becoming an independent open source developer, Simon was an engineering director at Eventbrite. Simon joined Eventbrite through their acquisition of Lanyrd, a Y Combinator funded company he co-founded in 2010.
> 
> He is a co-creator of the Django Web Framework, and has been blogging about web development and programming since 2002 at [simonwillison.net](https://simonwillison.net/)

## Subscribe [#](https://simonwillison.net/about/#subscribe)

You can subscribe to my blog via email newsletter, using Atom feeds or by following me on Mastodon or Bluesky or Twitter.

### Free weekly-ish newsletter [#](https://simonwillison.net/about/#newsletter)

I send out [a newsletter version](https://simonw.substack.com/) of this blog once every week or so. You can subscribe to that here:

### Paid monthly newsletter [#](https://simonwillison.net/about/#monthly)

I write a _lot_ of stuff. If you like you can **pay me to send you less**. At the end of every month I send out a much shorter newsletter to anyone who [sponsors me for $10 or more on GitHub](https://github.com/sponsors/simonw). It's intended to be a ten minute read that catches you up on the most important developments from the past month in LLMs and my other projects and research.

### Mastodon and Bluesky and Twitter [#](https://simonwillison.net/about/#social)

- [@simon@simonwillison.net](https://fedi.simonwillison.net/@simon) on Mastodon
- [simonwillison.net](https://bsky.app/profile/simonwillison.net) on Bluesky
- [@simonw](https://twitter.com/simonw) on Twitter

### Atom feeds [#](https://simonwillison.net/about/#atom)

The main feed for my site combines my blog entries, my blogmarks and my collected quotations:

`https://simonwillison.net/atom/everything/`

If you just want my longer form blog entries you can subscribe to this feed instead:

`https://simonwillison.net/atom/entries/`

Or this feed for just my links (excluding quotes):

`https://simonwillison.net/atom/links/`

Every [tag](https://simonwillison.net/tags/) on my blog has its own feed. You can subscribe to those by adding `.atom` to the URL to the tag page.

For example, to subscribe to just my content about Datasette, use the following:

`https://simonwillison.net/tags/datasette.atom`

### Disclosures [#](https://simonwillison.net/about/#disclosures)

I do not receive any compensation for writing about specific topics on this blog - no sponsored content! I plan to continue this policy. If I ever change this I will disclose that both here and in the post itself.

Part of work on [Datasette Cloud](https://www.datasette.cloud/) is sponsored by [Fly.io](https://fly.io/). I have a generous set of [GitHub Sponsors](https://github.com/sponsors/simonw) who support my work on Datasette and other open source projects.

I am currently a member of the board of directors [for the Python Software Foundation](https://www.python.org/psf/board/).

I am a [GitHub Star](https://stars.github.com/profiles/simonw/) (an unpaid position). GitHub paid me as a participant of their [GitHub Accelerator](https://github.blog/news-insights/company-news/github-accelerator-our-first-cohort-and-whats-next/) program in 2023.

Mozilla supported my work as part of [their MIECO program](https://web.archive.org/web/20240917063820/https://future.mozilla.org/mieco2023/) (Internet Ecosystem program) in 2023-2024.

I have not accepted payments from LLM vendors, but I am frequently invited to preview new LLM products and features from organizations that include OpenAI, Anthropic, Gemini and Mistral, often under NDA or subject to an embargo. This often also includes free API credits and invitations to events.

_One exception: OpenAI paid my for my time when I attended a GPT-5 preview at their office which was [used in a video](https://simonwillison.net/2025/Aug/7/previewing-gpt-5/). They did not ask for any editorial insight or control over what I wrote after that event, aside from keeping to their embargo._

I run ads on my blog using [EthicalAds](https://www.ethicalads.io/). I also earn money from Twitter's [Creator Revenue Sharing](https://help.x.com/en/using-x/creator-revenue-sharing) program, and try not to let that incentivize me to post engagement bait!

I provide ad-hoc consulting and training services to a number of different companies and organizations. If any of those represent a conflict of interest with my writing here I will disclose that in the relevant post.
 

L'archive des publications de **Simon Willison** brosse le portrait d'un expert en IA à la fois extrêmement enthousiaste par les gains de productivité et profondément vigilant quant aux dérives structurelles du métier de développeur.

Voici une synthèse thématique de ses positions actuelles :

---

## 🚀 Enthousiasmes : L'ère du "Vibe Coding"

Simon est fasciné par le franchissement d'un "seuil d'incroyance" avec les modèles récents (Claude 4.5, GPT-5.1, Gemini 3).

- **Vibe Coding :** Il promeut une approche où l'on code par l'intention plutôt que par la syntaxe. Il crée des outils complexes (comme des visualiseurs de fils Bluesky ou des applications de cuisine) directement sur son téléphone lors de ses promenades.
    
- **Agents de codage :** Il utilise massivement **Claude Code** et **Codex CLI**, allant jusqu'à faire tourner six agents en parallèle dans six terminaux différents ("delirium d'agent parallèle").
    
- **Prototypage radical :** Selon lui, le coût du code ayant chuté, il est désormais plus efficace de "tenter des trucs" pendant deux jours que de passer des mois en phase de conception.
    

## ⚠️ Alertes et Inquiétudes

Malgré son adoption rapide, il lance des avertissements clairs sur les risques systémiques.

- **Dette Cognitive :** C’est l’une de ses plus grandes craintes. L’utilisation excessive de code généré par IA sans revue approfondie fait perdre au développeur son "modèle mental" du projet, rendant les décisions futures plus difficiles et risquées.
    
- **Le "Deep Blue" :** Il a co-inventé ce terme pour décrire l’ennui psychologique et l’effroi existentiel des développeurs face à la puissance des LLM.
    
- **Sécurité des agents :** Il alerte sur les dangers des commandes comme `--dangerously-skip-permissions` (Claude Code) ou `--yolo` (Codex), citant des exemples où un agent peut accidentellement tenter de supprimer tout un répertoire personnel (`rm -rf ~/`).
    

## 🧠 Convictions Techniques

- **La fin du "Persona Prompting" :** Il estime qu'il faut arrêter de dire à l'IA "agis comme un expert" et plutôt lui donner des critères de succès clairs et lui préciser l'audience cible.
    
- **Vérifiabilité vs Compétence :** Il adhère à l'idée que si une tâche est vérifiable (par des tests unitaires), elle est optimisable par l'IA. Il crée des repos de "recherche" où des agents mènent des expériences de manière autonome.
    
- **Standards Ouverts :** Il milite pour des standards comme le **MCP** (Model Context Protocol) ou l'API **Open Responses** pour uniformiser l'interaction avec les modèles.
    

## 🧐 Observations sur l'Industrie

- **Nomenclature confuse :** Il se moque régulièrement des noms de modèles absurdes (comme "GPT-5.2-Codex-Max") et de l'incapacité des laboratoires d'IA à nommer leurs produits de manière cohérente.
    
- **Éducation :** Il s'inquiète du fait que nous ne sachions pas encore comment mesurer l'impact réel des changements pédagogiques nécessaires maintenant que les tests et essais classiques sont obsolètes.
    

---

### Le Benchmark du Pélican

Simon utilise une méthode unique et récurrente pour tester les capacités de raisonnement spatial et de rendu des modèles : leur demander de générer un **SVG d'un pélican brun de Californie faisant du vélo**.

_C'est pour lui le test ultime de "suivi d'instruction" et de créativité non-textuelle._

**Souhaitez-vous que je détaille ses notes spécifiques sur un modèle en particulier (comme Claude 4.5 ou Gemini 3 Deep Think) ou que j'approfondisse ses "astuces" de test avec `uv` et `pytest` ?**


======
Le blog de **Simon Willison** (simonwillison.net) est une référence majeure dans l'écosystème de l'intelligence artificielle et du développement open source. Voici une synthèse de ses préoccupations et sujets phares, basée sur ses publications récentes (fin 2025 - début 2026) :

### 1. L'évolution fulgurante du "Coding" par IA

Simon documente quotidiennement comment les LLM transforment le métier de développeur. Ses concepts clés incluent :

- **Vibe Coding :** L'idée de programmer par l'intention et la "vibration" plutôt que par la syntaxe. Il crée désormais des outils complets sur son téléphone en marchant, en guidant des agents comme **Claude Code**.
    
- **Agents Autonomes :** Il explore massivement l'usage d'agents capables de lire, écrire et exécuter du code (Claude Code, OpenAI Codex CLI, Rodney). Il expérimente le "codage en parallèle" avec jusqu'à six agents travaillant simultanément.
    
- **Vérifiabilité vs Confiance :** Il soutient que puisque l'IA peut désormais écrire du code de haute qualité, la compétence clé devient la capacité à **vérifier** et tester ce code plutôt qu'à le mémoriser.
    

### 2. Éthique et Risques de l'IA

Bien qu'enthousiaste, il est l'un des observateurs les plus lucides sur les dérives :

- **Dette Cognitive :** Il s'inquiète du fait que confier trop de code à l'IA sans revue rigoureuse fasse perdre au développeur la compréhension profonde de ses propres systèmes.
    
- **Prompt Injection :** C'est l'un des plus grands experts sur cette vulnérabilité. Il documente sans cesse comment les attaquants peuvent "hacker" les instructions des LLM.
    
- **IA "Slop" :** Il critique la prolifération de contenus générés par IA de faible qualité (le "slop") qui pollue le web et les communications (ex: les emails automatisés envoyés à des figures comme Rob Pike).
    
- **Deep Blue :** Un terme qu'il a aidé à forger pour décrire l'angoisse existentielle des développeurs face à la puissance des modèles.
    

### 3. Projets Open Source et Outils (Datasette)

Simon est le créateur de **Datasette**, un outil pour explorer et publier des données :

- **Écosystème SQLite :** Il promeut l'usage de SQLite comme format de base de données universel et puissant.
    
- **LLM (outil CLI) :** Il maintient une bibliothèque Python et un outil en ligne de commande (`llm`) qui permet d'interagir avec n'importe quel modèle (OpenAI, Anthropic, Google, modèles locaux) de manière standardisée.
    
- **Showboat & Rodney :** Des outils récents pour permettre aux agents d'IA de faire des démonstrations visuelles de ce qu'ils ont construit.
    

### 4. Standards et Interopérabilité

Il milite pour des protocoles ouverts qui empêchent le verrouillage par les grands laboratoires :

- **MCP (Model Context Protocol) :** Il suit de très près ce standard d'Anthropic qui permet aux modèles d'IA de se connecter plus facilement à des sources de données et des outils externes.
    
- **Open Responses API :** Il soutient la standardisation des formats de réponse des modèles pour faciliter le passage de l'un à l'autre.
    

### 5. Le Benchmark du "Pélican à bicyclette"

Devenu une signature de son blog, il utilise une épreuve spécifique pour comparer les modèles : demander un **SVG d'un pélican brun de Californie faisant du vélo**. Ce test simple révèle les capacités de raisonnement spatial, de respect des instructions complexes et de rendu technique des nouveaux modèles.

### En résumé

Simon Willison se définit comme un **"compulsive prototyper"**. Son blog est un laboratoire vivant où il teste chaque nouvelle API en quelques heures, partage ses "TIL" (Things I Learned) et réfléchit à la manière dont l'humanité peut garder le contrôle sur une technologie qui avance plus vite que nos capacités d'adaptation.