---
type: npc
locations:
 - "[[Feywild]]"
displayLink: "[[Nightmare Hag]]"
---

###### Nightmare Hag
<span class="sub2">:FasMapLocationDot: [[Feywild]] | :FasHeartPulse: Hostile </span>
___

> [!infobox|no-t right]
> ![[imgNightmareHag.png|350]]
>
> | Type | Stat |
> | ---- | ---- |
> | :FasVenusMars: Gender | Female |
> | :FasUser: Race | Hag |
>
>^InfoBox

# Profile

> [!boxed|no-t]
> A creature who walks in shadow even in the brightest light, her faces shrouded in darkness under the hood of the tattered shawl wrapped around her body. Her limbs are out of proportion, her legs bend in weird places at unnatural angles and four arms protrude from her shoulders. She has grey skin and long pointed black nails on the fingers of the hand which reaches out for you. Around her neck rests a neckless of bone, with a red gem embedded at its center.
>^IntroText

### Description
Nightmare Hags exist to warp the dreams of mortals into the disturbing, the frightening and the perverse. Revelling in the misery of the nightmares of mortals. They tend to collect nightmares, priding themselves on having the most awful collection, carefully choosing targets on which to bestow them.

[[Summer Night]] met a [[Nightmare Hag]] when she ran away from home and found herself in the [[Feywild]].

### Motivations
- Collect nightmares
- Twist the dreams of mortals to nightmares

### Enemies
- [[Summer Night]]

### Statblock
#### DND
```statblock
name: Nightmare Hag
layout: Basic 5e Layout
type: Fey
size: Medium
alignment: Neutral Evil
hp: 82
hit_dice: 11d8 + 33
ac: 17
speed: 30 ft.
stats: [18,12,16,13,14,14]
skillsaves: [Arcana: 3,Deception: 4,Perception: 4,Stealth: 3]
senses: Darkvision 120 ft.
languages: Common, Elvish, Sylvan
cr: 3
traits:
  - name: Incorporeal
    desc: The Nightmare Hag is resistant to all damage dealt whilst outside of dreams or dream rooms. If the Nightmare Hag ends her turn inside a nightmare she regains 2d8 hit points.
  - name: Innate Spellcasting
    desc: |-
      The nightmare hag's innate spellcasting ability is Wisdom (spell save DC 12, +4 to hit with spell attacks). It can innately cast the following spells, requiring no material components:

      At will: dancing lights, disguise self, invisibility, minor illusion, ray of sickness (level 3 version)
actions:
  - name: Multiattack
    desc: The Nightmare Hag makes two Claw attacks.
  - name: Claw
    desc: "Melee Weapon Attack: +6 to hit, reach 5 ft., one target. Hit: 8 (1d8 + 4) slashing damage."
bonus_actions:
  - name: Weave Nightmare
    desc: "Wisdom Saving Throw: DC 12, one creature within 60 ft. Failure: The target sees a creature from their nightmares in front of them and becomes frightened. The target can repeat this save at the end of each of its turns. If the target is Summer Night, the creature is be brought to life if it is CR 1 or lower with half hit points. A maximum of two such creatures can exist at once."
legendary_actions:
  - name: Nightmarish
    desc: "The Nightmare Hag uses Weave Nightmare"
```
#### Daggerheart
```statblock
name: Nightmare Hag
tier: "2"
layout: Daggerheart Adversary
type: Solo
description:
motives_and_tactics: 
difficulty: "15"
thresholds: 12/22
hp: "10"
stress: "5"
atk: "+5"
attack: "Dark Magic"
range: Close
damage: 2d6+3 mag
experience: Instinct +3
feats:
  - name: Relentless (2) - Passive
    text: The Nightmare Hag can be spotlighted up to two times per GM turn. Spend Fear as usual to spotlight them.
  - name: Creature of Dreams - Passive
    text: "The Nightmare Hag is invisible to all creatures with their eyes open outside of dreams, attacks made against them have disadvantage. They becomes visible inside dreams."
  - name: Weave Nightmare - Action
    text: "Spend a Fear to force all targets within Far range to make an Instinct Reaction Roll. On a failure, the target is frightened by visions of a creature from their nightmares, becoming vulnerable until they make a successful instinct roll or Mark a Stress to clear the condition. If Summer Night is targeted, summon a creature from the Nightmare Creatures table."
  - name: Summon Nightmare Creatures
    text: "Spend a Fear to summon two creatures from the Nightmare Creatures table."
  - name: Fearful Presence
    text: "mark 2 Stress to force all targets within Far range to make a Presence Reaction Roll. For each target who fails, you gain a Fear"
```
### Statblock
> ```statblock
> name: Nightmare Hag
> type: Fey
> size: Medium
> alignment: Neutral Evil
> hp: 82
> hit_dice: 11d8 + 33
> ac: 17
> speed: 30 ft.
> stats:
>   - 18
>   - 12
>   - 16
>   - 13
>   - 14
>   - 14
> skillsaves:
>   - Arcana: 3
>   - Deception: 4
>   - Perception: 4
>   - Stealth: 3
> senses: Darkvision 120 ft.
> languages: Common, Elvish, Sylvan
> cr: 3
> traits:
>   - name: Incorporeal
>     desc: The Nightmare Hag is resistant to all damage dealt whilst outside of dreams or dream rooms. If the Nightmare Hag ends her turn inside a nightmare she regains 2d8 hit points.
>   - name: Innate Spellcasting
>     desc: |-
>       The nightmare hag's innate spellcasting ability is Wisdom (spell save DC 12, +4 to hit with spell attacks). It can innately cast the following spells, requiring no material components:
> 
>       At will: dancing lights, disguise self, invisibility, minor illusion, ray of sickness (level 3 version)
> actions:
>   - name: Multiattack
>     desc: The Nightmare Hag makes two Claw attacks.
>   - name: Claw
>     desc: "Melee Weapon Attack: +6 to hit, reach 5 ft., one target. Hit: 8 (1d8 + 4) slashing damage."
> bonus_actions:
>   - name: Weave Nightmare
>     desc: "Wisdom Saving Throw: DC 12, one creature within 60 ft. Failure: The target sees a creature from their nightmares in front of them and becomes frightened. The target can repeat this save at the end of each of its turns. If the target is Summer Night, the creature is be brought to life if it is CR 1 or lower with half hit points. A maximum of two such creatures can exist at once."
> legendary_actions:
>   - name: Nightmarish
>     desc: "The Nightmare Hag uses Weave Nightmare"
> ```
