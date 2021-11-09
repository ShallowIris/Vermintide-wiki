# Potions

Potions target only performer, unless Moulder District is built. In the latter case, it will target performer_group.

Stack: 2 per type

Cannot be stocked in hamlet

### 회복의 포션 (Potion of Healing)

![Healing Potion](https://i.imgur.com/Xv14nWp.gif)

*치료 효과는 끝내줍니다. 혀가 얼얼해지는 맛에 비하면요.*<br/>
*Revitalizes a hero, but it tastes horrible.*

| effect                              | drop table                                                                                      | duration   | 
| :--------------------------------------------------------------- |  :------------------------------------------- | :---------------- |
| `Heal Max HP 25%`<br/>`Heals only 10% if Moulder District is built` | `V_potions: 25% chance to be chosen`<br/>`V_P&M: 16.7% chance to choose potion of healing`<br/><br/>`vermintide_crates curio: 80% to choose V_P&M, barehanded`<br/>`doom_production curio: 100% to choose V_P&M, with torch`<br/><br/>`ratling, engineer, warpfire thrower, globadier:`<br/>`5% chance to drop V_potions on kill` | `instant`

### 집중의 포션 (Potion of Concentration)

![Concentrate Potion](https://i.imgur.com/sQHX8Op.gif)

*"으윽, 포도주인줄 알았는데.. 잠을 못 자겠어." - 부디카*<br/>
*"Ugh, thought it was wine.. Feels like my heart is beating into my eyes." - Boudica.*

| effect                              | drop table                                                                                      | duration   | 
| :--------------------------------------------------------------- |  :------------------------------------------- | :---------------- |
| `ACC +10`<br/>`CRIT +7%`<br/>`ACC +7, CRIT +5% if Moulder District is built` | `V_potions: 25% chance to be chosen`<br/>`V_P&M: 16.7% chance to choose potion of concentration`<br/><br/>`vermintide_crates curio: 80% to choose V_P&M, barehanded`<br/>`doom_production curio: 100% to choose V_P&M, with torch`<br/><br/>`ratling, engineer, warpfire thrower, globadier:`<br/>`5% chance to drop V_potions on kill` | `duration: 4`<br/>`2 if Moulder District is built`<br/>`duration type: after_turn`

### 속도의 포션 (Potion of Speed)

![Speed Potion](https://i.imgur.com/QGSQouv.gif)

*톡 쏘는 맛이 납니다. 심장이 뛰는군요.*<br/>
*What a sharp taste! This makes your heart run.*

| effect                              | drop table                                                                                      | duration   | 
| :--------------------------------------------------------------- |  :------------------------------------------- | :---------------- |
| `SPD +3`<br/>`DODGE +10`<br/>`SPD +2, DODGE +7 if Moulder District is built` | `V_potions: 25% chance to be chosen`<br/>`16.7% chance to choose potion of speed`<br/><br/>`vermintide_crates curio: 80% to choose V_P&M, barehanded`<br/>`doom_production curio: 100% to choose V_P&M, with torch`<br/><br/>`ratling, engineer, warpfire thrower, globadier:`<br/>`5% chance to drop V_potions on kill` | `duration: 4`<br/>`2 if Moulder District is built`<br/>`duration type: after_turn`

### 완력의 포션 (Potion of Strength)

![Strong Potion](https://i.imgur.com/luVWsS9.gif)

*원료: 순도 100% 랫오거 담낭*<br/>
*Made with 100% pure Rat Ogre gall bladder*

| effect                              | drop table                                                                                      | duration   | 
| :--------------------------------------------------------------- |  :------------------------------------------- | :---------------- |
| `DMG +20%`<br/>`MAX HP +10%`<br/>`DMG +15%, MAX HP +10% if Moulder District is built` | `V_potions: 25% chance to be chosen`<br/>`V_P&M: 16.7% chance to choose potion of strength`<br/><br/>`vermintide_crates curio: 80% to choose V_P&M, barehanded`<br/>`doom_production curio: 100% to choose V_P&M, with torch`<br/><br/>`ratling, engineer, warpfire thrower, globadier:`<br/>`5% chance to drop V_potions on kill` | `duration: 4`<br/>`2 if Moulder District is built`<br/>`duration type: after_turn`



# 치료 키트 (Healing Kit)

Stack: 2 per type

Cannot be stocked in hamlet

### 보급용 치료 키트 (Basic Medical Supplies)

*영웅 한 명을 치료할 수 있을 정도의 물자가 들어있습니다.*<br/>
*Enough provisions to cure a hero.*

Target: Performer

![Bandage](https://i.imgur.com/qmt87jO.gif)

| effect                              | drop table                                                                                      | duration   | 
| :--------------------------------------------------------------- |  :------------------------------------------- | :---------------- |
| `Heal 5`<br/>`cure bleed/blight`<br/>`HEALRECV +15%` | `V_P&M: 16.7% chance to choose basic_medical_supplies`<br/><br/>`vermintide_crates curio: 80% to choose V_P&M, barehanded`<br/>`vermintide_crates curio: 70% chance to be dropped, with herb`<br/>`doom_production curio: 100% to choose V_P&M, with torch`<br/> | `duration: 2`<br/>`duration type: combat_end`

### 최상급 치료 키트 (Advanced Medical Supplies)

*이 정도 보급품량이면 원정대 전원을 치료할 수 있겠네요.*<br/>
*We can heal the entire party up with these provisions!*

Target: Performer_group

![Bandage](https://i.imgur.com/qmt87jO.gif)

| effect                              | drop table                                                                                      | duration   | 
| :--------------------------------------------------------------- |  :------------------------------------------- | :---------------- |
| `Heal 5`<br/>`cure debuff` | `V_P&M: 16.7% chance to choose advanced_medical_supplies`<br/><br/>`vermintide_crates curio: 80% to choose V_P&M, barehanded`<br/>`vermintide_crates curio: 30% chance to be dropped, with herb`<br/>`doom_production curio: 100% to choose V_P&M, with torch`<br/> | `duration: 2`<br/>`duration type: combat_end`



# Warpstone and Cure

Can be stocked in hamlet

### 워프스톤 (Warpstone)

Stack: 8 per type

Target: Performer

![Warpstone](https://i.imgur.com/vGMPj5C.gif)

*성자를 살인자로 뒤바꿔놓고, 처녀에게 색을 불어넣고, 인간을 금수로 만드는 이 돌은 무어란 말인가?*<br/>
*What is this substance that makes murderers of saints, lechers of the chaste, mutants out of men?*

| effect                              | drop table                                                                                      | duration   | 
| :--------------------------------------------------------------- |  :------------------------------------------- | :---------------- |
| `On first use:`<br/>`Blight/Stun chance +10%, stress +5`<br/>`On second use:`<br/>`Blight/Stun chance +10%, stress +5, 100% chance to get WSA` | `From Warpstone Refinery district: 2 warpstones per week`<br/>`vermintide_warp_stone curio: 100% to get 5 warpstones, with shovel`<br/>`doom_production curio: 100% to get 3 warpstones, with torch`<br/><br/>`ratling, engineer, warpfire thrower, globadier:`<br/>`40% chance to drop a warpstone on kill`<br/> |`duration: 3`<br/>`duration type: after_turn`

Refer to Quirks on wiki for more detailed effect when in Warpstone Addiction.

### VMARK-1 (Warpstone Addiction Cure)

Stack: 6 per type

Target: Performer

![Warpstone Cure](https://i.imgur.com/0qNDFCE.gif)

*급성 워프스톤 중독을 치료하기 위한 주사입니다.*<br/>
*A cure for acute Warpstone Addiction.*

| effect                              | drop table                                                                                      | duration   | 
| :--------------------------------------------------------------- |  :------------------------------------------- | :---------------- |
| `Cure Warpstone Addiction` | `From Plague Priest: 12 per difficulty` |`instant`