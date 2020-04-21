# A propos
Ce dépôt (repository) à pour but de permettre la traduction et la mise à jour de textes et descriptions incorrects, manquants, obsolètes, etc, présents sur Warframe Builder. Il sera généralement utile de comprendre l'anglais pour participer à la traduction, bien que cela ne soit pas indispensable.

# Comment l'utiliser
- Créez une copie (fork) de ce dépôt
- Faites vos changements sur votre copie
  - Pour les compétences, reportez-vous à la section [Comment traduire les compétences](#Comment-traduire-les-compétences) et éditez le fichier FR/Abilities.txt
  - Pour les mods, reportez-vous à la section [Comment traduire les mods](#Comment-traduire-les-mods) et éditez le fichier FR/Mods.txt
  - Pour l'onglet Détails, reportez-vous à la section [Comment traduire l'onglet Détails](#Comment-traduire-longlet-Détails) et éditez le fichier FR/Details.txt
- Une fois terminé, créez une « pull request » (PR)
- Votre PR sera vérifiée et mise en ligne une fois acceptée, généralement lors de la mise à jour suivante
  - Si votre PR n'est pas acceptée, des informations concernant les raisons de ce refus vous seront communiquées. Les changement nécessaires devront être appliqués afin de voir votre PR acceptée. Les problèmes les plus courants concernent le formatage du texte qui ne respecte pas les règles établies.

# Comment traduire les compétences
Pour chaque Warframe, vous trouverez une entête du type `# Ash`, permettant de trouver facilement les compétences associées, celles-ci étant les quatre lignes juste en dessous. Chacune de ces lignes représente une compétence et est composée de deux parties, séparées par une virgule. La première partie est l'identifiant (ID) de la compétence. Cette valeur ne doit **jamais** être modifiée. La seconde partie est le nom de la compétence. C'est cette partie qui doit être traduite en français, ou actualisée, le cas échéant. Veuillez vous assurer de sauvegarder vos fichiers avec des [fins de lignes « Unix » (\n)](#fins-de-lignes--unix--n)

#### Exemples
Pour [Ember](https://warframe.fandom.com/fr/wiki/Ember), dont une mise à jour modifiant le nom des compétences a eu lieu, Accélérant et Monde de Feu étant respectivement renommés Immolation et Inferno, les lignes du fichier FR/Abilities.txt ont changé de la façon suivante.

`6,Accélérant` vers `6,Immolation`

`8,Monde de Feu` vers `8,Inferno`

Pour [Inaros](https://warframe.fandom.com/fr/wiki/Inaros), dont les compétences n'ont jamais été traduites sur Warframe Builder, les lignes du fichier FR/Abilities.txt devraient changer de la façon suivante pour que la traduction soit correcte.

`125,Desiccation` vers `125,Dessiccation`

`126,Devour` vers `126,Inhumation`

`127,Sandstorm` vers `127,Tempête de Sable`

`128,Scarab Swarm` vers `128,Nuée de Scarabées`

# Comment traduire les mods
Pour les mods, chaque ligne est composée de trois parties, séparées par des virgules. La première est l'identifiant du mod (ID), et ne devrait **jamais** être modifiée. La seconde partie est le nom du mod et la troisième la description. Veuillez noter que les descriptions incluent des balises spécifiques nous permettant d'afficher les informations du mod correctement. Référez-vous au tableau des balises ci-dessous pour de plus amples informations à ce sujet. Veuillez également vous assurer de sauvegarder vos fichiers avec des [fins de lignes « Unix » (\n)](#fins-de-lignes--unix--n)

#### Exemples
La description du mod [Pensée Rapide](https://warframe.fandom.com/fr/wiki/Pens%C3%A9e_Rapide) sur Warframe Builder est obsolète et n'a également que peu de sens dans sa version actuelle. La ligne actuelle `57,Pensée Rapide,Drains d'énergie pour arrêter les blessures mortelles avec +[1]% d'efficacité.` devra être modifiée de la façon suivante : `57,Pensée Rapide,Draine l'énergie pour absorber une blessure mortelle avec +[1]% d'efficacité.`

Si vous désirez traduire le mod [Coaction Drift](https://warframe.fandom.com/wiki/Coaction_Drift) en français ([Art de la Coaction](https://warframe.fandom.com/fr/wiki/Art_de_la_Coaction)), la ligne `612,Coaction Drift,[u]+[1]% aura strength +[2]% aura effectiveness[/u]` devra être modifiée de la façon suivante : `612,Art de la Coaction,+[1]% de Puissance de l'Aura +[2]% d'Efficacité de l'Aura`

#### Tableau : Balises des mods
| Balise  | Description |
| ------- | ----------- |
| [1]     | Identifiant pour la première valeur variable du mod (valeur qui change en fonction du rang).
| [2]     | Identifiant pour la seconde valeur variable du mod (valeur qui change en fonction du rang).
| [3]     | Identifiant pour la troisième valeur variable du mod (valeur qui change en fonction du rang).
| [h][/h] | Masque le texte. Utilisé pour « tagger » les mods avec des mots-clés supplémentaires pour enrichir les recherches. |
| [u][/u] | Texte en majuscule. **Préférez désormais entrer le texte directement en majuscule afin de retirer ces tags.** |
| [hr]    | Crée une ligne horizontale. |
| [icon][/icon] | Affichage d'une icone. Voir [ICON_LIST.md](ICON_LIST.md) |

# Comment traduire l'onglet Détails
Le fichier FR/Details.txt contient les chaines de texte relatives aux informations liées aux Warframes, à certains mods et à des éléments de l'interface en général. Cela inclut entre autres les descriptions des effets des compétences, trouvées dans l'onglet Détails, pour chaque Warframe. Le fichier est découpé en plusieurs sections, elles-mêmes précédées de commentaires permettant de trouver facilement ce que vous recherchez.

Chaque ligne de ce fichier est composée de la clé utilisée par WFBuilder pour identifier ce texte, entourée de guillemets simples et suivie d'une flèche (`=>`), elle-même suivie du texte associé à cette clé, le texte affiché sur WFBuilder. Cette dernière partie est entourée de guillemets simples ou doubles et la ligne se termine par une virgule. Seul le contenu de cette dernière partie et qui se trouve entre guillemets doit être modifié. Pour ceux qui sont familiers avec les langages de programmation, il s'agit du contenu d'un tableau en PHP. Veuillez vous assurer de sauvegarder vos fichiers avec des [fins de lignes « Unix » (\n)](#fins-de-lignes--unix--n)

#### Exemples
Si, pour une raison quelconque, le statut Magnétique changeait de nom et que DE décidait de le renommer « Tempête d'électricité », alors la ligne ci-dessous devrait être modifiée de la façon suivante :

`'magnetique'=>'magnétique',` vers `'magnetique'=>'tempête d\'électricité',`

Notez le caractère d'échappement `\` (antislash) utilisé devant l'apostrophe du bloc `d\'électricité`. Il est nécessaire pour indiquer au script que ce guillemet simple n'indique pas la fin d'une chaine de texte, car il est le même que les guillemets simples qui entourent le bloc de texte. Une solution alternative est d'utiliser les guillemets doubles plutôt que le caractère d'échappement, cela produit exactement le même résultat. `'magnetique'=>"tempête d'électricité",`

Si les Shurikens que lance Ash étaient renommés Étoiles Filantes, alors la ligne suivante, trouvée facilement grace à l'entête `// SHURIKEN`, devrait être modifiée de la façon suivante :

`'shuriken'=>'shuriken(s)',` to `'shuriken'=>'étoile(s) filante(s)',`

# Fins de lignes « Unix » (\n)
Il est préférable d'utiliser la convention « Unix » pour les fins de lignes de ces fichiers, cela générera moins de problèmes lorsque vos données seront analysées par le système pour être intégrées à l'application. Si vous n'êtes absolument pas en mesure de respecter la convention « Unix » pour les fins de lignes, merci de le préciser dans votre PR.

Ci-dessous, une liste de liens vers la marche à suivre pour vous assurer de sauvegarder vos fichiers en respectant la convention « Unix » pour les fins de lignes, pour les éditeurs de texte les plus populaires.
* Notepad: Aucun support en dehors de Windows 10
* [Notepad++](https://notepad-plus-plus.org/downloads/): <https://support.nesi.org.nz/hc/en-gb/articles/218032857-Converting-from-Windows-style-to-UNIX-style-line-endings#how-to-convert>
* [Atom](https://atom.io/): <https://stackoverflow.com/a/48686409>
* [VSCode](https://code.visualstudio.com/): <https://marketplace.visualstudio.com/items?itemName=JakubBielawa.LineEndingsUnifier>
