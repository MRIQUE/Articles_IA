---
id: AI-TOOLS-005
type: tools
title: "DSPy : programmer les LLMs au lieu de les prompter"
version: 1.0
status: draft
created: 2026-03-24
updated: 2026-03-24
---

# DSPy : programmer les LLMs au lieu de les prompter

## Resume

DSPy (Declarative Self-improving Python) est un framework open-source cree par Stanford qui remplace le prompt engineering manuel par de la programmation declarative. Au lieu d'ecrire et d'affiner des prompts fragiles, le developpeur definit des signatures (entrees/sorties attendues) et des modules : DSPy se charge de generer et d'optimiser les prompts automatiquement. Le framework fournit des primitives pour les patterns LLM avances (raisonnement en chaine, agents, RAG) et des optimiseurs qui ajustent les prompts en fonction de metriques. Les applications DSPy sont LLM-agnostiques et fonctionnent avec OpenAI, Anthropic Claude ou des modeles locaux sans modifier la logique applicative.

## Le probleme : le prompt hacking et la fragilite des pipelines LLM

Avec les approches classiques (LangChain, appels directs aux LLMs), la logique applicative est intimement couplee au texte des prompts. Les developpeurs passent un temps considerable a ecrire et affiner manuellement des prompts qui restent fragiles, difficiles a maintenir et non portables entre modeles. Cela cree trois problemes majeurs :

- **Fragilite** : changer de modele (ex. GPT vers Claude) ou mettre a jour le code casse les prompts existants
- **Non-scalabilite** : affiner manuellement les prompts pour chaque cas d'usage est laborieux et non reproductible
- **Manque de fiabilite** : les prompts manuels ne garantissent pas des sorties structurees ou contraintes

## Qu'est-ce que DSPy

DSPy (Declarative Self-improving Python) est un framework open-source developpe par Stanford NLP qui remplace le prompt engineering par de la programmation declarative. Au lieu d'ecrire du texte de prompt, le developpeur definit des signatures (entrees/sorties attendues) et des modules qui specifient ce que le programme doit faire. DSPy se charge de generer et d'optimiser les prompts en coulisses.

```python
# Exemple de signature DSPy
class QA(dspy.Signature):
    """Repondre a une question en raisonnant etape par etape."""
    question: str = dspy.InputField()
    answer: str = dspy.OutputField()
```

Les applications DSPy sont LLM-agnostiques : elles fonctionnent avec OpenAI, Anthropic Claude, des modeles locaux Hugging Face, etc., sans modifier la logique applicative. Les modules s'enchainent pour former des pipelines complexes, et chaque module peut etre mis a jour ou optimise independamment.

## Fonctionnalites principales

### Signatures declaratives

Les signatures definissent le contrat entrees/sorties d'un module, sans specifier de prompt. DSPy genere automatiquement le prompt optimal a partir de cette specification. Le developpeur declare ce qu'il veut obtenir, pas comment l'obtenir.

### Modules de base (Predictors)

Ces modules sont les briques fondamentales. Tous sont construits par-dessus `dspy.Predict` :

| Module | Paradigme | Cas d'usage typique |
|---|---|---|
| `dspy.Predict` | Direct | Classification, extraction simple |
| `dspy.ChainOfThought` | Raisonnement | QA complexe, analyse |
| `dspy.ProgramOfThought` | Code-first | Maths, requetes structurees |
| `dspy.MultiChainComparison` | Ensemble | Decisions a fort enjeu |
| `dspy.majority` | Vote | Reduction du bruit sur predictions |

### Modules Agents

- **`dspy.ReAct`** : implemente la boucle Reason + Act. Le LM peut appeler des outils externes (fonctions Python, APIs, recherche web) de maniere iterative pour resoudre la tache
- **`dspy.RLM`** (Recursive LM) : explore de tres grands contextes via un REPL Python sandboxide avec des appels recursifs a des sous-LLMs, utile quand le contexte depasse la fenetre du prompt

### Optimiseurs (Teleprompters)

Les optimiseurs ajustent automatiquement les prompts et les demonstrations sans intervention manuelle :

- **BootstrapFewShot** : genere automatiquement des exemples few-shot a partir de donnees d'entrainement
- **MIPROv2** : optimisation bayesienne des instructions a chaque etape du pipeline
- **BootstrapFinetune** : distille un programme DSPy en fine-tuning reel des poids du LM pour des modeles plus petits

Chaque fois que le code ou les donnees changent, une recompilation suffit a regenerer des prompts optimaux.

### Composition de modules personnalises

DSPy permet de creer ses propres modules en heritant de `dspy.Module`, de maniere analogue aux modules PyTorch :

```python
class MonPipeline(dspy.Module):
    def __init__(self):
        self.retrieve = dspy.Retrieve(k=3)
        self.generate = dspy.ChainOfThought("context, question -> answer")

    def forward(self, question):
        context = self.retrieve(question).passages
        return self.generate(context=context, question=question)
```

Cette approche modulaire facilite le debogage et permet d'optimiser chaque composant independamment.

## Cas d'usage typiques

| Cas d'usage | Ce que DSPy apporte |
|---|---|
| **QA / RAG** | Combine retrieval + ChainOfThought, optimise automatiquement |
| **Agents** | Boucle ReAct avec gestion d'outils et backtracking |
| **Classification** | Sorties structurees avec garanties de type |
| **Resume / generation de code** | Pipeline multi-etapes sans prompt manuel |

DSPy est particulierement pertinent pour des projets ou les pipelines LLM sont complexes, multi-etapes, ou doivent evoluer rapidement : RAG sur base documentaire, agents metier, integrations enterprise.

## Positionnement : DSPy vs LangChain

DSPy et LangChain repondent a des philosophies differentes. LangChain est un orchestrateur qui facilite le chainage d'appels LLM, mais le developpeur reste responsable de l'ecriture et de la maintenance des prompts. DSPy abstrait completement la couche prompt : le developpeur programme des modules et des signatures, et le framework optimise les prompts automatiquement.

| Dimension | LangChain | DSPy |
|---|---|---|
| **Approche des prompts** | Ecriture et maintenance manuelles | Generation et optimisation automatiques |
| **Portabilite entre modeles** | Necessite d'adapter les prompts | LLM-agnostique par conception |
| **Paradigme** | Orchestration imperative | Programmation declarative |
| **Optimisation** | Manuelle (iterer sur les prompts) | Automatique (optimiseurs integres) |
| **Maturite ecosysteme** | Large ecosysteme, nombreuses integrations | Ecosysteme plus jeune, focuse recherche |

En pratique, DSPy est le plus adapte lorsque les pipelines LLM sont complexes et doivent etre optimises systematiquement, tandis que LangChain reste pertinent pour des integrations rapides ou l'ecosysteme de connecteurs est un critere prioritaire.

## Sources

- Stanford NLP, DSPy documentation officielle : https://dspy.ai/
- GitHub : https://github.com/stanfordnlp/dspy
- Omar Khattab et al., "DSPy: Compiling Declarative Language Model Calls into Self-Improving Pipelines", Stanford University, 2023
