# Curios

[골동품별 기반 확률, 출현율과 필요 보급품량](https://docs.google.com/spreadsheets/d/1SVZWRxlQy89Iefn3GhNC77Z2CIdacQPk89y62JhtLvA/edit#gid=0)

```
Hallway Curio: 10 for short, 15 for medium, 20 for long
Room Curio: 1 for short, 1-2 for medium, 2-3 for long
```

## Skaven Altar (스케이븐 토템)

[[https://github.com/115dkk/darkest_dungeon_skaven_mod_project/blob/dev/0_2_0_Skaven%20Mod%20Alpha/props/shared/curios/vermintide_altar/vermintide_altar.png]]

```
쥐의 상징으로 저주받은 돌기둥.
A pillar, cursed with the sign of the rat.
```

Tags: Knowledge, Worship, Reflective, Unholy, All

### Expected Number per Mission
| Short     | Medium       | Long   | 
| :------------- |  :----------- | :---------------- |
| 0.76 | 1.23 | 1.52 |

### Barehand:

```
이 불길한 돌덩이를 만져봅니다...
Lay your hand on this wretched stone...
```

| effect type     | effect       | Chance  | String | 
| :--------- |  :--------------------------------- | :------ | :---------------------------- | 
| Quirk | Heretic Quirk | 20% | `강렬한 기운이 영웅에게 흘러들어옵니다!`<br/>`An intense force flows through the hero!` | 
| Quirk | Counterspell Quirk | 9% | `강렬한 기운이 영웅에게 흘러들어옵니다!`<br/>`An intense force flows through the hero!` | 
| Quirk | Horned Rat's Gift Quirk | 1% | `강렬한 기운이 영웅에게 흘러들어옵니다!`<br/>`An intense force flows through the hero!` | 
| Effect | Hero: Stress +25 | 70% | `불길한 기운이 영웅을 저주합니다.`<br/>`An ominous feeling mars the hero's mind.` | 

### Interacted with Provisions:

| effect type     | effect       | Provision, Chance  | String | 
| :--------- |  :--------------------------------- | :---------------- | :---------------------------- | 
| Quirk Removal | Remove a random **negative** quirk | Holy Water, 100% | `신성한 기운이 삼각형과 영웅을 정화합니다.`<br/>`A holy force cleanses both triangle and the hero.`  |
| Effect | Hero: Stress +100 | Shovel, 100% | `영웅은 끔찍한 저주를 받았습니다!`<br/>`The hero was appalled with the revelation!` |

## Stolen Supplies (도둑맞은 물자)

[[https://github.com/115dkk/darkest_dungeon_skaven_mod_project/blob/dev/0_2_0_Skaven%20Mod%20Alpha/props/shared/curios/vermintide_crates/vermintide_crates.png]]

```
제각기 소유자가 다른 것처럼 보이는 상자들이 어지러이 쌓여있습니다. 이제는 스케이븐의 것인가보죠.
Those boxes seem to be from different former owners. But right now, they're Skaven's.
```

Tags: Treasure, Food, Scrounging, All

### Expected Number per Mission
| Short     | Medium       | Long   | 
| :------------- |  :----------- | :---------------- |
| 1.53 | 2.38 | 3.06 |

### Barehand:

```
어떤 물건이 있나 살펴볼까요?
Let's look for something to take.
```

| effect type     | effect       | Chance  | String | 
| :--------- |  :--------------------------------- | :------ | :---------------------------- | 
| Loot | Drop 3 "H" Table | 75% | `숨겨진 가보가 쏟아집니다!`<br/>`Stacks of hidden heirlooms!` |
| Quirk | Kleptomaniac Quirk | 5% | `영웅이 나쁜 손버릇을 들여버렸습니다...`<br/>`The hero got a foul habit of plifering...` |
| Summon | Summon 'vermintide_summon' mash | 20% | `보급품의 주인들이 돌아왔습니다!`<br/>`Owners have returned!` |

### Interacted with Provisions:

| effect type     | effect       | Provision, Chance  | String | 
| :--------- |  :--------------------------------- | :---------------- | :---------------------------- | 
| Loot | Drop 1 Basic Medical Supplies | herbs, 70% | `약초로 망가진 의료품을 복구했습니다.`<br/>`Tainted medicines were restored with herbs.` |
| Loot | Drop 1 Advanced Medical Supplies | herbs, 30% | `약초로 망가진 의료품을 복구했습니다.`<br/>`Tainted medicines were restored with herbs.` |
| Loot | Drop 1 Firewood | Shovel, 25% | `상자를 쪼개 쓸만한 보급품을 얻었습니다.`<br/>`Smashing the boxes gives you valuable provisions.` |
| Loot | Drop 4 Torches | Shovel, 75% | `상자를 쪼개 쓸만한 보급품을 얻었습니다.`<br/>`Smashing the boxes gives you valuable provisions.` |

## Abandoned Potion Table (버려진 포션 테이블)

[[https://github.com/115dkk/darkest_dungeon_skaven_mod_project/blob/dev/0_2_0_Skaven%20Mod%20Alpha/props/shared/curios/vermintide_alchemy_table/vermintide_alchemy_table.png]]

```
지저분하고 오염된 테이블입니다. 쓸만한 물약이 남아있을 수도 있을까요?
An unclean table. Maybe there are some redeemable potions left...?
```

Tags: Drink, Knowledge, Treasure, All

### Expected Number per Mission
| Short     | Medium       | Long   | 
| :------------- |  :----------- | :---------------- |
| 0.77 | 1.15 | 1.54 |

### Barehand:

```
맨손으로 실험집기들을 만져봅니다...
Handle paraphernalias with bare hands...
```
| effect type     | effect       | Chance  | String | 
| :--------- |  :--------------------------------- | :------ | :---------------------------- | 
| Nothing | - | 25% | `쓸만한 건 없군요.`<br/>`Nothing valuable here.` |
| Quirk | Cleanly Quirk | 12.5% | `영웅이 지저분한 먼지를 뒤집어씁니다.`<br/>`The hero is covered with mungy dusts.` |
| Quirk | Uncleanly Quirk | 12.5% | `영웅이 지저분한 먼지를 뒤집어씁니다.`<br/>`The hero is covered with mungy dusts.` |
| Effect | Hero: Blight 2 * 3rds (100% base chance) | 50% | `영웅이 수상쩍은 액체에 중독됐습니다.`<br/>`The hero is poisoned by suspicious liquid.` |

### Interacted with Provisions:

| effect type     | effect       | Provision, Chance  | String | 
| :--------- |  :--------------------------------- | :---------------- | :---------------------------- | 
| Loot | Drop 1 random potion | antivenom, 100% | `오염된 포션을 해독제로 중화했습니다!`<br/>`Contaminant in the potion has been neutralized!` |

## Huge Warpstone Ore (대형 워프스톤 광맥)

[[https://github.com/115dkk/darkest_dungeon_skaven_mod_project/blob/dev/0_2_0_Skaven%20Mod%20Alpha/props/shared/curios/vermintide_warp_stone/vermintide_warp_stone.png]]

```
매혹적인 초록빛으로 빛나는 광맥. 보는 사람을 유혹하는 듯 합니다.
An ore gleaming with enticing green.
```

Tags: Treasure, All, Warpstone

### Expected Number per Mission
| Short     | Medium       | Long   | 
| :------------- |  :----------- | :---------------- |
| 1.35 | 2.02 | 2.69 |

### Barehand:

```
맨손으로 광맥을 파봅니다.
Dig into the ore with bare hands.
```

| effect type     | effect       | Chance  | String | 
| :--------- |  :--------------------------------- | :------ | :---------------------------- | 
| Nothing | - | 15% | `광맥을 파내자 갑자기 돌이 빛을 잃고 바스라집니다.`<br/>`Upon digging up, the ore suddenly loses its light and crumbles.` |
| Loot | Drop 3 "B" Tables | 15% | `값진 보물을 발견했습니다!`<br/>`Valuable loots!` |
| Quirk | Mutated Quirk | 30% | `워프스톤에서 기이한 빛이 납니다...`<br/>`What a strange light...` |
| Disease | Warpstone Addiction: Exposed | 20% | `영웅이 워프스톤 가루를 지나치게 흡입했습니다.`<br/>`The hero inhaled too much Warpstone.` |
| Summon | Summon 'vermintide_skryre_summon' mash | 20% | `보석에 정신이 팔린 사이 쥐새끼들이 기습했습니다!`<br/>`Blindsided by bloody rats!` |

### Interacted with Provisions:

| effect type     | effect       | Provision, Chance  | String | 
| :--------- |  :--------------------------------- | :---------------- | :---------------------------- | 
| Loot | Drop 3 "G" Tables, and 3 Warpstones | Shovel, 100% | `대량의 워프스톤을 채굴했습니다!`<br/>`A huge chunk of Warpstone!` |

## Weapon Stand (무기 거치대)

[[https://github.com/115dkk/darkest_dungeon_skaven_mod_project/blob/dev/0_2_0_Skaven%20Mod%20Alpha/props/shared/curios/vermintide_weapon_holder/vermintide_weapon_holder.png]]

```
곰팡이가 슬고 조잡한 무기 보관대. 아직 덜 마른 피가 묻어있습니다.
A moldy and shoddy weapon stand. Blood on some of them is yet to dry.
```

Tags: Scrounging, All

### Expected Number per Mission
| Short     | Medium       | Long   | 
| :------------- |  :----------- | :---------------- |
| 1.14 | 1.81 | 2.29 |

### Barehand:

```
날붙이 사이를 조심조심 뒤져봅니다.
Look through bladeware with care.
```

| effect type     | effect       | Chance  | String | 
| :--------- |  :--------------------------------- | :------ | :---------------------------- | 
| Nothing | - | 20% | `쓸만한 게 없군요.`<br/>`Nothing of value here.` |
| Loot | Drop 2 "rats" Tables | 20% | `무기 사이에 귀중품이 숨겨져있습니다!`<br/>`Prizes are found among the weapons!` |
| Effect | Hero: Bleed 3 * 3rds (120% base chance) | 40% | `영웅이 날에 베였습니다.`<br/>`The hero got cut by blades.` |
| Disease | Tetanus | 13.33% | `녹과 곰팡이의 냄새가 지독하군요...`<br/>`This stand reeks of mold and rust...` |
| Disease | Random | 6.67%  | `녹과 곰팡이의 냄새가 지독하군요...`<br/>`This stand reeks of mold and rust...` |

### Interacted with Provisions:

| effect type     | effect       | Provision, Chance  | String | 
| :--------- |  :--------------------------------- | :---------------- | :---------------------------- | 
| Loot | Drop 3 Torches | Shovel, 100% | `일부 무기들은 횃불로 활용할 수 있을 것 같습니다.`<br/>`Some of them can be kindled and used as torches.` |
| Effect | +20% DMG, +10% PROT | Bandage, 100% | `손을 보호하면서 꽤 쓸만한 날붙이를 발견했습니다.`<br/>`The hero found usable weapon with protected hands.` |

## Furless Thing Cage (민머리 전시 철장)

[[https://github.com/115dkk/darkest_dungeon_skaven_mod_project/blob/dev/wiki/image/cage_full.png]]

```
누군가가 철장 안에 갇혀 있습니다. 꺼내려면 난리가 날 것 같군요. 
Someone is locked inside the cage. It would be quite a fuss to let him out.
```

Tags: Torture, All

### Expected Number per Mission
| Short     | Medium       | Long   | 
| :------------- |  :----------- | :---------------- |
| 0.19 | 0.29 | 0.38 |

### Barehand:

```
맨손으로 억지로 열어봅시다.
Forcefully open the cage.
```

| effect type     | effect       | Chance  | String | 
| :--------- |  :--------------------------------- | :------ | :---------------------------- | 
| Nothing | - | 100% | `맨손으로는 열리지 않습니다.`<br/>`Cannot open this cage without tools.` |

### Interacted with Provisions:

| effect type     | effect       | Provision, Chance  | String | 
| :--------- |  :--------------------------------- | :---------------- | :---------------------------- | 
| Summon | 2 Mutated Rat Wolves, 1 Unclean Hybrid | Shovel, 100% | `철장이 열리자 이를 눈치챈 주인이 돌아왔습니다!`<br/>`Upon opening the cage, the owner noticed it and returned!` |

## Unfinished Doomwheel (미완성된 둠휠)

[[https://github.com/115dkk/darkest_dungeon_skaven_mod_project/blob/dev/0_2_0_Skaven%20Mod%20Alpha/props/shared/curios/doom_production/doom_production.png]]

```
정교한 공학 설계가 돋보이는 기계. 사람이 타기에는 좁아보입니다.
A warmachine engineered with utmost delicacy. Maybe a little bit cramped for a man-thing.
```

Tags: Knowledge, All, Warpstone

### Expected Number per Mission
| Short     | Medium       | Long   | 
| :------------- |  :----------- | :---------------- |
| 0.48 | 0.76 | 0.95 |

### Barehand:

```
기계장치를 이리저리 건드려봅니다.
Mess around with this machine.
```

| effect type     | effect       | Chance  | String | 
| :--------- |  :--------------------------------- | :------ | :---------------------------- | 
| Quirk | Warp Engineer Quirk | 20% | `영웅이 워프스톤 배터리를 건드렸습니다!`<br/>`The hero came in contact with a Warpstone battery!` |
| Quirk | Venomous Quirk | 25% | `영웅이 워프스톤 배터리를 건드렸습니다!`<br/>`The hero came in contact with a Warpstone battery!` |
| Effect | Hero: Blight Resist -15% (Until Quest End) | 25% | `독기가 새어나옵니다. 무언가 잘못됐습니다.`<br/>`A virulent gas is leaking. Something is wrong.` |
| Summon | Summon 'vermintide_engineer_summon' mash | 30% | `함정입니다!`<br/>`It's a trap!` |

### Interacted with Provisions:

| effect type     | effect       | Provision, Chance  | String | 
| :--------- |  :--------------------------------- | :---------------- | :---------------------------- | 
| Quirk | Warp Engineer Quirk | Shovel, 20% | `정교한 공학 설계가 영감을 불어넣었습니다!`<br/>`Delicate engineering inspires the hero!` |
| Quirk | Random Positive Quirk | Shovel, 80% | `정교한 공학 설계에 영감을 불어넣었습니다!`<br/>`Delicate engineering inspires the hero!` |
| Loot | 1 "G" + Drop 1 random potion, or a warpstone | Torch, 100% | `횃불로 태우자 잔해들이 결정화됩니다.`<br/>`Burning it left us with crystalized gems.` |

## Noisy Repair - 상호작용할 때 이름 및 설명이 뜨지 않음

[[https://github.com/115dkk/darkest_dungeon_skaven_mod_project/blob/dev/0_2_0_Skaven%20Mod%20Alpha/props/shared/curios/noisy_repairs/noisy_repairs.png]]

Tags: Treasure, All

Only turns up as a room curio

### Expected Number per Mission
| Short     | Medium       | Long   | 
| :------------- |  :----------- | :---------------- |
| 0.36 | 0.73 | 0.73 |

### Barehand:

| effect type     | effect       | Chance                                                                                | 
| :--------------------------------------------------------------- |  :------------------------------------------- | :---------------- |
| Loot | Drop 2 "Rats" Tables | 100% |

## Others

Room Treasures: equal to the base game.

Hallway Curios: Discarded Pack and Crates will be added as a filler material, with 23 base chance.

### Expected Number per Mission of Pack and Crates
| Short     | Medium       | Long   | 
| :------------- |  :----------- | :---------------- |
| 4.42 | 6.63 | 8.85 |


# Obstacles

```
Obstacles: 1-3 for short, 1-4 for medium, 1-5 for long
```

### Collapsed Shaft (갱도 잔해)

[[https://github.com/115dkk/darkest_dungeon_skaven_mod_project/blob/dev/wiki/image/townrubble.png]]

```
천장이 무너져 목재와 석재가 길을 막고 있습니다.
An impasse out of stone and wooden beams, from a collapsed ceiling.
```

Shovel needed, 1/2 chance

### Obsolete Scaffold (버려진 비계)

[[https://github.com/115dkk/darkest_dungeon_skaven_mod_project/blob/dev/0_2_0_Skaven%20Mod%20Alpha/props/shared/obstacles/obstacle_noisyrepair/obstacle_noisyrepair.png]]

```
갱도 공사에 쓰였던 비계처럼 보이지만, 지금은 길을 막는 장애물일 뿐입니다.
Seems like this was used for constructing a shaft, but it's a mere obstacle now.
```

Torch needed, 1/2 chance

# Traps

```
Obstacles: 1-2 for short, 2-4 for medium, 3-5 for long
```

### Spikes

[[https://github.com/115dkk/darkest_dungeon_skaven_mod_project/blob/dev/wiki/image/spikes.png]]

1/2 chance

Proc: DMG Max HP 20 / 23 / 25%, Hero debuff: PROT -25% / -40% / -55% (120 / 140 / 160% base chance, until quest end)

### Rat Trap

[[https://github.com/115dkk/darkest_dungeon_skaven_mod_project/blob/dev/wiki/image/trap.png]]

1/2 chance

Success: Stress -8, 5% chance to gain 'Tunnel Rat' quirk

Proc: Party Surprised by rats, Party debuff: SPD -3 (500% base chance)