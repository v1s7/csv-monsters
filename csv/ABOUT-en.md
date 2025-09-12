<sup>written by v1s7, special thanks to Null's Brawl Mods<!--Pro--> group</sup> 

<!--
v62 new files:

csv/csv_client/character_components_client.csv
        csv/csv_logic/character_components_logic.csv
        csv/csv_logic/record_levels.csv
        csv/csv_logic/records.csv
        csv/csv_logic/traits.csv
        csv/csv_logic/trophy_world_milestones.csv
        csv/csv_logic/trophy_world_parts.csv
        csv/csv_logic/trophy_worlds.csv
-->
[Версия на русском 🇷🇺](/csv/ABOUT.md)
 
The contents of this list can be accessed by clicking the ⋮☰ button in the upper right corner.
-----

> [!NOTE] 
> It is recommended that you read the [manual](/MANUAL.md) before you start reading.

-----
# Symbols
- 👻 - Not yet written / more information required
- 🧊 - Github won't make a neat table out of this file as it weighs more than 400 KB. In that case, download it («•••» → «Download», on a computer it's just «<ins>↓</ins>») and open it locally
- 🪦 - Files not used in the game, and therefore not of interest for modding.
<!--- ⛔ - The file is (almost or completely) unmodifiable-->

# csv-client
Files that specify client-side behavior, i.e. fully modifiable.

###### [animations.csv](/csv/csv_client/animations.csv "animations.csv") 🧊
Controls all brawler and skin animations. Includes start/end of animations, their speed, transitions, cycling and playback priority
###### [availability_window.csv](/csv/csv_client/availability_window.csv "availability_window.csv") 
Responsible for availability of skins for limited or seasonal time (corresponding icon under skins)
###### [billing_packages.csv](/csv/csv_client/billing_packages.csv "billing_packages.csv")
Every single in-game purchase with real money. Gets ignored in Null's Brawl
###### [bp_purchase_popup.csv](/csv/csv_client/bp_purchase_popup.csv "bp_purchase_popup.csv") 
Brawl Pass purchase animation, as well as pin and skin animations from it
###### [character_components_client.csv](/csv/csv_client/character_components_client.csv "character_components_client.csv") 👻 
…
###### [client_globals.csv](/csv/csv_client/client_globals.csv "client_globals.csv") 
Various global client customizations
###### [color_gradients.csv](/csv/csv_client/color_gradients.csv "color_gradients.csv") 
Sets the colors, speed and intensity of gradient text in different parts of the game
###### [credits.csv](/csv/csv_client/credits.csv "credits.csv") 
A list of all the developers who participated in the development of the game. It can be found in the corresponding button in the game settings.
###### [effects.csv](/csv/csv_client/effects.csv "effects.csv") 🧊
Lists every single visual effect in the game (and there're quite a few)
###### [faces.csv](/csv/csv_client/faces.csv "faces.csv") 
Lists the basic animations of brawlers and their skins from characters.sc, namely on victory, defeat and inactivity
###### [fame_tiers.csv](/csv/csv_client/fame_tiers.csv "fame_tiers.csv") 
Stages of credit fame and everything related to them
###### [health_bars.csv](/csv/csv_client/health_bars.csv "health_bars.csv") 
Columns that show the health of players and NPCs (robots)
###### [hints.csv](/csv/csv_client/hints.csv "hints.csv") 
Shelly's hints (early in the game), player selection tips, and other advices
###### [local_notifications.csv](/csv/csv_client/local_notifications.csv "local_notifications.csv") 
Push notifications (those sent outside the game)
###### [location_features.csv](/csv/csv_client/location_features.csv "location_features.csv") 
Makes changes to map environments when certain conditions are met (for example, hides Tara from the bazaar background if she was picked by the player in a match).
###### [login_calendar_items.csv](/csv/csv_client/login_calendar_items.csv "login_calendar_items.csv") 
Every single daily reward
###### [music.csv](/csv/csv_client/music.csv "music.csv") 
Manages all music in the game. Includes track path, designation of the track as background, backup for playback, volume, whether the track needs to be looped infinitely or how many times it needs to be done
###### [particle_emitters.csv](/csv/csv_client/particle_emitters.csv "particle_emitters.csv")
Controls all particles in the game, their sources from effects.sc and has many different parameters
###### [shop_items.csv](/csv/csv_client/shop_items.csv "shop_items.csv")
Everysingle item in the shop
###### [sounds.csv](/csv/csv_client/sounds.csv "sounds.csv") 
Controls every single sound effect in the game. Includes track path, designating the track as background, min/max volume, pitch, whether the track needs to be looped, and various playback delay/cut-off manipulations
###### [tutorial.csv](/csv/csv_client/tutorial.csv "tutorial.csv") 
Parameters for how the tutorial with Shelly should run (when logging in for the first time without an account). Gets ignored in Null's Brawl


# csv-logic
Files that set the behavior of both the client and the server. This means not all are subject to modification, either partially or completely.

###### [accessories.csv](/csv/csv_logic/accessories.csv "accessories.csv") 
Characteristics of every gadget in the game
###### [ad_placements.csv](/csv/csv_logic/ad_placements.csv "ad_placements.csv") 🪦
The never released "watch an ad for an extra reward", and is unlikely ever to. Provides zero interest for modding
###### [alliance_badges.csv](/csv/csv_logic/alliance_badges.csv "alliance_badges.csv") 
Lists clan emblems from ui.sc
###### [alliance_league_modes.csv](/csv/csv_logic/alliance_league_modes.csv "alliance_league_modes.csv") 🪦 👻
Old file from the days of gold ticket clan wars, makes clan emblem replacement when status is Competitive
###### [alliance_league_ranks.csv](/csv/csv_logic/alliance_league_ranks.csv "alliance_league_ranks.csv") 🪦 👻 
Same old file, responsible for club ranks
###### [alliance_roles.csv](/csv/csv_logic/alliance_roles.csv "alliance_roles.csv") 
Positions in the club, from Member to President
###### [area_effects.csv](/csv/csv_logic/area_effects.csv "area_effects.csv") 
Characteristics of various area effects that can be created both by brawlers (like fire on the ground from Brock's rockets, spilled beer from Barley, etc.) and by the game itself (respawning, healing, robots, etc.).
###### [battle_feats.csv](/csv/csv_logic/battle_feats.csv "battle_feats.csv") 
Sets the player medals' (for highest kills, damage or healing) gradient variant and TID from localization files
###### [bosses.csv](/csv/csv_logic/bosses.csv "bosses.csv") 🪦 👻 
Boss levels either from Boss Fight or Super City Rampage, it's not clear at all... Contains parameters of 7 bosses, for each of them there is a reward of 10 gems. Might as well be cut content from Project Lazer days.
###### [campaign.csv](/csv/csv_logic/campaign.csv "campaign.csv") 🪦 👻 
Presumably cut content from the days of Project Lazer. A reward of 3 crystals is given for each completion of a campaign stage
###### [cards.csv](/csv/csv_logic/cards.csv "cards.csv") 
Info cards on brawlers and their gadgets, starpowers, hypercharges, attacks, supers, and pets (turrets, minions, alternate forms, etc.)
###### [carryables.csv](/csv/csv_logic/carryables.csv "carryables.csv") 
Parameters of all items that can be picked up and carried (like balls)
###### [catalog_collections.csv](/csv/csv_logic/catalog_collections.csv "catalog_collections.csv") 
Manages the sections in the catalog of cosmetics (skins, avatars, pins and sprays) in the shop
###### [challenges.csv](/csv/csv_logic/challenges.csv "challenges.csv") 
Time-limited championships (those with a limited number of defeats)
###### [character_components_logic.csv](/csv/csv_logic/character_components_logic.csv "character_components_logic.csv") 👻 
…
###### [characters.csv](/csv/csv_logic/characters.csv "characters.csv") 
Characteristics of the brawlers themselves. Useful for finding out who's hiding under which codename (for example, Poco's codename is DeadMariarchi)
###### [chronos_asset_ids.csv](/csv/csv_logic/chronos_asset_ids.csv "chronos_asset_ids.csv") 🪦 👻 
Some kind of a hack for megapig
###### [class_archetypes.csv](/csv/csv_logic/class_archetypes.csv "class_archetypes.csv") 
Lists brawlers' classes (tanks, assassins, artillery, etc.)
###### [club_piggy_levels.csv](/csv/csv_logic/club_piggy_levels.csv "club_piggy_levels.csv") 
The levels of completeness of the megapig
###### [club_piggy_types.csv](/csv/csv_logic/club_piggy_types.csv "club_piggy_types.csv") 
Alternative skins of the megapig
###### [club_piggy_wins.csv](/csv/csv_logic/club_piggy_wins.csv "club_piggy_wins.csv") 
Sets the level of the megapig by the number of club wins
###### [collab_game_modes.csv](/csv/csv_logic/collab_game_modes.csv "collab_game_modes.csv") 👻 
Temporal collab modes with leaderboards or a kind of progression
###### [collabs.csv](/csv/csv_logic/collabs.csv "collabs.csv") 👻 
All the collabs in the game's history and the cosmetics from them
###### [competitive_pass_tiers.csv](/csv/csv_logic/competitive_pass_tiers.csv) 👻
…
###### [contest_types.csv](/csv/csv_logic/contest_types.csv "contest_types.csv") 👻
…
###### [emote_bundles.csv](/csv/csv_logic/emote_bundles.csv "emote_bundles.csv") 
Lists collections of pins
###### [emotes.csv](/csv/csv_logic/emotes.csv "emotes.csv") 
Parameters of all pins in the game
###### [enumerated_id_lists.csv](/csv/csv_logic/enumerated_id_lists.csv "enumerated_id_lists.csv") 👻
…
###### [event_modifiers.csv](/csv/csv_logic/event_modifiers.csv "event_modifiers.csv") 👻
…
###### [event_slots.csv](/csv/csv_logic/event_slots.csv "event_slots.csv") 👻
Responsible for the various slots in the mode rotation (e.g. random - Mystery mode)
###### [game_mode_variations.csv](/csv/csv_logic/game_mode_variations.csv "game_mode_variations.csv") 
Parameters of all modes in the game
###### [gear_boosts.csv](/csv/csv_logic/gear_boosts.csv "gear_boosts.csv") 
Parameters of all gears in the game
###### [gear_levels.csv](/csv/csv_logic/gear_levels.csv "gear_levels.csv") 🪦
Gear levels, a deprecated mechanic
###### [gear_rarities.csv](/csv/csv_logic/gear_rarities.csv "gear_rarities.csv") 
Gear rarities (blue, purple and red)
###### [globals.csv](/csv/csv_logic/globals.csv "globals.csv") 
Global settings for various parameters
###### [intro_flows.csv](/csv/csv_logic/intro_flows.csv "intro_flows.csv") 
Screens that may appear immediately after loading the game (New Year's megapig and season resets)
###### [items.csv](/csv/csv_logic/items.csv "items.csv")
The parameters of the so-called items that appear either from brawlers (bombs from Piper's super, Griff's explosive piggy bank, Gray's portals, etc.), from the map itself (jump pads, power cube boxes, teleporters, etc.), or directly from the player (sprays). In addition to physical items, the table also mentions visual items (regeneration, acceleration, energy effects, etc.)
###### [locales.csv](/csv/csv_logic/locales.csv "locales.csv") 
Parameters of game languages and unique settings for them (mainly changing links to display content in different languages)
###### [location_themes.csv](/csv/csv_logic/location_themes.csv "location_themes.csv") 
All map environments in the game. The environments themselves are stored in separate SCW and GLB files, and their thumbnails (animations under the name of the mode and map) - in a single events.sc
###### [locations.csv](/csv/csv_logic/locations.csv "locations.csv") 
Lists all maps pre-installed in the game
###### [map_templates.csv](/csv/csv_logic/map_templates.csv "map_templates.csv") 
Initial states when creating a new map in the map creator in the form of ASCII-arts
###### [maps.csv](/csv/csv_logic/maps.csv "maps.csv") 🧊 
All the preset maps in the game in the form of ASCII-arts in one big table (responsible for both map and preview)
###### [mastery_hero_confs.csv](/csv/csv_logic/mastery_hero_confs.csv "mastery_hero_confs.csv") 
Lists the brawler's masteries and which unique rewards will be on the way (pin and avatar)
###### [mastery_levels.csv](/csv/csv_logic/mastery_levels.csv "mastery_levels.csv") 
The rewards of mastery path themselves
###### [mastery_points.csv](/csv/csv_logic/mastery_points.csv "mastery_points.csv") 👻 
…
###### [mastery_reward_types.csv](/csv/csv_logic/mastery_reward_types.csv "mastery_reward_types.csv") 
Types of rewards on the mastery path
###### [messages.csv](/csv/csv_logic/messages.csv "messages.csv") 
Quick chat messages and some pins anchored at the very top of the list
###### [milestones.csv](/csv/csv_logic/milestones.csv "milestones.csv") 
Huge table of intervals of all possible "paths"
###### [mutation_components.csv](/csv/csv_logic/mutation_components.csv "mutation_components.csv") 👻
…
###### [name_colors.csv](/csv/csv_logic/name_colors.csv "name_colors.csv") 
Player name colors
###### [night_market_bundles.csv](/csv/csv_logic/night_market_bundles.csv "night_market_bundles.csv") 👻 
…
###### [night_market_items.csv](/csv/csv_logic/night_market_items.csv "night_market_items.csv") 👻 
…
###### [player_frames.csv](/csv/csv_logic/player_frames.csv "player_frames.csv") 
Lists the frames of the battle card (either Ranked or Fame)
###### [player_map_environments.csv](/csv/csv_logic/player_map_environments.csv "player_map_environments.csv") 
Manages the available themes in Map Maker (as well as, apparently, the maps themselves)
###### [player_thumbnails.csv](/csv/csv_logic/player_thumbnails.csv "player_thumbnails.csv") 
Manages player avatars taken from player_icons.sc
###### [player_titles.csv](/csv/csv_logic/player_titles.csv "player_titles.csv") 
Sets gradient variant (BP/BP+) and TID from localization files for player titles
###### [pricepoints.csv](/csv/csv_logic/pricepoints.csv) 👻
…
###### [progression_skin_details.csv](/csv/csv_logic/progression_skin_details.csv) 👻
…
###### [projectiles.csv](/csv/csv_logic/projectiles.csv "projectiles.csv") 🧊
All characteristics of all attacks of all brawlers. The textures themselves are taken from effects.sc, effects_brawler.sc and effects_brawler2.sc
###### [random_reward_containers.csv](/csv/csv_logic/random_reward_containers.csv "random_reward_containers.csv")
Parameters for all possible boxes and drops, as well as the megapig and Godzilla's eggs
###### [random_rewards.csv](/csv/csv_logic/random_rewards.csv "random_rewards.csv") 
Parameters of all random rewards
###### [ranked_locations.csv](/csv/csv_logic/ranked_locations.csv "ranked_locations.csv") 
Maps in ranked battles
###### [ranked_ranks.csv](/csv/csv_logic/ranked_ranks.csv "ranked_ranks.csv") 
Parameters of ranked leagues
###### [ranked_star_rewards.csv](/csv/csv_logic/ranked_star_rewards.csv "ranked_star_rewards.csv")
Possible awards from the ranked drop for each season
###### [record_levels.csv](/csv/csv_logic/record_levels.csv "record_levels.csv") 👻 
…
###### [records.csv](/csv/csv_logic/records.csv "records.csv") 👻 
…
###### [regions.csv](/csv/csv_logic/regions.csv "regions.csv") 
Lists geolocations (countries/regions) from the corresponding button in the settings
###### [resources.csv](/csv/csv_logic/resources.csv "resources.csv") 
In-game currencies (coins, gems, blings, etc.)
###### [seasonal_skin_sections.csv](/csv/csv_logic/seasonal_skin_sections.csv "seasonal_skin_sections.csv") 👻
Manages the skin category suggestions in the shop
###### [shop_panel_layouts.csv](/csv/csv_logic/shop_panel_layouts.csv "shop_panel_layouts.csv") 👻 
Once again controls some kind of offer in the shop
###### [shop_style_sets.csv](/csv/csv_logic/shop_style_sets.csv "shop_style_sets.csv") 👻 
Some other file that manages the offers in the shop
###### [skills.csv](/csv/csv_logic/skills.csv "skills.csv") 
Characteristics of brawlers' attacks and supers
###### [skin_albums.csv](/csv/csv_logic/skin_albums.csv "skin_albums.csv") 👻
…
###### [skin_anim_sequences.csv](/csv/csv_logic/skin_anim_sequences.csv "skin_anim_sequences.csv") 👻
Judging by the name it should control the order of skin animations, but since the file has only 1 line with Mortis there is an assumption that this is just a hack.
###### [skin_campaigns.csv](/csv/csv_logic/skin_campaigns.csv "skin_campaigns.csv") 
Skin category parameters
###### [skin_confs.csv](/csv/csv_logic/skin_confs.csv "skin_confs.csv") 🧊 
Contains extremely extensive (about 200 columns!) parameters of all skins (including standard ones), models with textures and animations taken from various SCW and GLB files.
###### [skin_rarities.csv](/csv/csv_logic/skin_rarities.csv "skin_rarities.csv") 
Average prices of skins by rarities 
###### [skins.csv](/csv/csv_logic/skins.csv "skins.csv") 
Manages data of all skins and base models and textures from various SCTX files. Data includes skins prices, categories, rarities, discounts and more
###### [sprays.csv](/csv/csv_logic/sprays.csv "sprays.csv") 
Parameters of all sprays in the game, taken from individual PNG images and paint particles from sprays.sc
###### [status_effects.csv](/csv/csv_logic/status_effects.csv "status_effects.csv") 
Characterizes all buffs and debuffs (shields, burning, sliding, poisoning, hypnosis, stun, etc).
###### [string_replacement.csv](/csv/csv_logic/string_replacement.csv) 👻
…
###### [themes.csv](/csv/csv_logic/themes.csv "themes.csv") 
Controls the backgrounds in the main menu, taken from background_\*.sc.
###### [tiles.csv](/csv/csv_logic/tiles.csv "tiles.csv") 
Characterizes all blocks (tiles) in the game
###### [traits.csv](/csv/csv_logic/traits.csv "traits.csv") 👻 
…
###### [trophy_season_reward_levels.csv](/csv/csv_logic/trophy_season_reward_levels.csv "trophy_season_reward_levels.csv") 
Lists the levels of the seasonal boxes
###### [trophy_world_milestones.csv](/csv/csv_logic/trophy_world_milestones.csv "trophy_world_milestones.csv") 👻 
…
###### [trophy_world_parts.csv](/csv/csv_logic/trophy_world_parts.csv "trophy_world_parts.csv") 👻 
…
###### [trophy_worlds.csv](/csv/csv_logic/trophy_worlds.csv "trophy_worlds.csv") 👻 
…
###### [visual_offer_groupings.csv](/csv/csv_logic/visual_offer_groupings.csv "visual_offer_groupings.csv") 👻 
Offer to buy hypercharge in the store
 
# localization
Localization files. It is recommended to modify only [texts_patch.csv](/csv/localization/texts_patch.csv "texts_patch.csv"), as the game will take longer to load when modifying the other files. It is enough to set it the existing TIDs and languages in other files, for which the replacement is needed
###### [ar.csv](/csv/localization/ar.csv "ar.csv") 🧊
Arabic (العربية)
###### [cn.csv](/csv/localization/cn.csv "cn.csv") 🧊
Chinese Simplified (简体中文)
###### [cnt.csv](/csv/localization/cnt.csv "cnt.csv") 🧊
Chinese Traditional (繁體中文)
###### [de.csv](/csv/localization/de.csv "de.csv") 🧊
German (Deutsch)
###### [es.csv](/csv/localization/es.csv "es.csv") 🧊
Spanish (Español)
###### [fi.csv](/csv/localization/fi.csv "fi.csv") 🧊
Finnish (Suomi)
###### [fr.csv](/csv/localization/fr.csv "fr.csv") 🧊
French (Français)
###### [he.csv](/csv/localization/he.csv "he.csv") 🧊
Hebrew (עברית)
###### [id.csv](/csv/localization/id.csv "id.csv") 🧊
Indonesian (Bahasa Indonesia)
###### [it.csv](/csv/localization/it.csv "it.csv") 🧊
Italian (Italiano)
###### [jp.csv](/csv/localization/jp.csv "jp.csv") 🧊
Japanese (日本語)
###### [kr.csv](/csv/localization/kr.csv "kr.csv") 🧊
Korean (한국어)
###### [ms.csv](/csv/localization/ms.csv "ms.csv") 🧊
Malay (Bahasa Melayu)
###### [nl.csv](/csv/localization/nl.csv "nl.csv") 🧊
Нидерландский (Nederlands)
###### [pl.csv](/csv/localization/pl.csv "pl.csv") 🧊
Polish (Polski)
###### [pt.csv](/csv/localization/pt.csv "pt.csv") 🧊
Portugal (Português)
###### [ru.csv](/csv/localization/ru.csv "ru.csv") 🧊
Russian (Русский)
###### [texts.csv](/csv/localization/texts.csv "texts.csv") 🧊
English (yes, exactly)
###### [texts_patch.csv](/csv/localization/texts_patch.csv) 
A universal file for swapping TIDs directly for all languages
###### [th.csv](/csv/localization/th.csv "th.csv") 🧊
Thai (ภาษาไทย)
###### [tr.csv](/csv/localization/tr.csv "tr.csv") 🧊
Turkish (Türkçe)
###### [vi.csv](/csv/localization/vi.csv "vi.csv") 🧊
Vietnamese (Tiếng Việt)
