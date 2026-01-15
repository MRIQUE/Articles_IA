# Index des articles IA

## Tous les articles

```dataview
TABLE type AS "Type", title AS "Titre", status AS "Statut", updated AS "Mis à jour"
FROM ""
WHERE id != null AND !contains(file.path, "_templates")
SORT updated DESC
```

## Brouillons en cours

```dataview
TABLE type AS "Type", title AS "Titre", created AS "Créé le"
FROM ""
WHERE status = "draft" AND !contains(file.path, "_templates")
SORT created DESC
```

## Articles publiés

```dataview
TABLE type AS "Type", title AS "Titre", updated AS "Publié le"
FROM ""
WHERE status = "published" AND !contains(file.path, "_templates")
SORT updated DESC
```

## Statistiques par type

```dataview
TABLE length(rows) AS "Nombre d'articles"
FROM ""
WHERE id != null AND !contains(file.path, "_templates")
GROUP BY type
```
