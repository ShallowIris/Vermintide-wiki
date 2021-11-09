- [Disease](#disease)
- [Positive Quirks](#positive-quirks)
- [Negative Quirks](#negative-quirks)

랜덤으로 얻을 수 있는 기벽: 164종, 긍정 65종, 부정 76종, 질병 23종 (모두 기반 확률 1)
광기의 색채 랜덤 기벽: 22종, 긍정 11종, 부정 9종, 질병 2종 (모두 기반 확률 1)

=> 긍정 기벽 기반 확률 76, 부정 기벽 기반 확률 85, 질병 기반 확률 25

# Warpstone Addiction

![](https://cdn.discordapp.com/attachments/876891269773787176/877562019291742318/unknown.png)

감염되었을 경우, 노출됨(2단계)부터 시작

* 1단계 - Radiating (발현) - 마력이 발산되는 상태
* 1'단계 - Warped (뒤틀림) - 마력이 충만해진 상태
* 2단계 - Exposed (노출됨) - 기본, 감염될시 Exposed에서 시작
* 2'단계 - Enlaced (뒤얽힘) - 워프스톤의 기운이 몸에 충만해진 상태, 영어로 'lace'는 하나의 약에 다른 약을 섞은 것을 뜻하기도 하기 때문에 이를 노린 네이밍
* 3단계 - Corrupted (오염됨) - 기존의 Hazy와 같음

## 워프스톤

* act_out_consume_priority = 1

### 워프스톤 드랍

1) 화기반이 높은 확률로 드랍 - 매쉬에서의 발생 빈도를 고려해봤을 때, 대략 30라운드 정도에 2개 정도 드랍할 수 있는 수준
2) 둠휠, 워프스톤 광맥 등에서 드랍
3) 활성화 퀘스트에서 골동품(워프스톤 구조물)을 활성화시킬시 넉넉하게 드랍

### 일반 상태에서 워프스톤을 사용할 경우:
 
* 중독 및 기절 확률 +10% (3턴간), 스트레스 +5
* 첫번째 사용할 경우 걸릴 확률이 없음, 해당 원정에서 2번째 이상 사용할 경우 100% 확률로 워프스톤 중독에 걸림

### 뒤틀림 상태에서: 
* 복용시 뒤틀림 상태의 지속시간 20턴 증가, 중독 및 기절 확률 +10% (20턴간)

### 뒤얽힘 상태에서: 
* 복용시 뒤얽힘 상태의 지속시간 20턴 증가, 피해 +15% (20턴간)

### 발현 상태에서: 
* 뒤틀림 상태로 진행

### 노출됨 상태에서: 
* 뒤얽힘 상태로 진행

### 오염됨 상태에서: 
* 노출됨 상태로 진행

## 감염 시점: 
1) 글로버디어, 파이어랫, 래틀링, 둠휠에게 피격시 (특정 기술만, 예를 들어 글로버디어의 평타, 파이어랫의 평타, 래틀링의 표식기, 둠휠의 Zzzap) 20% 확률로 감염
2) 워프스톤 사용시 감염
3) 워프스톤 Ore를 만질시 결과 중 20% 확률로 워프스톤 중독 감염 결과가 나옴

## 치료 시점:
1) 치료제가 드랍되는 방안 - 역병사제가 해독제를 대량으로 드랍

## Actout

### 1. 발현 단계:
1) 아무것도 없음 - 기반 확률 91
2) 턴 시작시 환각을 봐서 헛소리 - 파티원 전체 스트레스 ("BarkStress") - 기반 확률 3
3) 턴 시작시 파티원들에게 워프스톤의 기운을 부여함 (파티원 전체 버프 - spd +1, 중독 확률 -15%) - 기반 확률 4
4) 턴 시작시 워프스톤 소모 (consume_item actout + 워프스톤의 매우 높은 consume priority를 통해 구현) - 기반 확률 2

### 1'. 뒤틀림 단계:
1) 아무것도 없음 - 기반 확률 87
2) 턴 시작시 환각을 봐서 헛소리 - 파티원 전체 스트레스 ("BarkStress") - 기반 확률 3
3) 턴 시작시 파티원들에게 워프스톤의 기운을 부여함 (파티원 전체 버프 - spd +2, blight 1 * 3rds (500% base)) - 기반 확률 3
4) 턴 시작시 뽕 맞음 (스트레스 -10, 체력 피해 3) - 기반 확률 3
5) 턴 시작시 파티원 공격 (최대 체력 5%, 기절 120%) - 기반 확률 2
6) 턴 시작시 파티원 한 명에게 버프 (spd +3, atk +10) 및 워프스톤 중독 부여 - 기반 확률 2
7) 15% 확률로 후퇴 거부

### 2. 노출됨 단계:
1) 아무것도 없음 - 기반 확률 99
2) 턴 시작시 워프스톤 소모 - 기반 확률 1

### 2'. 뒤얽힘 단계:
1) 아무것도 없음 - 기반 확률 84
2) 무작위 행동 - 기반 확률 4
3) 턴 시작시 파티원을 팸 (최대 체력의 15%) - 기반 확률 4
4) 턴 시작시 워프스톤의 기운이 넘침 (스트레스 -5, 체력 회복 3) - 기반 확률 8
5) 15% 확률로 후퇴 거부

### 3. 오염됨 단계:
1) 아무것도 없음 - 기반 확률 69
2) 턴 시작시 헛소리 - 파티원 스트레스- 기반 확률 9
3) 턴 넘김 - 기반 확률 3
4) 무작위 행동 - 기반 확률 6
5) 턴 시작시 자해 (감각이 무뎌져간다! 이런 식으로?) - 최대 체력의 10% - 기반 확률 4
6) 턴 시작시 파티원을 팸 (최대 체력의 15%) - 기반 확률 4
7) 턴 시작시 워프스톤 소모 - 기반 확률 5
8) 힐, 버프, 캠핑시 식사, 캠핑시 기술 사용 혹은 효과 받기 거부 - 33% 확률
9) 광산에 있는 워프스톤 관련 골동품 (워프스톤 덩어리, 둠휠) 17% 확률로 강제 상호작용

## 워프스톤 중독 단계별 효과
| id                               | positive                                                                                      | negative                                                                                                                                                                                                                                                                            | imcompatible | duration   | 
| :------------------------------- | :-------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| :-------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 워프스톤 중독 - 발현 <br/> (WSA - Radiating) | `spd +1`<br/>`stun/blight chance +0.1`                                                                                      | `stress recv +0.15`<br/>`blight res -0.1`                                                                                                                                                                                                                                             |  핏빛 저주 모든 단계 <br/> 워프스톤 중독 다른 단계 <br/> Darkwraith, 대양인 질병  | 21 ~ 39 rds<br/>vmt_mine이 아닐시 지속시간 100rds 증가    |
| 워프스톤 중독 - 뒤틀림<br/>(WSA - Warped)  | `spd +3`<br/>`stun +0.1`<br/>`blight +0.15`<br/>`bleed +0.15`<br/>`debuff +0.15` | `stress recv +0.15` <br/>`blight res -0.1`                                                                                                                                                                                                                                                                   |  핏빛 저주 모든 단계 <br/> 워프스톤 중독 다른 단계 <br/> Darkwraith, 대양인 질병   |  19 ~ 31 rds   |
| 워프스톤 중독 - 노출됨<br/>(WSA - Exposed)   |  `max hp +0.1`                                                                                        | `stress recv +0.15`<br/>`blight res -0.1`                                                                                                                                                                                                                               | 핏빛 저주 모든 단계 <br/> 워프스톤 중독 다른 단계 <br/> Darkwraith, 대양인 질병  | 21 ~ 39 rds<br/>vmt_mine이 아닐시 지속시간 100rds 증가    |
| 워프스톤 중독 - 뒤얽힘<br/>(WSA - Enlaced)   |  `max hp +0.15`<br/>`spd +2`<br/>`dmg +0.1`                                                                                         | `stress recv +0.15`<br/>`blight res -0.1`                                                                                                                                                                                                                               | 핏빛 저주 모든 단계 <br/> 워프스톤 중독 다른 단계 <br/> Darkwraith, 대양인 질병  |  19 ~ 31 rds    |
| 워프스톤 중독 - 오염됨<br/>(WSA - Corrupted)    |                                                                                               | `stress recv p +0.5`<br/>`resolve check p -0.2`<br/>`blight res -0.3`<br/>`max_hp p -0.2`<br/>`spd -4`                                                                                                                                                                              | 핏빛 저주 모든 단계 <br/> 워프스톤 중독 다른 단계 <br/> Darkwraith, 대양인 질병 |  indefinite    |

* 마을에 있을시 일괄 15 rds 지남

# Disease

총 기반 확률 31

워프스톤 중독을 제외한 질병의 경우 광산에서 걸릴 수 있는 질병 + 적당히 골때리는 컨셉들로 잡았습니다.


| id                               | positive                                                                                      | negative                                                                                                                                                                                                                                                                            | chance | imcompatible                                                                                                                                                                                                                    | misc |
| :------------------------------- | :-------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | :--- |
| 진폐증 (Black Lung)                       |                                                                                               | `spd -3 after 1st rounds`<br/>`crit -0.03 after 1st rounds`<br/>`dmg p -0.1 after 1st rounds`                                                                                                                                                                                       | 1      |                                                                                                                                                                                                                                 |      |
| 심재성 화상 (Deep Burn)                             |                                                                                               | `bleed/blight res -0.15`<br/>`bleed/blight dmgrecv +0.15`<br/>`disease res -0.25`                                                                                                                                                                                                                    | 1      |                                                                                                                                                                                                                                 |      |
| 만성 피로 (Chronic Fatigue)                  |                                                                                               | `stress heal recv p -0.5 if idle`<br/>`stress heal recv p -0.5 in buildings` | 1      |                                                                                                                                                                                                                                 |      |
| 돌발성 난청 (Sudden Deafness)               |                                                                                               | `이동 및 기절 저항 -20%`<br/>`격려의 선율 및 위험 경보로 받는 스트레스 해소 수치 -50%` | 1      | tended_deafness                                                                                                                                                                                                                               | `60라운드 지속`<br/>`마을에 있을시 60라운드 모두 진행됨`<br/>`60라운드 이후:`<br/>`난청증(Tended Deafness)으로 변경`     |
| 난청증(Tended Deafness)                  |                                                                                               | `이동 및 기절 저항 -10%`<br/>`격려의 선율 및 위험 경보로 받는 스트레스 해소 수치 -20%` | `돌발성 난청에서 60라운드 경과`     |  sudden_deafness                                                                                                                                                                                                                               |      |
| 가연성 화농 (Inflammable Pyrogenesis)          | `torch increase p +0.4`                                                                       | `dmg recv p +0.33`                                                                                                                                                                                                                                                                  | 1      |                                                                                                                                                                                                                                 |      |
| 안구진탕증 (Dancing Eyes)                       |                                                                                               | `on attack: random target 20%`                                                                                                                                                                                                                                                                    | 1       |                                                                                                                                                                                                                                 |      |
| 황열병 (Yellow Skull Fever)                       |                                                                                               | `max hp p -0.7`<br/>`heal received p -0.9`<br/>`blight resist -0.7`                                                                                                                                                                                                                                                                   | `역병사제 스킬`       |                                                                                                                                                                                                                                 |      |
# Positive Quirks

총 기반 확률 86.4

Nemesis나 Mistwalker같이 기존에 '어떤 몬스터를 처치했을 때' 기벽을 얻을 수 있는 것으로 기획안이 잡혔던 경우, 대신에 '해당 몬스터를 타격할 때' 기벽을 얻을 수 있는 것으로 구현할 수 있습니다. 실험 결과, 처치시 기벽을 주는 것도 가능합니다.

| id                    | positive                                                                                                                        | negative                  | chance | imcompatible                                            | misc |
| :-------------------- | :------------------------------------------------------------------------------------------------------------------------------ | :------------------------ | :----- | :------------------------------------------------------ | :--- |
| 워프 공학자 (Warp-Engineer)   | `dmg p +0.10 vs warp engineered`<br/>`atk +0.05 vs rat`<br/>`trap res +0.15`                                                    |                           | 0.5<br/>`둠휠 골동품에서 드랍`      |  Mechanophobia                                          |      |
| 성큼걸이 (Strider)          | `spd +3 in corridor` `spd +1 in room`                                                                                                                       | `move res -0.3`           | 0.75      | Bull-Step                                            |      |
| 전장의 기수 (Standard-bearer)<br/>`전투 및 응급 상황에서 아군을 위로합니다.`      | `10% 확률로 자신을 제외한 원정대 스트레스 3 회복`<br/>`아군이 적의 공격을 회피할시 대상 10% 확률로 스트레스 5 회복`<br/>`아군이 적에게 공격을 명중시킬시 대상 10% 확률로 스트레스 5 회복`<br/>`함정 해제 실패시 50% 확률로 대상 스트레스 5 회복`                                                                                        |                           | 0.5      |                                                  |      |
| 카나리아 (Yellow Canary)              | `party surprise -0.1`<br/>`scouting +0.07`                                                                                      |                           | 0.4    |                                                         | 고유기벽     | 
| 청결함 (Cleanly)               | `blight res +0.1`<br/>`blight res +0.1 if has holy water`<br/>`disease res +0.1`                                                                                        |                           | 0.75      | uncleanly                                               |      |
| 주술 파훼꾼 (Counterspell)          | `debuff res +0.2`                                                                                                               |                           | 0.5<br/>`스케이븐 토템에서 드랍`      | hexer                                                        | `500라운드 지속`<br/>`마을에 있을시 10라운드 진행`<br/>`500라운드 이후:`<br/>`저주술사(Hexer)로 변경`<br/>`진화형 기벽 - 색상 다르게`     |
| 저주술사 (Hexer)          | `debuff res +0.2`<br/>`debuff chance +0.2`                                                                                                                |                           | `주술 파훼꾼에서 진행`      |  counterspell                                                       |      |
| 여명의 인도자 (Dawnbringer)           | `torch inc p +0.3`                                                                                                              |                           | 0.5      | "nocturnal"<br/>"sensitive_to_light"<br/>"phengophobia"<br/>"daybreaker" | `500라운드 지속`<br/>`마을에 있을시 10라운드 진행`<br/>`500라운드 이후:`<br/>`새벽을 여는 자(Daybreaker)로 변경`<br/>`진화형 기벽 - 색상 다르게`     |
| 새벽을 여는 자 (Daybreaker)           | `torch inc p +0.3` `stun chance +0.1 if torch above 76`                                                                                                              |                           | `여명의 인도자에서 진행`      | "nocturnal"<br/>"sensitive_to_light"<br/>"phengophobia"<br/>"dawnbringer" |      |
| 처형자 (Executioner)           | `atk +0.07 vs hp below 0.5`<br/>`crit +0.07 vs hpbelow 0.5`                                                                       |                           | 0.75<br/>`일반병종 처치시 1% 확률로 획득`      |                                                         |      |
| 쥐 혐오 (Hatred of Rat)         | `dmg p +0.15 vs rat`<br/>`stress res p -0.15 vs rat`                                                                            |                           | 0.75      | fear_of_rat                                             |      |
| 뿔난 쥐의 은총 (Horn Rats Gift)        | `bleed res +0.2`<br/>`blight res +0.2`<br/>`disease res +0.3`                                                                   | `stress recv p +0.1`      | 0.5    |                                                         | 고유기벽    |
| 선천성 얼간이 (Natural Born Idiot)            | `stun res +0.2`                                                                                                                 | `resolve xp bonus p -0.5` | 0.75      |                                              |  고유기벽    |
| 행운을 타고난 자 (Luckwearer)            | `def +0.025`<br/>`crit +0.025`<br/>`scouting 0.025`                                                                                |                           | 0.75      | unluckwearer                                            |      |
| 안개걸음 (Mistwalker)            | `턴 시작시, 15% 확률로 스스로에게 은신 (2rds)`                                                                                                                                |                           | 0<br/>`거터러너류 처치시 2% 확률`     |                                                         |      |
| 징벌자 (Nemesis)               | `dmg p +0.15 vs sz2`<br/>`atk +0.05 vs sz2`                                                                                     |                           | 0<br/>`랫오거류 타격시 1% 확률`    |                                                         |      |
| 쥐 학살자 (Slayer of Rat)         | `atk +0.1 vs rat`<br/>`crit +0.05 vs rat`                                                                                       |                           | 0.75      | fear of rat                                             |      |
| 의연함 (Determined)         | `death blow res +0.1`<br/>`prot +0.1 when marked`                                                                   |                           | 0.75       | weak_willed<br/>suicidal                                |      |
| 땅굴쥐 (Tunnel Rat)         | `scouting chance +0.05`<br/>`trap resist +0.1`                                                                   |                           | 0<br/>`쥐 함정 해제시 5% 확률로 획득`<br/> |                                |      |
| 야전 의료병 (Field Medic)         | `Heal amount +1`                                                                   |                           | 0<br/>`한 던전에서 일반 치료 키트를 4회 사용할 시 획득` |                                |      |

# Negative Quirks

총 기반 확률 95.5

| id                       | positive                                         | negative                                                                                                           | chance | imcompatible                                          | misc |
| :----------------------- | :----------------------------------------------- | :----------------------------------------------------------------------------------------------------------------- | :----- | :---------------------------------------------------- | :--- |
| 검은 굶주림 (Black Hunger)             | `crit +0.03`<br/>`dmg p +0.1`                    | `stress recv p +2 in camping`<br/>`food consumption p +2`<br/>`stress recv p +2 in hunger`<br/>`starving dmg +0.2 (percentage of MAX HP)` | 0.75    |                                                       |      |
| 배신자 (Betrayer)                 |                                                  |  `턴 시작시 5% 확률로 아군 공격 (체력 10%)`<br/>`5% 확률로 임의 행동`                                                                                                                  | 0.75      |                                                       |      |
| 유약함 (Wimpy)            |                                                  | `stress heal p -0.2`                                                                                               | 0.75      |                                                       |      |
| 황소 걸음 (Bull-Step)             | `move res +0.3`                                  | `spd -3 in corridor` `spd -1 in room`                                                                                                          | 0.75      | Strider                                         |      |
| 깊은 상처 (Deep Scar)                |                                                  | `max hp p -0.1`<br/>`death blow res -0.1`<br/>`bleed cure received chance -0.2`<br/>`blight cure received chance -0.2`                                                                          | 0<br/>`거터러너에게 피격시 5% 확률`      |                                                       |      |
| 쥐새끼 (Dirty Rat)                | `속도 +2`                                                 | `stress recv p +1 in camping`<br/>`food consumption p +1`<br/>`stress recv p +1 in hunger`<br/>`starving dmg +0.2 (percentage of MAX HP)`<br/>`3% 확률로 턴 시작시 아군 공격 (체력 20% 피해)`<br/>                                                                                                                 | 0<br/>`마을 이벤트 용병만`      | "slayer_of_rat"<br/>"hatred_of_rat"<br/>"fear_of_rat" |      |
| 쥐 공포증 (Fear of Rat)              |                                                  | `stress recv p +0.15 vs rat`<br/>`atk -0.1 vs rat`                                                                 | 0.75      | "hatred_of_rat"<br/>"slayer_of_rat"                   |      |
| 이단자 (Heretic)                  |                                                  | `worship 골동품 30% 확률로 강제 상호작용`<br/>`강제 상호작용 후 전리품 훔침`                                                                                                                   | 0.75      | "faithful"<br/>"god_fearing"                          |      |
| 순교자 (Martyr)              |                                                  |  `턴 시작시 7.5% 확률로 임의 영웅 가드`<br/>`턴 시작시 7.5% 확률로 자신에게 표식`                                                                                                                 | 0.75      |                                                       |      |                      
| 돌연변이 (Mutated)<br/>`이곳에선 도움의 손길이 절실합니다. 마침 이 자는 팔이 3개군요.`                  | `max hp +0.15x`                                   | `stress res p +0.3`                                                                                                | 0.75    |                                                       |      |
| 자급 자족 (Self Sufficient)          |  `5% 확률로 턴 시작시 Actordot 발동, 적을 처치할 때마다 보급품 획득`                                                | `5% 확률로 턴 시작시 임의로 보급품 사용`                                                                                                                   | 0.75      |                                                       | 바닐라 영웅만 사용 가능     |
| 뒤틀림 (Twisted)                  | `hp above 50%: dmg received -10%`<br/>`stress below 50: stress -10%`                                      | `hp below 50%: dmg received +20%`<br/>`stress above 50: stress +20%`                                                                                               | 0.75      |                                                       |      |
| 불결함 (Uncleanly)                |                                                  | `blight res -0.1`<br/>`blight res -0.1 if no holy water`<br/>`disease res -0.1`                                                                           | 0.75      | "cleanly"                                             |      |
| 불운을 타고난 자 (Unluckwearer)             |                                                  | `def -0.025`<br/>`crit -0.025`<br/>`scouting -0.025`                                                                  | 0.75      | "luckwearer"                                          |      |
| 독기를 품은 (Venomous)                 | `dmg p +0.25 if poisoned`                        | `blight res -0.2`                                                                                                  | 0.75      |                                                       |      |
| 워프스톤 광산 약탈자 (Warpstone Mine Scrounger) | `scout +0.1 in mine`          | `10% forced interaction with every curio in mine, steals`                                                                                                    | 0.75      |                                                       |      |
| 기계 공포증 (Mechanophobia)   | `dmg p -0.10 vs warp engineered`<br/>`trap res -0.2`                                                    |                           | 0.75     |  Warp-Engineer                                        |      |