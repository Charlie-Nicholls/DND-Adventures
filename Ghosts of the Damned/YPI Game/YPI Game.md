---
type: notes
date: 2025-06-11
Detective: "Canis"
Author: "Featherwick Crowley"
Chef: "Winnie Bearett"
ChefRussian: "Misha Bearov"
Pychic: "Mystic Myrtle"
Villian: "Harriet Adder"
---
###### YPI Game
<span class="sub2">:FasClock: Plan</span>

---


### Names

Detective: "Canis"
Author: "Featherwick Crowley"
Chef: "Winnie Bearett"
ChefRussian: "Misha Bearov"
Pychic: "Mystic Myrtle"
Villian: "Harriet Adder"

### Mod Rolls
Mod 1: 17

### `=this.Author`

Game is being run with three players so `=this.Author` will be run as an NPC using the following statblock:

```statblock
name: Author
speed: 30
ac: 12
hp: 28
stats: [10,14,10,14,15,18]
languages: English
skillsaves: [Deception: 6, Insight: 4, Investigation: 4, Stealth: 4]
traits:

actions:
  - name: Claw
    desc: "Melee Attack Roll: +4, reach 5 ft. Hit: 6 (1d6 + 3) Piercing damage"
bonus_actions:
  - name: First Aid Training (2/Day)
    desc: "A creature of the author's choice within 5ft. gains 7(1d4 + 4) hit points"
  - name: Bardic Inspiration (3/Day)
    desc: "The author chooses a creature within 60 feet. That creature gains one d6 die they can expend within the next 10 minutes to add to one ability check, attack roll or saving throw."
