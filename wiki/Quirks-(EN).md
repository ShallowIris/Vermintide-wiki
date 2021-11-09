- [Disease](#disease)
- [Positive Quirks](#positive-quirks)
- [Negative Quirks](#negative-quirks)

Vanilla Random Quirks: 164, Pos 65, Neg 76, Dis 23 (Base Chance 1)
CoM Random Quirks: 22, Pos 11, Neg 9, Dis 2 (Base Chance 1)

=> Pos Base Chance 76, Neg Base Chance 85, Dis Base Chance 25

# Warpstone Addiction (WSA)

![](https://cdn.discordapp.com/attachments/876891269773787176/877562019291742318/unknown.png)

If infected, start from Exposed (Stage 2)

* Stage 1 - Radiating
* Stage 1' - Warped
* Stage 2 - Exposed
* Stage 2' - Enlaced
* Stage 3 - Corrupted

## Warpstone

* act_out_consume_priority = 1

### Loot table

1) Warp-Engineered monsters - It should be as frequent as 2 warpstones per 30 rds, considering how many of them are in mashes
2) Doomwheel and Warpstone Ore curios
3) By activating Warpstone Architecture in 'Activate' missions

### Effect without Warpstone Addiction:
 
* Blight / Stun Chance +10% (3 rds), Stress +5
* No chance to catch WSA in 1st usage. If used for 2nd time in the same quest, 100% chance to catch WSA.

### Warped Effect: 
* +20 rds of duration, Blight / Stun Chance +10% (20 rds)

### Enlaced Effect: 
* +20 rds of duration, DMG +15% (20 rds)

### Radiating Effect: 
* Evolve to Warped

### Exposed Effect: 
* Evolve to Enlaced

### Corrupted Effect: 
* Evolve to Exposed

## How to get infected: 
1) Globadier, Warpfire Thrower, Ratling Gunner, Doomwheel Skills - 20% chance
2) Effect from Warpstone
3) Upon interacting with Warpstone Ore curio

## How to Cure:
1) Cures (a la CC) - Killing Plague Priest will give you 12 cures.

## Actout

### 1. Radiating:
1) Nothing - base chance 91
2) Upon turn start - party wide stress ("BarkStress") - base chance 3
3) Upon turn start - buff party (spd +1, blight resist -15%) - base chance 4
4) Upon turn start - consume warpstone (consume_item actout + highest consume priority of warpstone) - base chance 2

### 1'. Warped:
1) nothing - base chance 87
2) Upon turn start - party wide stress ("BarkStress") - base chance 3
3) Upon turn start - buff party (spd +2, blight 1 * 3rds (500% base)) - base chance 3
4) Upon turn start - buff self (Stress -10, HP DMG 3) - base chance 3
5) Upon turn start - attack ally (Max HP 5%, Stun 120%) - base chance 2
6) Upon turn start - buff one companion (spd +3, Acc +10) and afflict them with WSA - base chance 2
7) 115% chance to reject retreat

### 2. Exposed:
1) nothing - base chance 99
2) Upon turn start - consume warpstone - base chance 1

### 2'. Enlaced:
1) nothing - base chance 84
2) random command - base chance 4
3) Upon turn start - attack ally (Max HP 15%) - base chance 4
4) Upon turn start - buff self (stress -5, HP heal 3) - base chance 8
5) 15% chance to reject retreat

### 3. Corrupted:
1) nothing - base chance 69
2) Upon turn start - party wide stress - base chance 9
3) ignore command - base chance 3
4) random command - base chance 6
5) Upon turn start - self damage (Max HP 10%) - base chance 4
6) Upon turn start - attack ally (Max HP 15%) - base chance 4
7) Upon turn start - consume warpstone - base chance 5
8) Reject Heal, Buff, Camping Meal, Camp skill usage/receiving buff from camp skills - 33% chance
9) Forced interaction with Warpstone Ore and Doomwheel Curio - 17% chance

## Effects according to stage
| id                               | positive                                                                                      | negative                                                                                                                                                                                                                                                                            | imcompatible | duration   | 
| :------------------------------- | :-------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| :-------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| WSA - Radiating | `spd +1`<br/>`stun/blight chance +0.1`                                                                                      | `stress recv +0.15`<br/>`blight res -0.1`                                                                                                                                                                                                                                             |  CC <br/> Other WSAs <br/> Darkwraith, Pelagic<br/>Cryophilic (Mountain)  | 21 ~ 39 rds<br/>+100rds if not in vmt_mine   |
| WSA - Warped  | `spd +3`<br/>`stun +0.1`<br/>`blight +0.15`<br/>`bleed +0.15`<br/>`debuff +0.15` | `stress recv +0.15` <br/>`blight res -0.1`                                                                                                                                                                                                                                                                   |  CC <br/> Other WSAs <br/> Darkwraith, Pelagic<br/>Cryophilic (Mountain)   |  19 ~ 31 rds   |
| WSA - Exposed   |  `max hp +0.1`                                                                                        | `stress recv +0.15`<br/>`blight res -0.1`                                                                                                                                                                                                                               | CC <br/> Other WSAs <br/> Darkwraith, Pelagic<br/>Cryophilic (Mountain)  | 21 ~ 39 rds<br/>+100rds if not in vmt_mine    |
| WSA - Enlaced   |  `max hp +0.15`<br/>`spd +2`<br/>`dmg +0.1`                                                                                         | `stress recv +0.15`<br/>`blight res -0.1`                                                                                                                                                                                                                               | CC <br/> Other WSAs <br/> Darkwraith, Pelagic<br/>Cryophilic (Mountain)  |  19 ~ 31 rds    |
| WSA - Corrupted    |                                                                                               | `stress recv p +0.5`<br/>`resolve check p -0.2`<br/>`blight res -0.3`<br/>`max_hp p -0.2`<br/>`spd -4`                                                                                                                                                                              | CC <br/> Other WSAs <br/> Darkwraith, Pelagic<br/>Cryophilic (Mountain) |  indefinite    |

* 15 rds passes when in hamlet

# Disease

base chance 31

| id                               | positive                                                                                      | negative                                                                                                                                                                                                                                                                            | chance | imcompatible                                                                                                                                                                                                                    | misc |
| :------------------------------- | :-------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | :--- |
| Black Lung                       |                                                                                               | `spd -3 after 1st rounds`<br/>`crit -0.03 after 1st rounds`<br/>`dmg p -0.1 after 1st rounds`                                                                                                                                                                                       | 1      |                                                                                                                                                                                                                                 |      |
| Deep Burn                             |                                                                                               | `bleed/blight res -0.15`<br/>`bleed/blight dmgrecv +0.15`<br/>`disease res -0.25`                                                                                                                                                                                                                    | 1      |                                                                                                                                                                                                                                 |      |
| Chronic Fatigue                  |                                                                                               | `stress heal recv p -0.5 if idle`<br/>`stress heal recv p -0.5 in buildings` | 1      |                                                                                                                                                                                                                                 |      |
| Sudden Deafness               |                                                                                               | `move res & stun res -20%`<br/>`stress heal received from cry havoc/inspiring tunes -50%` | 1      | tended_deafness                                                                                                                                                                                                                               | `60rds duration`<br/>`60rds pass in hamlet`<br/>`After 60rds:`<br/>`evolve to Tended Deafness`     |
| Tended Deafness                  |                                                                                               | `move res & stun res -10%`<br/>`stress heal received from cry havoc/inspiring tunes -20%` | `60rds passed after catching tended_deafness`     |  sudden_deafness                                                                                                                                                                                                                               |      |
| Inflammable Pyrogenesis          | `torch increase p +0.4`                                                                       | `dmg recv p +0.33`                                                                                                                                                                                                                                                                  | 1      |                                                                                                                                                                                                                                 |      |
| Dancing Eyes                       |                                                                                               | `on attack: random target 20%`                                                                                                                                                                                                                                                                    | 1       |                                                                                                                                                                                                                                 |      |
| Yellow Skull Fever                       |                                                                                               | `max hp p -0.7`<br/>`heal received p -0.9`<br/>`blight resist -0.7`                                                                                                                                                                                                                                                                   | `catch from Plague Priest`       |                                                                                                                                                                                                                                 |      |
# Positive Quirks

base chance 86.4


| id                    | positive                                                                                                                        | negative                  | chance | imcompatible                                            | misc |
| :-------------------- | :------------------------------------------------------------------------------------------------------------------------------ | :------------------------ | :----- | :------------------------------------------------------ | :--- |
| Warp-Engineer   | `dmg p +0.10 vs warp engineered`<br/>`atk +0.05 vs rat`<br/>`trap res +0.15`                                                    |                           | 0.5<br/>`Can get from Doomwheel Curio`      |  Mechanophobia                                          |      |
| Strider         | `spd +3 in corridor`<br/>`spd +1 in room`                                                                                                                       | `move res -0.3`           | 0.75      | Bull-Step                                            |      |
| Standard-bearer      | `Upon turn start - 10% chance to stress heal companions (3)`<br/>`Upon companion dodging attack: 10% chance to stress heal companion (5)`<br/>`Upon companion landing attack: 10% chance to stress heal companion (5)`<br/>`Upon trap activating: 50% chance to stress heal companion (5)`                                                                                        |                           | 0.5      |                                                  |      |
| Yellow Canary              | `party surprise -0.1`<br/>`scouting +0.07`                                                                                      |                           | 0.4    |                                                         | Singleton     | 
| Cleanly               | `blight res +0.1`<br/>`blight res +0.1 if has holy water`<br/>`disease res +0.1`                                                                                        |                           | 0.75      | uncleanly                                               |      |
| Counterspell          | `debuff res +0.2`                                                                                                               |                           | 0.5<br/>`Can get from Skaven Totem curio`      | hexer                                                        | `500rds`<br/>`10rds pass in hamlet`<br/>`500 rds pass:`<br/>`Evolve to Hexer`     |
| Hexer          | `debuff res +0.2`<br/>`debuff chance +0.2`                                                                                                                |                           | `evolved from Counterspell`      |  counterspell                                                       |      |
| Dawnbringer           | `torch inc p +0.3`                                                                                                              |                           | 0.5      | "nocturnal"<br/>"sensitive_to_light"<br/>"phengophobia"<br/>"daybreaker" | `500rds`<br/>`10rds pass in hamlet`<br/>`500 rds pass:`<br/>`Evolve to Daybreaker`     |
| Daybreaker           | `torch inc p +0.3` `stun chance +0.1 if torch above 76`                                                                                                              |                           | `evolved from Dawnbringer`      | "nocturnal"<br/>"sensitive_to_light"<br/>"phengophobia"<br/>"dawnbringer" |      |
| Executioner           | `atk +0.07 vs hp below 0.5`<br/>`crit +0.07 vs hpbelow 0.5`                                                                       |                           | 0.75<br/>`Kill Slaverat/Clanrat/Stormvermin:`<br/>`1% chance`      |                                                         |      |
| Hatred of Rat         | `dmg p +0.15 vs rat`<br/>`stress res p -0.15 vs rat`                                                                            |                           | 0.75      | fear_of_rat                                             |      |
| Horn Rats Gift        | `bleed res +0.2`<br/>`blight res +0.2`<br/>`disease res +0.3`                                                                   | `stress recv p +0.1`      | 0.5    |                                                         | Singleton   |
| Natural Born Idiot            | `stun res +0.2`                                                                                                                 | `resolve xp bonus p -0.5` | 0.75      |                                              |  Singleton    |
| Luckwearer            | `def +0.025`<br/>`crit +0.025`<br/>`scouting 0.025`                                                                                |                           | 0.75      | unluckwearer                                            |      |
| Mistwalker            | `Upon turn start - Stealth self for 15% chance (2rds)`                                                                                                                                |                           | 0<br/>`Kill Gutter Runner: 2% chance`     |                                                         |      |
| Nemesis               | `dmg p +0.15 vs sz2`<br/>`atk +0.05 vs sz2`                                                                                     |                           | 0<br/>`Attack Ratogre: 1% Chance`    |                                                         |      |
| Slayer of Rat        | `atk +0.1 vs rat`<br/>`crit +0.05 vs rat`                                                                                       |                           | 0.75      | fear of rat                                             |      |
| Determined         | `death blow res +0.1`<br/>`prot +0.1 when marked`                                                                   |                           | 0.75       | weak_willed<br/>suicidal                                |      |
| Tunnel Rat         | `scouting chance +0.05`<br/>`trap resist +0.1`                                                                   |                           | 0<br/>`Disarm Rat Trap: 5% chance` |                                |      |
| Field Medic         | `Heal amount +1`                                                                   |                           | 0<br/>`Use Basic Medicine Supplies 4 times in the same dungeon with the same hero` |                                |      |

# Negative Quirks

base chance 95.5

| id                       | positive                                         | negative                                                                                                           | chance | imcompatible                                          | misc |
| :----------------------- | :----------------------------------------------- | :----------------------------------------------------------------------------------------------------------------- | :----- | :---------------------------------------------------- | :--- |
| Black Hunger             | `crit +0.03`<br/>`dmg p +0.1`                    | `stress recv p +2 in camping`<br/>`food consumption p +2`<br/>`stress recv p +2 in hunger`<br/>`starving dmg p +2` | 0.75    |                                                       |      |
| Betrayer                 |                                                  |  `upon turn start - attack ally (5%, Max HP 10%)`<br/>`upon turn start - randon command (5%)`                                                                                                                  | 0.75      |                                                       |      |
| Wimpy           |                                                  | `stress heal p -0.2`                                                                                               | 0.75      |                                                       |      |
| Bull-Step             | `move res +0.3`                                  | `spd -3 in corridor` `spd -1 in room`                                                                                                          | 0.75      | Strider                                         |      |
| Deep Scar                |                                                  | `max hp p -0.1`<br/>`death blow res -0.1`<br/>`bleed cure received chance -0.2`<br/>`blight cure received chance -0.2`                                                                          | 0<br/>`5% chance if hit by Gutterrunner`      |                                                       |      |
| Dirty Rat                | `SPD +2`                                                 | `food consumption p +2`<br/>`stress recv p +2 in hunger`<br/>`starving dmg p +2`<br/>`Upon turn start - attack ally (3%, Max HP 20%)`                                                                                                                 | 0<br/>`Heroes from town event`      | "slayer_of_rat"<br/>"hatred_of_rat"<br/>"fear_of_rat" |      |
| Fear of Rat              |                                                  | `stress recv p +0.15 vs rat`<br/>`atk -0.1 vs rat`                                                                 | 0.75      | "hatred_of_rat"<br/>"slayer_of_rat"                   |      |
| Heretic                  |                                                  | `worship curio - 30% forced interaction`<br/>`steals loot afterwards`                                                                                                                   | 0.75      | "faithful"<br/>"god_fearing"                          |      |
| Martyr              |                                                  |  `Upon Turn Start - Guard companion (7.5%%)`<br/>`upon turn start - self mark (7.5%)`                                                                                                                 | 0.75      |                                                       |      |                      
| Mutated                  | `max hp +0.15x`                                   | `stress res p +0.3`                                                                                                | 0.75    |                                                       |      |
| Self Sufficient          |  `Upon turn start - 5% Actordot (on kill: provision loot)`                                                | `Upon turn start - 5% chance to use an item`                                                                                                                   | 0.75      |                                                       | effect not available for mod heroes    |
| Twisted                  | `hp above 50%: dmg received -10%`<br/>`stress below 50: stress -10%`                                      | `hp below 50%: dmg received +20%`<br/>`stress above 50: stress +20%`                                                                                               | 0.75      |                                                       |      |
| Uncleanly                |                                                  | `blight res -0.1`<br/>`blight res -0.1 if no holy water`<br/>`disease res -0.1`                                                                           | 0.75      | "cleanly"                                             |      |
| Unluckwearer             |                                                  | `def -0.025`<br/>`crit -0.025`<br/>`scouting -0.025`                                                                  | 0.75      | "luckwearer"                                          |      |
| Venomous                 | `dmg p +0.25 if poisoned`                        | `blight res -0.2`                                                                                                  | 0.75      |                                                       |      |
| Warpstone Mine Scrounger | `scout +0.1 in mine`          | `10% forced interaction with every curio in mine, steals`                                                                                                    | 0.75      |                                                       |      |
| Mechanophobia   | `dmg p -0.10 vs warp engineered`<br/>`trap res -0.2`                                                    |                           | 0.75     |  Warp-Engineer                                        |      |