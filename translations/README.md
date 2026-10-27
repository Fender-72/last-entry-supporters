# Last Entry — traductions communautaires

Le français est le texte de référence du jeu. Vous pouvez corriger une traduction, compléter une langue ou signaler une formulation peu naturelle.

## Proposer une correction sur GitHub

1. Ouvrez le fichier de votre langue : [English](en.json), [日本語](ja.json), [Español](es.json), [Deutsch](de.json), [한국어](ko.json), [中文](zh.json).
2. Cliquez sur le crayon **Edit this file**. Avec votre compte GitHub, GitHub vous proposera de créer une copie du dépôt (fork) si vous n'avez pas les droits d'écriture.
3. Recherchez une phrase avec Ctrl+F. Chaque entrée contient `french` (référence), `translation` (à corriger) et `context`.
4. Modifiez uniquement `translation`, puis cliquez **Propose changes** et **Create pull request**. Décrivez brièvement la correction et la langue.
5. Shokomaki vérifie et accepte les propositions. Les corrections apparaîtront dans une prochaine publication de la map, pas instantanément dans les instances ouvertes.

Vous pouvez aussi ouvrir une **Issue** avec la langue, le français, la correction souhaitée et, si possible, une capture d'écran. Les contributeurs n'ont pas besoin d'Unity ni des fichiers du projet.

## Ce qu'il faut conserver

- Ne modifiez pas `id`, `french`, `sourceHash`, `context`, `archived` ou `excluded`.
- Conservez les variables (`{0}`, `{1}`, `%s`...), les nombres de gameplay et les balises (`<color=...>`, `</color>`, etc.).
- Conservez les retours à la ligne et les tabulations existants. En JSON, ils sont écrits `\n` et `\t`.
- Respectez le format JSON : guillemets, virgules et échappements. Les guillemets dans une traduction doivent être échappés : `\"`.
- `todo` : traduction manquante ; `needs_review` : français modifié, ancienne traduction à vérifier ; `translated` : texte présent, pas nécessairement relu par un humain ; `archived` : ancien texte ; `excluded` : traduction désactivée par le créateur.
- Ignorez les entrées archivées ou exclues. Le texte français du fichier `fr.json` est une référence, pas un fichier à traduire.
- Ne traduisez pas littéralement les noms propres si cela change leur identité ; une translittération naturelle peut être proposée au créateur.

## Pour Shokomaki — mise à jour avant publication

1. Hors Play, ouvrez le traducteur multilingue dans Unity et cliquez **Scanner la scène et les scripts** après vos changements de texte.
2. Dans **4. Communauté / GitHub**, choisissez le dossier `translations` de votre copie locale du dépôt.
3. Récupérez d'abord les dernières corrections validées sur GitHub (GitHub Desktop : Fetch/Pull, ou téléchargement du dépôt).
4. Cliquez **Analyser les corrections du dossier**. Vérifiez les différences, puis **Importer ces corrections dans le catalogue**. Les sources françaises périmées et les variables altérées bloquent l'import.
5. Cliquez **Exporter / actualiser les fichiers FR et langues** pour ajouter les nouveaux textes et actualiser les sources. Les corrections externes en attente sont conservées ; un conflit local/GitHub bloque l'export au lieu d'écraser un texte.
6. Envoyez les fichiers modifiés sur GitHub (GitHub Desktop ou **Add file → Upload files**). Ne remplacez pas `supporters.txt` : ce dossier est indépendant de Patreon.
7. Dans Unity, revenez à l'onglet Textes et cliquez **Appliquer à la scène**, vérifiez le rendu, enregistrez et publiez normalement.

L'outil ne publie rien automatiquement, ne change ni les tailles ni les positions des textes et ne télécharge aucune traduction pendant une partie. Une sauvegarde du catalogue est créée dans `Library/LastEntryTranslationBackups` avant chaque import de corrections.

Les identifiants sont persistants dans le catalogue Unity. Après un premier scan, les textes liés à un emplacement d'auteur identifiable sont suivis : changement de français = ancienne traduction conservée et à vérifier ; disparition = archivage. Si un emplacement est ambigu ou déplacé, l'outil crée une nouvelle entrée au lieu de rattacher une ancienne traduction au mauvais texte. Les entrées historiques dont l'origine n'est pas identifiable sont conservées par précaution.
