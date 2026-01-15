# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is an **Obsidian vault** for managing AI-themed articles in French. Articles can be published to newsletters, blogs, or exported as PDFs. The vault uses the Dataview plugin for dynamic indexing.

## Folder Structure

```
Articles_IA/
├── FACT/       → Articles de type "fact"
├── IDEA/       → Articles de type "idea"
├── ACTOR/      → Articles de type "actor"
├── RISK/       → Articles de type "risk"
├── FUTURES/    → Articles de type "futures"
├── TOOLS/      → Articles de type "tools"
├── PAPERS/     → Articles de type "papers"
├── _templates/ → Templates d'articles
├── _index.md   → Index maître (Dataview)
└── AGENT.md    → Consignes éditoriales complètes
```

## Article Types and IDs

| Type | ID Prefix | Folder | Description |
|------|-----------|--------|-------------|
| fact | AI-FACT-XXX | FACT/ | Faits vérifiés sur l'IA |
| idea | AI-IDEA-XXX | IDEA/ | Concepts et réflexions |
| actor | AI-ACTOR-XXX | ACTOR/ | Acteurs de l'écosystème IA |
| risk | AI-RISK-XXX | RISK/ | Risques liés à l'IA |
| futures | AI-FUTURES-XXX | FUTURES/ | Prospective et tendances |
| tools | AI-TOOLS-XXX | TOOLS/ | Outils et technologies |
| papers | AI-PAPERS-XXX | PAPERS/ | Articles académiques |

## Workflow de création d'article

### Étape 1 : Déterminer le prochain ID

Lister les fichiers existants dans le dossier cible pour trouver le dernier numéro :
```bash
ls -1 RISK/  # Exemple pour un article RISK
```
Le nouvel ID = dernier numéro + 1 (format 3 chiffres : 001, 002, etc.)

### Étape 2 : Créer le fichier

- **Emplacement** : `{TYPE}/{ID}.md` (ex: `RISK/AI-RISK-001.md`)
- **Nom du fichier** = ID de l'article

### Étape 3 : Appliquer le front-matter

```yaml
---
id: AI-{TYPE}-{NUM}
type: {type_lowercase}
title: "Titre descriptif et informatif"
status: draft
created: {date_du_jour}
updated: {date_du_jour}
---
```

### Étape 4 : Structure du contenu

Utiliser la structure de base puis adapter selon le type :

```markdown
# {Titre de l'article}

## Résumé

## Contenu principal

## Sources
```

**Important** : Pour les articles suivants, s'inspirer de la structure du dernier article publié du même type.

## Règles éditoriales strictes

### Obligatoire
- Langue : **Français**
- 1 fichier = 1 article = 1 idée
- Front-matter YAML **toujours en premier**
- Ton neutre, factuel, précis
- Aucune invention de sources ou de faits

### Interdit
- Mélanger plusieurs types dans un article
- Modifier l'ordre ou le nom des sections standard
- Ajouter des sections non prévues
- Créer un article sans front-matter
- Utiliser des emojis (sauf demande explicite)

## Commandes utiles

```bash
# Voir tous les articles d'un type
ls -la RISK/

# Compter les articles par type
ls -1 FACT/*.md 2>/dev/null | wc -l

# Trouver le dernier ID d'un type
ls -1 IDEA/ | sort -V | tail -1
```

## Checklist avant finalisation

- [ ] Front-matter complet et valide
- [ ] ID unique et correctement formaté
- [ ] Fichier dans le bon dossier
- [ ] Titre clair et descriptif
- [ ] Sources citées si applicable
- [ ] Pas de contenu inventé

## Reference

Voir `AGENT.md` pour les consignes éditoriales détaillées et les modèles par type d'article.
