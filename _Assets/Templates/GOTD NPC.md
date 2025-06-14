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

// ###########################################################
//                         Main Code
// ###########################################################

// Call modal form & declare variables
const result = await MF.openForm('GOTD NPC');
const gender = result.Gender.value;
const name = result.Name.value;
const species = result.Species.value;

if (result.status === 'ok') {

    // Rename file & open in new tab; Fire toast notification
    await tp.file.rename(name);
    await app.workspace.getLeaf(true).openFile(tp.file.find_tfile(name));
    new Notice().noticeEl.innerHTML = `<span style="color: green; font-weight: bold;">Finished!</span><br>New NPC <span style="text-decoration: underline;">${name}</span> added`;

} else {

    // Fire toast notification & exit templater
    new Notice().noticeEl.innerHTML = `<span style="color: red; font-weight: bold;">Cancelled:</span><br>NPC has not been added`;
    return;
}
_%>

---
type: npc
displayLink: "[[<% name %>]]"
---

###### <% name %>
<span class="sub2"><% gender %> <% species %> </span>
___

> [!infobox|no-t right]
> ![[portrait.jpg|350]]
> 
> | Name |
> | :----: |
> | :FasUser: <% name %> | 
> 
> | Type | Stat |
> | ---- | ---- |
> | :FasVenusMars: Gender | <% gender %> |
> | :FasUser: Species | <% species %> |
>^InfoBox

# Profile

> [!boxed|no-t]
> Introduction for players
>^IntroText

### Description


### Secrets
- 

### Knowledge
- 

### Alibi 


### Statblock
>```statblock
name: <% name %>
speed: 30
ac: 10
hp: 10
stats: [10,10,10,10,10,10]
languages: English
skillsaves: []