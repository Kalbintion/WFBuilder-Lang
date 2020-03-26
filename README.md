# About
This repo is about being able to translate incorrect, missing, outdated, etc language descriptions found throughout Warframe Builder.

# How To Use
Create a Fork of this repo<br />
Make your changes on your Fork<br />
Once done, create a Pull Request (PR)<br />
Review of your PR will be made and upon being accepted will make it to the live site afterwards (usually on next site update)<br />
<br />

# Abilities Format
Each line contains three parts for abilities, each part separated by commas. The first is the ID of the ability, this should **never** be changed. Second part is the frame and ability identifier, the frame should **never** be changed nor should the ability identifier here. The ability identifier in the second part will be changed as deemed necessary by the WFBuilder authors. The final part is the name in the respective language of the ability. Please ensure the files save with Unix style endings (\n)<br />

# Mods Format
Each line contains three parts for mods, each part separated by commas. The first is the ID of the mod, this should **never** be changed. Second part is the displayed name of the mod in the respective language. The third part is the mod's description. Please note that there are specific custom tags in use for displaying information properly. Please refer to the table below. Please ensure the files save with Unix style endings (\n)<br />

| Tag     | Description |
| ------- | ----------- |
| [1]     | Replaced with the mods data, such as damage value. Should be left in-place in the ordering found there.
| [2]     | Replaced with the mods data, such as status chance. Should be left in-place in the ordering found there.
| [3]     | Replaced with the mods data, such as augment ranges. Should be left in-place in the ordering found there.
| [h][/h] | Hides given text. Used for tagging mods to show up on additional searches. |
| [u][/h] | Uppercases text. |
| [hr]    | Creates a horizontal rule. |
| [icon][/icon] | Provides an icon at that part. See ICON_LIST.md |
