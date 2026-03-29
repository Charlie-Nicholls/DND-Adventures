###### Grove Ritual
<span class="sub2">:RiSwordFill: Encounter</span>

---

```statblock
name: Eloris Grove
tier: "1"
layout: Daggerheart Environment
type: Exploration
description: A former druidic grove haunted by the spirits of the slaughtered druids.
difficulty: "11"
potential_adversaries: Beasts (Bear, Dire Wolf, Glass Snake)
feats:
  - name: Overgrown Battlefield - Passive
    text: |-
      There has been a battle here. A PC can make an Instinct Roll to identify evidence of that fight. On a success with Hope, learn all three pieces of information below. On a success with Fear, learn two. On a failure, a PC can mark 3 Stress to learn one and gain advantage on the next action roll to investigate this environment. A PC with an appropriate background or Experience can learn an additional detail and ask a follow-up question about the scene and get a truthful (if not always complete) answer.

        - Traces of a battle (broken weapons and branches, gouges in the ground) litter the ground.
        - A moss-covered tree trunk is actually the corpse of a treant.
        - Still-standing trees are twisted in strange ways, as if by powerful magic.
  - name: Barbed Vines - Action
    text: Pick a point within the grove. All targets within Very Close range of that point must succeed on an Agility Reaction Roll or take 1d8+3 physical damage and become Restrained by barbed vines. Restrained lasts until they’re freed with a successful Finesse or Strength roll or by dealing at least 6 damage to the vines.
  - name: This Place Is Defended - Action
    text: The spirits of defeated druids appear to defend the grove, turning into spectral beastforms to attack. Two Dire Wolves and a number of Giant Rats equal to the number of PCs.
  - name: Bear - Action
    text: "**Spend a Fear** to summon a beastformed druid spirit of a Bear. They appear within Far range of a chosen PC and immediately take the spotlight."
  - name: Reinforcements - Action
    text: Summon the beastformed druid spirit of a Glass Snake or a number of Giant rats equal to the number of PCs. They appear within Far range of a chosen PC.
source: DaggerheartSRD
```
<br>

```statblock
creature: Bear
```
<br>

```statblock
creature: Dire Wolf
```
<br>

```statblock
creature: Glass Snake
```
<br>

```statblock
creature: Giant Rat
qty: 3
```