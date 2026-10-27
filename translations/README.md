# Last Entry — traductions communautaires

## Ce qu'il faut conserver

- Ne modifiez pas `id`, `french`, `sourceHash`, `context`, `archived` ou `excluded`.
- Conservez les variables (`{0}`, `{1}`, `%s`...), les nombres de gameplay et les balises (`<color=...>`, `</color>`, etc.).
- Conservez les retours à la ligne et les tabulations existants. En JSON, ils sont écrits `\n` et `\t`.
- Respectez le format JSON : guillemets, virgules et échappements. Les guillemets dans une traduction doivent être échappés : `\"`.
- `todo` : traduction manquante ; `needs_review` : français modifié, ancienne traduction à vérifier ; `translated` : texte présent, pas nécessairement relu par un humain ; `archived` : ancien texte ; `excluded` : traduction désactivée par le créateur.
- Ignorez les entrées archivées ou exclues. Le texte français du fichier `fr.json` est une référence, pas un fichier à traduire.
- Ne traduisez pas littéralement les noms propres si cela change leur identité ; une translittération naturelle peut être proposée au créateur.
