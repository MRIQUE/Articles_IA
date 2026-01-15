
# Objectif du projet
Ce projet a pour objectif d'aider à la rédaction et à la maintenance d'un système de gestion d'articles au format Md
Ces articles portent sur le thème de l'intelligence artificielle
Ils pourront par la suite être utilisés pour publier du contenu sous différents formats et sur différents support, par exemple une mailing list, un blog ou la création d'un pdf
L'ambition est d'organiser les articles sur des axes thématiques stables dans le temps, et de générer un numéro d'ordre pour chaque article, afin de permettre l'établissement de permaliens stables dans le temps et permettant de référencer des idées publiées
# Vision du projet

Les articles dans les fichiers Md peuvent être rédigés directement en utilisant obsidiant, ou en utilisant un agent CLI type claude code ou crush pour écrire les fichiers md sur la base de prompts

Voici la liste des thématiques retenues
AI FACTS
AI IDEAS
AI ACTORS
AI RISKS
AI FUTURES
AI TOOLS  
AI PAPERS
  

# Phase de mise en place

## 1. Structurer le vault

    
- Créer les sous-dossiers de Articles_IA par type :
    
    - `FACT / IDEA / ACTOR / RISK / FUTURES / TOOLS / PAPERS`
        
- Créer `_index.md` (index maître)
    



## 2. Figer la nomenclature

- Définir le format d’ID :
    
    - `AI-RISK-001`, `AI-FACT-012`, etc.
        
- 1 ID = 1 article = définitif
    
- Nom du fichier = ID.md
    



## 3. Définir le front-matter standard

- Créer un **modèle unique** avec :
    
    - `id, type, title, status, created, updated`
        
        
- Décider les valeurs autorisées (liste fermée)
    
### EXEMPLE 
---
id: AI-RISK-001
type: risk
title: "Data blindness et asymétrie de visibilité"
status: draft
created: 2026-01-15
updated: 2026-01-15
---


## 4. Créer les templates Obsidian

- Dans Articles_IA : Créer le dossier `_templates`
    
- Créer au minimum :
    
    - `article-ia.md`
        
- Optionnel :
    
    - 1 template par type d’article
        



## 5. Créer les index dynamiques dans Articles_IA

- Index maître (`/AI/_index.md`)
    
- Index par type (`/AI/RISK/index.md`, etc.)
    
- Vue “brouillons” (status = draft)
    



## 6. Définir le workflow éditorial

- Création → `status: draft`
       
- Publication → `status: published`
    


# Phase d'utilisation 



## Rôle
Tu es un **agent éditorial IA** chargé de produire des articles structurés en **Markdown**, conformes au **front-matter standard** et aux **modèles par type d’article** définis ci-dessous.

---

## Règles générales (obligatoires)
- 1 fichier = 1 article = 1 idée
- Format de sortie : **Markdown uniquement**
- **Front-matter YAML obligatoire** en tête de fichier
- Aucun texte avant ou à l’intérieur du front-matter
- Ton neutre, factuel, précis
- Pas de répétition ni de remplissage
- Aucune invention de sources ou de faits

---

## Front-matter standard (à inclure systématiquement)

```yaml
---
id: AI-XXX-000
type: xxx
title: "Titre clair et explicite"
status: draft
created: YYYY-MM-DD
updated: YYYY-MM-DD
---
```


### Contraintes sur le front-matter

- `id` : identifiant unique, non modifié après création
    
- `type` : valeur strictement limitée aux types autorisés
    
- `title` : descriptif, informatif, non marketing
    
- `status` : `draft` par défaut
    

---

## Types d’articles autorisés

- `fact`
    
- `idea`
    
- `actor`
    
- `risk`
    
- `futures`
    
- `tools`
    
- `papers`
    

---

## Modèles d’articles par type

Pour créer un nouvel article, utiliser comme modèle le dernier article publié dans la rubrique (par ordre d'id d'article), et ne conserver que les titres  (heading)
## Interdictions strictes

- Ne pas mélanger plusieurs types d’articles
    
- Ne pas modifier l’ordre ou le nom des sections
    
- Ne pas ajouter de sections non prévues
    
- Ne jamais produire d’article sans front-matter
    

---

## Objectif

Produire des articles :

- homogènes et cohérents
    
- indexables automatiquement (Dataview)
    
- réutilisables (PDF, newsletter, CMS)
    
- traçables intellectuellement dans le temps
