README
Amethyst Imbuement
------------------

Config Changelog:
1.18.1-13/1.18.2-14: Added imbuingTableReplaceEnchantingTable to the Altars Config. Config updated to v1.
1.19-09/1.18.2-26: updated Altars to v2 with the addition of many (currently unused) integration options. Updated Villages to v1 with the addition of many options related to CTOV and RS. Updated Scepters to v1 and added default durabilities/damage values for the Scepter of Blades and Lethality.
1.19-11/1.18.2-28: Added the entities config file.
1.19-14/1.18.2-31: Added the trinkets config file and updated Entities to v1 with (currently unused) selections.
1.19-22/1.18.2-39: changed the scepters config from scepters_v1 to items_v0 and added the glistering tome boolean.
1.19.3-02/1.19-25/1.18.2-42: Added a config for the chance an experience bush will grow (in Altars config v3).
1.19.3-03/1.19-26/1.18.2-43: Added configurable durability for the Totem of Amethyst.

Note:  Previous versions of updated configs that have new version numbers (v1 from v0, for example) will be read and copied over to the new version, and the old version deleted.


Items Config:
The items config json tweaks the properties of the scepters in-game. You may want to tweak it if you feel like scepters have too many uses at once, or conversely if you feel that they run out of mana too quickly

> giveGlisteringTome: if set to false, a player joining the world for the first time won't be given a Glistering Tome.
> totemOfAmethystDurability: default 360, defines the mana (durability) of the Totem of Amethyst.
> opalineDurability: define durability for the Opaline Scepter (Low tier).
> iridescentDurability: define durability for the Iridescent Scepter (mid tier).
> lustrousDurability: define durability for the Lustrous Scepter (high tier).
> baseRegenRateTicks: how quickly the scepters regain mana naturally. Value is in ticks (20 tick per second). 20 ticks is the minimum allowed.
> bladesDurability: the durability for the Scepter of Blades item
> bladesDamage: the damage of the Scepter of Blades item
> lethalityDurability: the durability for the Lethality item
> lethalityDamage: the damage of the Lethality item


Altars Config:
This json defines functional tweaks for the altars, tables, and blocks in the mod.

> experienceBushBonemealChance: sets the chance that an experience bush will grow to the next phase when bonemeal is used on it. Set to 0.0 to make experience bushes not grow with bonemeal.
> experienceBushBonemealChance: chance that an experience bush will grow to the next phase when ticked randomly ('natural' growth). Set to 0.0 to make experience bushes not grow naturally at all.
> disenchantLevelCosts: array of the levels required to disenchant the first, second, third, etc. enchantment off a particular item. You can extend this array if you'd like, but it won't do anything unless you also add to the base disenchants allowed. If you allow 3 base enchants, an array up to 7 long would have practical use.
> disenchantBaseDisenchantsAllowed: the base number of disenchants allowed with just the table present before adding pillars. If you want virtually infinite disenchants, make this number very high. You could make it 0, meaning you have to add pillars before you can disenchant at all, but I don't recommend it.
> imbuingTableEnchantingEnabled: disable this to prevent the player from using the imbuing table as an enchanting table. Use this if you have an alternate enchanting system and don't want the table to allow vanilla style enchanting.
> imbuingTableReplaceEnchantingTable: disabled by default. Enable to replace all Enchanting Tables with Imbuing tables during structure generation. Doesn't affect existing structures or tables.
> imbuingTableDifficultyModifier: Multiplies the level cost of imbuing by the value entered. A value of 0.5 will halve the imbuing level costs, 2.0 will double them, and so on. Clamped between 0.0 (free) and 10.0
> imbuingTableMatchEasyMagicBehavior: (currently unused) Matches the enchanting table behavior of Easy Magic if that mod is installed, based on the following Easy Magic related config options.
> imbuingTableEasyMagicRerollEnabled: (currently unused) If true, enabled rerolling of shown enchantments in the same style as Easy magic
> imbuingTableEasyMagicLevelCost: (currently unused) Integer determining the number of enchantment levels needed to reroll Easy Magic-style
> imbuingTableEasyMagicLapisCost: (currently unused) Integer determining the number of lapis lazuli needed to reroll Easy Magic-style
> imbuingTableEasyMagicShowTooltip: (currently unused) If false, will not show an enchantment tooltip in the table at all
> imbuingTableEasyMagicSingleEnchantTooltip: (currently unused) If set to false, will show all enchantments that would be added with the highlighted enchantment process instead of just a random one from the list.
> imbuingTableEasyMagicLenientBookshelves: (currently unused) If set to true, allows other non-solid blocks besides air to be between the shelves and table (like water)
> imbuingTableMatchRerollBehavior: (currently unused) Matches the rerolling behavior of Reroll if that mod is installed, based on the following Reroll related config options.
> imbuingTableRerollLevelCost: (currently unused) Integer determining the number of enchantment levels needed to reroll Reroll-style
> imbuingTableRerollLapisCost: (currently unused) Integer determining the number of lapis lazuli needed to reroll Reroll-style
> imbuingTableMatchEnhancementBehavior: (currently unused) Matches the enchanting table behavior of Enhancement if that mod is installed, based on the following Enhancement related config options.
> imbuingTableEnhancementLevelsPer: (currently unused) Integer determining the number of enchantment levels needed for each enchantment being added Enhancement-style
> imbuingTableEnhancementLapisPer: (currently unused) Integer determining the number of lapis lazuli for each enchantment being added Enhancement-style
> imbuingTableMatchEasierEnchantingBehavior: (currently unused) Matches the enchanting table behavior of Easier Enchanting if that mod is installed, based on the following Easier Enchanting related config options.
> imbuingTableEasierEnchantingLapisCost: (currently unused) Integer determining the number of lapis lazuli needed to reroll Easier Enchanting-style
> imbuingTableMatchBetterEnchantmentBoostingBehavior: (currently unused) Matches the bookshelf placement behavior of Better Enchantment Boosting if that mod is installed.
> altarOfExperienceBaseLevels: Base number of levels a player can store in an altar of experience surrounded by 0 candles.
> altarOfExperienceCandleLevelsPer: Number of storable levels each candle placed around the altar of experience adds. Warding Candles provide double this base bonus.
> altarOfExperienceCustomXpMethod: When true, the Altar of Experience will use a custom method for giving/taking XP that bypasses vanilla code. This might help avoid undesirable interactions with mods that monitor XP gain. If these interactions are desirable, set to false.


Entities Config:
This config sets various base stats for custom Amethyst Imbuement mobs that can be summoned or otherwise created.

> unhallowedBaseLifeSpan: The base lifespan in ticks of the Unhallowed mob created by the Summon Zombie augment. Setting this below zero will make the lifespan infinite.
> unhallowedBaseHealth: The base health points of the Unhallowed mob.
> unhallowedBaseDamage: The base damage of the Unhallowed mob.
> crystalGolemSpellBaseLifeSpan: The base lifespan in ticks of the Crystalline Golem mob created by the Summon Golem augment. Setting this below zero will make the lifespan infinite.
> crystalGolemSpellPerLvlLifeSpan: The additional Crystalline Golem lifespan in ticks per level of the Summon Golem augment (levels start at 1 so this is always counted at least once). Setting this below zero alongside the base lifespan will make the lifespan infinite.
> crystalGolemGuardianLifeSpan: The base lifespan in ticks of the Crystalline Golem mob created by the Guardian augment trigger. Setting this below zero will make the lifespan infinite.
> crystalGolemBaseHealth: The base health points of the Crystalline Golem mob.
> crystalGolemBaseDamage: The base damage of the Crystalline Golem mob.


Colors Config:
This config sets the outline colors for the various ores when seen under the Draconic Vision augment. If an ore is not in these lists, it will appear as the default white outline. Map keys are the ore identifiers, which can be seen with the advanced tooltips turned on (F3+H by default). If an ore is in both a color map and a rainbow list, the rainbow list will take precedence. The mod color map takes precedence over the default one, in case you put a pre-existing color in the mod map, your desired color will still be shown

Precedence: defaultRainbowList = modRainbowList > modColorMap > defaultColorMap

> defaultColorMap: A map of the default colors pre-assigned to vanilla ores. By default includes some ores from common ore-gen mods.
> defaultRainbowList: List of the vanilla ores that are pre-assigned a rainbow outline. By default includes some ores from common ore-gen mods.
> modColorMap: A map where you can add ores from other mods you are playing with.
> modRainbowList: List for mod ores you want to appear as a rainbow outline.


Augments Configs:
These configs allow you to tweak the casting parameters for individual spells. Change these if you perhaps think a spell doesn't cost enough mana, or is too slow between casts

> id: don't change this, or the config will break for that spell.
> enabled: if set to false, it will stop the game from registering this spell. Combine this with removing the recipe via kubejs or similar to completely remove an augment from the game.
> cooldown: time in ticks (20 per second) between each cost of the spell.
> manaCost: durability usage of the scepter on each cast. Note the default durabilities in the scepter config to determine proper values.
> minLvl: the minimum scepter level required before the spell can be used in that scepter. Recommend keeping as-is, but may be useful to tweak if you think a spell is too easy to attain, for example.


Villages Configs
These configs allow you to tweak the generation for the Crystal Workshops
> enable[Village_Type]Workshops: True by default. If for some reason you wish to disable generation completely, set to false.
> [Village_Type]WorkshopWeight: The weight that the workshops are selected from the building pool for spawning in villages. Recommend leaving as-is.
> ctov[___]: switch and weights for custom crystal workshops integrated into the ChoiceTheorems Overhauled Villages mod.
> rs[___]: switch and weights for custom crystal workshops integrated into the Repurposed Structures mod.


Enchantments Config
This config allows you to enable or disable the various vanilla-style enchantments added by the mod. You may want to disable an enchantment this way if, for example, an enchantment is redundant to another mods enchantment and you want to reduce clutter.

> enabledEnchantments: A map of the enchantments the mod adds and if they are enabled. All enchantments are enabled by default.


Trinkets Config
This config allows you to enable or disable the various trinket augments added by the mod. You may want to disable an augment this way if, for example, the server AI is being added to does not want creative flight (disable Angelic in this case).

> enabledAugments: A map of the augments the mod adds and if they are enabled. All augments are enabled by default.
