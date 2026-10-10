# Fonctions et déclencheurs — Fallen Gateways / Les Portes Déchues

**119 fichiers de fonctions Minecraft** trouvés dans la variante `1.21-26.3`.

Il s'agit d'un audit statique des instructions présentes, **pas d'un test du comportement en jeu**. Les fonctions peuvent être appelées conditionnellement ou jamais.

## Fonctions clés répertoriées

| Fichier | Commandes non-commentaires |
| --- | ---: |

| `data/bns/function/init/load.mcfunction` | 22 |

| `data/bns/function/init/tick.mcfunction` | 34 |

| `data/bns/function/build/overworld_portal_village_cluster.mcfunction` | 19 |

| `data/bns/function/build/overworld_portal_village_cluster_alt.mcfunction` | 4 |

| `data/bns/function/quest/final_reward.mcfunction` | 4 |

| `data/bns/function/quest/progress_broadcast.mcfunction` | 1 |

## Objectifs scoreboard déclarés

| Valeur observée | Occurrences textuelles |
| --- | ---: |

| `bns_tick` | 1 |

| `bns_anchor` | 1 |

| `bns_books` | 1 |

| `bns_invasion` | 1 |

| `bns_lang` | 1 |

| `bns_language` | 1 |

## Créatures mentionnées par des commandes summon

| Valeur observée | Occurrences textuelles |
| --- | ---: |

| `minecraft:piglin` | 12 |

| `minecraft:hoglin` | 10 |

| `minecraft:piglin_brute` | 9 |

| `minecraft:wither_skeleton` | 6 |

| `minecraft:blaze` | 5 |

| `minecraft:magma_cube` | 4 |

| `minecraft:zombified_piglin` | 4 |

| `minecraft:ghast` | 3 |

| `minecraft:zoglin` | 3 |

| `minecraft:pig` | 2 |

| `minecraft:allay` | 2 |

| `minecraft:vex` | 2 |

| `minecraft:strider` | 2 |

| `minecraft:marker` | 1 |

## Principaux mots d'instruction

| Valeur observée | Occurrences textuelles |
| --- | ---: |

| `fill` | 1194 |

| `setblock` | 185 |

| `execute` | 140 |

| `tellraw` | 69 |

| `summon` | 64 |

| `scoreboard` | 41 |

| `tag` | 20 |

| `function` | 19 |

| `bossbar` | 17 |

| `give` | 13 |

| `experience` | 13 |

| `effect` | 6 |

| `data` | 1 |

| `kill` | 1 |

| `forceload` | 1 |

## Principaux appels de fonction

| Valeur observée | Occurrences textuelles |
| --- | ---: |

| `bns:quest/final_reward` | 12 |

| `bns:summon/vaerok_guard` | 4 |

| `bns:language/prompt` | 3 |

| `bns:quest/found_aelys` | 2 |

| `bns:quest/found_end` | 2 |

| `bns:quest/found_factions` | 2 |

| `bns:quest/found_livestock` | 2 |

| `bns:quest/found_mobs` | 2 |

| `bns:quest/found_nerath` | 2 |

| `bns:quest/found_phantoms` | 2 |

| `bns:quest/found_portes` | 2 |

| `bns:quest/found_umbraeviel` | 2 |

| `bns:quest/found_voyages` | 2 |

| `bns:quest/found_warden_origin` | 2 |

| `bns:quest/found_warden_player` | 2 |

| `bns:build/deepdark_sealed_library` | 2 |

| `bns:build/deepdark_watch_chamber` | 2 |

| `bns:build/deepdark_forbidden_district` | 2 |

| `bns:build/deepdark_living_matter_vault` | 2 |

| `bns:summon/vaerok_brute` | 2 |

| `bns:build/nether_colony_storehouse` | 2 |

| `bns:build/nether_colony_aqueduct` | 2 |

| `bns:build/nether_support_network` | 2 |

| `bns:build/nether_evacuation_bridge` | 2 |

| `bns:build/nether_ruin_outpost` | 2 |

| `bns:build/nether_support_anchor` | 2 |

| `bns:build/overworld_gate_metropolis` | 2 |

| `bns:build/overworld_ancient_road` | 2 |

| `bns:build/overworld_walled_village` | 2 |

| `bns:invasion/find_site` | 2 |

| `bns:invasion/refresh_max` | 2 |

| `bns:invasion/wave/one` | 2 |

| `bns:build/deepdark_seal` | 1 |

| `bns:build/deepdark_experiment_hall` | 1 |

| `bns:build/deepdark_vex_foundry` | 1 |

## Extraits représentatifs (2 lignes au plus par fonction)

### `data/bns/function/init/load.mcfunction`

    scoreboard objectives add bns_tick dummy
    scoreboard objectives add bns_anchor dummy

### `data/bns/function/init/tick.mcfunction`

    scoreboard players add #timer bns_tick 1
    scoreboard players add #timer bns_invasion 1

### `data/bns/function/build/overworld_portal_village_cluster.mcfunction`

    function bns:build/overworld_walled_village
    fill ~-22 ~1 ~40 ~-8 ~6 ~52 minecraft:oak_planks

### `data/bns/function/build/overworld_portal_village_cluster_alt.mcfunction`

    function bns:build/overworld_walled_village
    execute positioned ~18 ~ ~10 run function bns:build/overworld_shrine_waystop

### `data/bns/function/quest/final_reward.mcfunction`

    tag @s add bns_story_complete
    tellraw @s [{"text":"[Quete] ","color":"gold"},{"text":"Collection completee : Sur les traces d'une ancienne civilisation","color":"yellow"}]

### `data/bns/function/quest/progress_broadcast.mcfunction`

    execute as @a run tellraw @s [{"text":"[Quete] ","color":"gold"},{"text":"Sur les traces d'une ancienne civilisation : ","color":"yellow"},{"score":{"name":"@s","objective":"bns_books"},"color":"yellow"},{"text":" / 12",

**Note :** le nombre de fonctions ne dit rien à lui seul de la fréquence des événements. Pour conclure sur un compteur ou un délai, il faut suivre les déclencheurs réels, les valeurs et les conditions d'exécution.

[Retour](../README.md)
