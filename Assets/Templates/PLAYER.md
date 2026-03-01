<%*
// ###########################################################
//                       Helper Functions
// ###########################################################

// Convert string to camelCase
function toCamelCase(str) {
  return str
    .replace(/(?:^\w|[A-Z]|\b\w|\s+|[-_])/g, (match, index) =>
      index === 0 ? match.toLowerCase() : match.toUpperCase()
    )
    .replace(/[\s-_]+/g, '');
}

// Return icon based on class
function getIcon(Class) {
  const iconMappings = {
    Bard: ':FasGuitar:',
    Druid: ':FasMoon:',
    Guardian: ':FasUserShield:',
    Paladin: ':FasFireFlameCurved:',
    Ranger: ':FasBullseye:',
    Rogue: ':RiSwordFill:',
    Seraph: ':FasPersonPraying:',
    Sorcerer: ':FasHandSparkles:',
    Warrior: ':FasHandFist:',
    Warlock: ':FasBurst:',
    Wizard: ':FasWandMagicSparkles:'
  };

  return iconMappings[Class] || ':FasCircleQuestion: Sub Class';
}

// ###########################################################
//                         Main Code
// ###########################################################

// Call modal form & declare variables
const result = await MF.openForm('PC');
const name = result.Name.value;
const Ancestry = result.Ancestry.value;
const Community = result.Community.value;
const Class = result.Class.value;
const subClass = result.subClass.value;
const subType = getIcon(Class);
const quote = result.Quote.value;
const cSheet = result.cSheet.value;

if (result.status === 'ok') {

    // Rename file & open in new tab; Fire toast notification
    await tp.file.rename(name);
    await app.workspace.getLeaf(true).openFile(tp.file.find_tfile(name));
    new Notice().noticeEl.innerHTML = `<span style="color: green; font-weight: bold;">Finished!</span><br>New player character <span style="text-decoration: underline;">${name}</span> added`;

} else {

    // Fire toast notification & exit templater
    new Notice().noticeEl.innerHTML = `<span style="color: red; font-weight: bold;">Cancelled:</span><br>Player character has not been added`;
    return;
}
-%>
---
type: pc
level: 1
evasion: 10
hp: 6
stress: 5
ancestry: "<% Ancestry ? Ancestry : '' %>"
community: "<% Community ? Community : '' %>"
class: "<% Class ? Class : '' %>"
subClass: "<% subClass ? subClass : '' %>"
cover: "/Assets/Images/Portrait.jpg"

---

###### <% name %>
:FasPerson: Player Character | :FasQuoteLeft: <% quote ? quote : 'Quote or tagline here' %> :FasQuoteRight:
___
> [!infobox|no-t right]
> ![[portrait.jpg|350]]
>
> | Type | Stat |
> | ---- | ---- |
> | :FasCrown: Level   | `=this.level` |
> | :RiSwordFill: Class |  `=this.class` |
> | <% subType %> Subclass |  `=this.subClass`|
> |  :LiDna: Ancestry |  `=this.ancestry`|
> |  :FasUserGroup: Community |  `=this.community`|
> 
>> [!tip]- STATS
>> | Stat | Score |
>> | ---- | :----: |
>> | :FasPersonRunning: Agility | +0 |
>> | :LiBicepsFlexed: Strength | +0 |
>> | :FasHands: Finesse | +0 |
>> | :LiEye: Instinct | +0 |
>> | :RiSpeakFill: Presence | +0 |
>> | :FasBook: Knowledge | +0 |
>> | :RaPlayerDodge: Evasion | `=this.evasion` |
>> | :FasHeart: Max HP | `=this.hp` |
>> | :FasBoltLightning: Max Stress | `=this.stress` |
>
>^InfoBox

> [!infobox|no-t clean right]
> ```meta-bind-button
> label: Character Sheet
> icon: link
> tooltip: external character sheet
> style: default
> action: {type: open, link: <% cSheet %>, newTab: true}
> ```

# Profile

> [!boxed|no-t]
> Introduction for players
>^IntroText
	
### Description

#### Background

#### Secrets

#### Motivations 

### Relationships

#### Allies
- [[Characters]] or [[Organisations]]

#### Enemies
- [[Characters]] or [[Organisations]]

### Magic Items / Abilities
- None
