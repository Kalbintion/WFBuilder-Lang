# About
This repo is about being able to translate/update incorrect, missing, outdated, etc language descriptions found throughout Warframe Builder. It will be generally helpful, but not a requirement, to be able to speak and understand English in some situations.

# How To Use
- Create a Fork of this repo
- Make your changes on your Fork
  - For Abilities, see section [How To Translate Details](#How_To_Translate_Details) and edit the EN/Abilities.txt
  - For Mods, edit the EN/Mods.txt
  - For Details, edit the EN/Details.txt
- Once done, create a Pull Request (PR)
- Review of your PR will be made and upon being accepted will make it to the live site afterwards (usually on next site update)
  - If your PR is not accepted, a note on why will made, and fixes will need to happen before it can be accepted. Common issues for this would be the formatting of the changes not following guidelines.

# How To Translate Abilities
You will find a header line, such as `# Ash`, for abilities for that frame to help minimize confusion and to find an ability faster. Each line contains two parts for abilities, each part separated by commas. The first is the ID of the ability, this should **never** be changed. The second part is the name in the respective language of the ability. Please ensure the files save with Unix style endings (\n)

#### Examples
For [Ember](https://warframe.fandom.com/wiki/Ember) who had a rework that changed two of her ability names, Accelerant and World on Fire to Immolation and Inferno, respectively, would cause their respective lines in the EN/Abilities.txt file from:

`6,Accelerant` to `6,Immolation` and

`8,World On Fire` to `8,Inferno`

Or for [Vauban](https://warframe.fandom.com/wiki/Vauban) who had received a rework at the same time, having his ability Tesla Grenades be replaced with Tesla Nervos, his Bastille moving into his fourth slot, and Vortex being combined with Bastille caused his abilities would require the following updates:

**Tesla Grenades -> Tesla Nervos**

`61,Tesla Grenades` to `61,Tesla Nervos`

**Bastille -> Photon Strike**

`63,Bastille` to `63,Photon Strike`

**Vortex -> Bastille**

`64,Vortex` to `64,Bastille`

# How To Translate Mods
Each line contains three parts for mods, each part separated by commas. The first is the ID of the mod, this should **never** be changed. Second part is the displayed name of the mod in the respective language. The third part is the mod's description. Please note that there are specific custom tags in use for displaying information properly. Please refer to the table (Mod Tags) below. Please ensure the files save with Unix style endings (\n)

#### Examples
For the mod [Fulmination](https://warframe.fandom.com/wiki/Fulmination) that changed to being permitted on all secondaries and where its description changed, the line would go from it's previous description of:
`817,Fulmination,Improves the blast radius of secondary launcher weapons. +[1]% Blast Radius`
to
`817,Fulmination,Improves the Blast Radius of weapons with Radial Attacks. +[1]% Blast Radius`

For the mod [Guided Ordnance](https://warframe.fandom.com/wiki/Guided_Ordnance) where the name was incorrectly displayed on the site before as Guided Ordinance, the line would go from it's previous value of:
`632,Guided Ordinance,[u]on hit:[/u] +[1]% Accuracy while aiming for [2] seconds.`
to
`632,Guided Ordnance,[u]on hit:[/u] +[1]% Accuracy while aiming for [2] seconds.`

#### Table: Mod Tags
| Tag     | Description |
| ------- | ----------- |
| [1]     | Replaced with the mods data. Typically the first variable for the mod.
| [2]     | Replaced with the mods data. Typically the second variable for the mod.
| [3]     | Replaced with the mods data. Typically the third variable for the mod.
| [h][/h] | Hides given text. Used for tagging mods to show up on additional searches. |
| [u][/u] | Uppercases text. **Deprecated. This tag to be phased out. Match capitalization to the mod found in-game.** |
| [hr]    | Creates a horizontal rule. |
| [icon][/icon] | Provides an icon at that part. See [ICON_LIST.md](ICON_LIST.md) |

# How To Translate Details
The Details file contains extra information typically used by warframes, mods and other key parts of the interface. This includes information like special ability descriptions and augment descriptions found in the Details tab of a warframe. The information is broken up into sections to find easier, including header comments for frames and their abilities.

Each line found in there contains the key used by WFBuilder, surrounded by single quotes, following by an equal sign and greater than (`=>`) and finally the string that is shown. This is typically encapsulated by single or double quotes and the line ends with a comma. The only portion that should be modified with the displayed string mentioned, and the line must end with a comma. For those who are a bit more knowledgeable about programming, this is the contents of a PHP array used by the language file itself.

#### Examples
If, as a hypothetical, the status Magnetic term was no longer used and DE changed it to be "shield shock" then the following line would need to be changed:

`'magnetique'=>'magnetic',` to `'magnetique'=>'shield shock',`

Or if Ash's Shurikens were renamed as Throwing Stars, then the line for his ability, found under the header `// SHURIKEN` would be changed from:

`'shuriken'=>'shuriken(s)',` to `'shuriken'=>'throwing star(s)',`
