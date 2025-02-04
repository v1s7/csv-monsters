<sup>v0.1 – написал v1s7</sup> 

[Switch to English](https://github.com/v1s7/csv-monsters/tree/main/FILETYPESen.md)

> [!TIP] 
> Содержание этого списка можно открыть, нажав на кнопку ⋮☰ в правом верхнем углу.

> [!NOTE] 
> Перед началом чтения рекомендуется прочесть [мануал](https://github.com/v1s7/csv-monsters/tree/main/MANUAL.md).

-----
# csv-client
Файлы, задающие поведение на стороне клиента, то есть полностью подлежащие модификации.

###### [animations.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_client/animations.csv "animations.csv") 
<!--"Name","FileName","StartFrame","EndFrame","FaceFreezeFrame","Speed","TransitionInMs","TransitionOutMs","AutoFadeMs","Looping","Priority"-->
Управляет всеми анимациями бравлеров и скинов. Включает в себя начало/конец анимаций, их скорость, переходы, цикличность и приоритет воспроизведения
###### [availability_window.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_client/availability_window.csv "availability_window.csv") 
Отвечает за доступность скинов за ограниченное время или сезонное (соответствующий значок под скинами)
###### [billing_packages.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_client/billing_packages.csv "billing_packages.csv") 
Все донатные акции магазина, то есть за реальные деньги. В Null's Brawl игнорируется
###### [bp_purchase_popup.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_client/bp_purchase_popup.csv "bp_purchase_popup.csv") 
Анимация покупки Brawl Pass, а также анимации пинов и скинов из него
###### [client_globals.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_client/client_globals.csv "client_globals.csv") 
Разнообразные настройки глобального клиента
###### [color_gradients.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_client/color_gradients.csv "color_gradients.csv") – 👻 
###### [credits.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_client/credits.csv "credits.csv") 
Перечисление разработчиков, которые участвовали в развитии игры. Находится в соответствующей кнопке в настройках игры
###### [effects.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_client/effects.csv "effects.csv") 
Перечисляет все визуальные эффекты в игре (а их в ней немало)
###### [faces.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_client/faces.csv "faces.csv") 
Перечисляет базовые анимации бравлеров и их скинов из characters.sc, а именно при победе, поражении и бездействии
###### [fame_tiers.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_client/fame_tiers.csv "fame_tiers.csv") 
Этапы кредитной славы и всё с ними связанное
###### [health_bars.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_client/health_bars.csv "health_bars.csv") 
Столбцы, которые показывают ОЗ игроков и NPC (роботов)
###### [hints.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_client/hints.csv "hints.csv") 
Подсказки от Шелли (в ранних стадиях игры), советы при подборе игроков и прочие рекомендации
###### [local_notifications.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_client/local_notifications.csv "local_notifications.csv") 
Push-уведомления игры (те, что отправляются за её пределами)
###### [location_features.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_client/location_features.csv "location_features.csv") 
Вносит изменения в окружения карт при соответствии определённым условиям (к примеру, скрытие Тары с фона базара, если её взяли в матче)
###### [login_calendar_items.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_client/login_calendar_items.csv "login_calendar_items.csv") – 👻 
###### [music.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_client/music.csv "music.csv") 
Управляет всей музыкой в игре. Включает в себя путь к треку, обозначение трека как фонового, запасной вариант для воспроизведения, громкость, требуется ли бесконечно зациклить трек или сколько раз это требуется сделать
###### [particle_emitters.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_client/particle_emitters.csv "particle_emitters.csv")
Управляет вообще всеми частицами в игре, их исходниками из effects.sc и имеет много различных параметров
###### [shop_items.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_client/shop_items.csv "shop_items.csv") 
Все возможные предметы в магазине. В Null's Brawl игнорируется
###### [sounds.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_client/sounds.csv "sounds.csv") 
Управляет вообще всеми звуковыми эффектами в игре. Включает в себя путь к треку, обозначение трека как фонового, мин./макс. громкость, тон, требуется ли зациклить трек, и различные махинации с задержками/обрывами воспроизведения
###### [tutorial.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_client/tutorial.csv "tutorial.csv") 
Параметры того, как должно проходить обучение с Шелли (при захоже в игру в первый раз без аккаунта)


# csv-logic
Файлы, задающие поведение и клиента, и сервера. А это значит, что не все подлежат модификации, либо частично либо полностью.

###### [accessories.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/accessories.csv "accessories.csv") – 👻 
###### [ad_placements.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/ad_placements.csv "ad_placements.csv") – 👻 
###### [alliance_badges.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/alliance_badges.csv "alliance_badges.csv") – 👻 
###### [alliance_league_modes.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/alliance_league_modes.csv "alliance_league_modes.csv") – 👻 
###### [alliance_league_ranks.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/alliance_league_ranks.csv "alliance_league_ranks.csv") – 👻 
###### [alliance_roles.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/alliance_roles.csv "alliance_roles.csv") – 👻 
###### [area_effects.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/area_effects.csv "area_effects.csv") – 👻 
###### [battle_feats.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/battle_feats.csv "battle_feats.csv") – 👻 
###### [bosses.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/bosses.csv "bosses.csv") – 👻 
###### [campaign.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/campaign.csv "campaign.csv") – 👻 
###### [cards.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/cards.csv "cards.csv") – 👻 
###### [carryables.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/carryables.csv "carryables.csv") – 👻 
###### [catalog_collections.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/catalog_collections.csv "catalog_collections.csv") – 👻 
###### [challenges.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/challenges.csv "challenges.csv") – 👻 
###### [characters.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/characters.csv "characters.csv") – 👻 
###### [chronos_asset_ids.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/chronos_asset_ids.csv "chronos_asset_ids.csv") – 👻 
###### [class_archetypes.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/class_archetypes.csv "class_archetypes.csv") – 👻 
###### [club_piggy_levels.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/club_piggy_levels.csv "club_piggy_levels.csv") – 👻 
###### [club_piggy_types.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/club_piggy_types.csv "club_piggy_types.csv") – 👻 
###### [club_piggy_wins.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/club_piggy_wins.csv "club_piggy_wins.csv") – 👻 
###### [collab_game_modes.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/collab_game_modes.csv "collab_game_modes.csv") – 👻 
###### [collabs.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/collabs.csv "collabs.csv") – 👻 
###### [emote_bundles.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/emote_bundles.csv "emote_bundles.csv") – 👻 
###### [emotes.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/emotes.csv "emotes.csv") – 👻 
###### [enumerated_id_lists.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/enumerated_id_lists.csv "enumerated_id_lists.csv") – 👻 
###### [event_slots.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/event_slots.csv "event_slots.csv") – 👻 
###### [game_mode_variations.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/game_mode_variations.csv "game_mode_variations.csv") – 👻 
###### [gear_boosts.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/gear_boosts.csv "gear_boosts.csv") – 👻 
###### [gear_levels.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/gear_levels.csv "gear_levels.csv") – 👻 
###### [gear_rarities.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/gear_rarities.csv "gear_rarities.csv") – 👻 
###### [globals.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/globals.csv "globals.csv") – 👻 
###### [intro_flows.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/intro_flows.csv "intro_flows.csv") – 👻 
###### [items.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/items.csv "items.csv") – 👻 
###### [locales.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/locales.csv "locales.csv") – 👻 
###### [location_themes.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/location_themes.csv "location_themes.csv") – 👻 
###### [locations.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/locations.csv "locations.csv") – 👻 
###### [map_templates.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/map_templates.csv "map_templates.csv") – 👻 
###### [maps.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/maps.csv "maps.csv") – 👻 
###### [mastery_hero_confs.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/mastery_hero_confs.csv "mastery_hero_confs.csv") – 👻 
###### [mastery_levels.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/mastery_levels.csv "mastery_levels.csv") – 👻 
###### [mastery_points.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/mastery_points.csv "mastery_points.csv") – 👻 
###### [mastery_reward_types.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/mastery_reward_types.csv "mastery_reward_types.csv") – 👻 
###### [messages.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/messages.csv "messages.csv") – 👻 
###### [milestones.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/milestones.csv "milestones.csv") – 👻 
###### [name_colors.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/name_colors.csv "name_colors.csv") – 👻 
###### [night_market_bundles.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/night_market_bundles.csv "night_market_bundles.csv") – 👻 
###### [night_market_items.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/night_market_items.csv "night_market_items.csv") – 👻 
###### [player_frames.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/player_frames.csv "player_frames.csv") – 👻 
###### [player_map_environments.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/player_map_environments.csv "player_map_environments.csv") – 👻 
###### [player_thumbnails.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/player_thumbnails.csv "player_thumbnails.csv") – 👻 
###### [player_titles.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/player_titles.csv "player_titles.csv") – 👻 
###### [projectiles.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/projectiles.csv "projectiles.csv") – 👻 
###### [random_reward_containers.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/random_reward_containers.csv "random_reward_containers.csv") – 👻 
###### [random_rewards.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/random_rewards.csv "random_rewards.csv") – 👻 
###### [ranked_locations.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/ranked_locations.csv "ranked_locations.csv") – 👻 
###### [ranked_ranks.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/ranked_ranks.csv "ranked_ranks.csv") – 👻 
###### [ranked_star_rewards.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/ranked_star_rewards.csv "ranked_star_rewards.csv") – 👻 
###### [regions.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/regions.csv "regions.csv") – 👻 
###### [resources.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/resources.csv "resources.csv") – 👻 
###### [seasonal_skin_sections.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/seasonal_skin_sections.csv "seasonal_skin_sections.csv") – 👻 
###### [shop_panel_layouts.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/shop_panel_layouts.csv "shop_panel_layouts.csv") – 👻 
###### [shop_style_sets.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/shop_style_sets.csv "shop_style_sets.csv") – 👻 
###### [skills.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/skills.csv "skills.csv") – 👻 
###### [skin_anim_sequences.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/skin_anim_sequences.csv "skin_anim_sequences.csv") – 👻 
###### [skin_campaigns.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/skin_campaigns.csv "skin_campaigns.csv") – 👻 
###### [skin_confs.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/skin_confs.csv "skin_confs.csv") – 👻 
###### [skin_rarities.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/skin_rarities.csv "skin_rarities.csv") – 👻 
###### [skins.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/skins.csv "skins.csv") – 👻 
###### [sprays.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/sprays.csv "sprays.csv") – 👻 
###### [status_effects.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/status_effects.csv "status_effects.csv") – 👻 
###### [themes.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/themes.csv "themes.csv") – 👻 
###### [tiles.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/tiles.csv "tiles.csv") – 👻 
###### [trophy_season_reward_levels.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/trophy_season_reward_levels.csv "trophy_season_reward_levels.csv") – 👻 
###### [visual_offer_groupings.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/csv_logic/visual_offer_groupings.csv "visual_offer_groupings.csv") – 👻 
 
# localization
Файлы локализаций. Рекомендуется модифицировать только [texts_patch.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/localization/texts_patch.csv "texts_patch.csv"), так как игра будет дольше загружаться при модификации остальных файлов. Достаточно задать ему существующие в других файлах TID и языки, на которых нужна замена.
###### [ar.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/localization/ar.csv "ar.csv") 
Арабский (العربية)
###### [cn.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/localization/cn.csv "cn.csv") 
Китайский упрощённый (简体中文)
###### [cnt.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/localization/cnt.csv "cnt.csv") 
Китайский традиционный (繁體中文)
###### [de.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/localization/de.csv "de.csv") 
Немецкий (Deutsch)
###### [es.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/localization/es.csv "es.csv") 
Испанский (Español)
###### [fi.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/localization/fi.csv "fi.csv") 
Финский (Suomi)
###### [fr.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/localization/fr.csv "fr.csv")
Французский (Français)
###### [he.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/localization/he.csv "he.csv") 
Иврит (עברית)
###### [id.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/localization/id.csv "id.csv")
Индонезийский (Bahasa Indonesia)
###### [it.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/localization/it.csv "it.csv") 
Итальянский (Italiano)
###### [jp.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/localization/jp.csv "jp.csv") 
Японский (日本語)
###### [kr.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/localization/kr.csv "kr.csv") 
Корейский (한국어)
###### [ms.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/localization/ms.csv "ms.csv") 
Малайский (Bahasa Melayu)
###### [nl.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/localization/nl.csv "nl.csv") 
Нидерландский (Nederlands)
###### [pl.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/localization/pl.csv "pl.csv") 
Польский (Polski)
###### [pt.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/localization/pt.csv "pt.csv")
Португальский (Português)
###### [ru.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/localization/ru.csv "ru.csv") 
Русский (да, именно он)
###### [texts.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/localization/texts.csv "texts.csv") 
Английский (English)
###### [texts_patch.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/localization/texts_patch.csv)
Универсальный файл для замены TID непосредственно на все языки
###### [th.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/localization/th.csv "th.csv")
Тайский (ภาษาไทย)
###### [tr.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/localization/tr.csv "tr.csv") 
Турецкий (Türkçe)
###### [vi.csv](https://github.com/v1s7/csv-monsters/blob/main/csv/localization/vi.csv "vi.csv") 
Вьетнамский (Tiếng Việt)
