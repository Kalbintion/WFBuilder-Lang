# Sur
Ce repo consiste à pouvoir traduire des descriptions de langue incorrectes, manquantes, obsolètes, etc. trouvées dans Warframe Builder.

# Comment utiliser
Créer une fourchette de ce repo<br />
Faites vos changements sur votre Fork<br />
Une fois terminé, créez une Pull Request (PR)<br />
L'examen de votre RP sera effectué et une fois accepté, il sera ensuite rendu sur le site en ligne (généralement lors de la prochaine mise à jour du site)<br />

# Format des capacités
Chaque ligne contient trois parties pour les capacités, chaque partie étant séparée par des virgules. Le premier est l'ID de la capacité, cela ne devrait ** jamais ** être changé. La deuxième partie est le cadre et l'identifiant de capacité, le cadre ne doit ** jamais ** être modifié ni l'identifiant de capacité ici. L'identifiant de capacité dans la deuxième partie sera modifié comme jugé nécessaire par les auteurs de WFBuilder. La dernière partie est le nom dans la langue respective de la capacité. Veuillez vous assurer que les fichiers sont enregistrés avec des terminaisons de style Unix (\n)<br />
<br />
# Format des mods
Chaque ligne contient trois parties pour les mods, chaque partie séparée par des virgules. Le premier est l'ID du mod, cela ne devrait ** jamais ** être changé. La deuxième partie est le nom affiché du mod dans la langue respective. La troisième partie est la description du mod. Veuillez noter que des balises personnalisées spécifiques sont utilisées pour afficher correctement les informations. Veuillez vous reporter au tableau ci-dessous. Veuillez vous assurer que les fichiers sont enregistrés avec des terminaisons de style Unix (\n)<br />

| Tag | Description |
| ------- | ----------- |
| [1] | Remplacé par les données des mods, telles que la valeur des dommages. Doit être laissé en place dans la commande qui s'y trouve.
| [2] | Remplacé par les données de mods, telles que la chance de statut. Doit être laissé en place dans la commande qui s'y trouve.
| [3] | Remplacé par les données des mods, telles que les plages d'extension. Doit être laissé en place dans la commande qui s'y trouve.
| [h][/h] | Masque le texte donné. Utilisé pour baliser les mods pour apparaître sur des recherches supplémentaires. |
| [u][/h] | Texte en majuscules. |
| [hr] | Crée une règle horizontale. |
| [icon][/icon] | Fournit une icône à cette partie. Voir ICON_LIST.md |