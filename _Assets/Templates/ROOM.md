<%*
// ###########################################################
//                        Helper Functions
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
//                        Main Code Section
// ###########################################################

// Call modal form & declare variables
const result = await MF.openForm('ROOM');
const location = result.Location.value;
const name = result.Name.value;

if (result.status === 'ok') {

    // Rename file & open in new tab; Fire toast notification
    await tp.file.move(`Ghosts of the Damned/Beaverton Hall/${location}/${name}`);
    await app.workspace.getLeaf(true).openFile(tp.file.find_tfile(name));
    new Notice().noticeEl.innerHTML = `<span style="color: green; font-weight: bold;">Finished!</span><br>New landmark <span style="text-decoration: underline;">${name}</span> added`;

} else {

    // Fire toast notification & exit templater
    new Notice().noticeEl.innerHTML = `<span style="color: red; font-weight: bold;">Cancelled:</span><br>Room has not been added`;
    return;
}
_%>

---
cssClasses: grayTable, wideTable
type: room
locations:
 - <% location ? `"[[${location}]]"` : '' %>
displayLink: "[[<% name %>]]"
---
###### <% name %>
<span class="sub2">:FasHouse: <% location %></span>

---

> [!recite|clean no-t]
>	Introduction for players
>^IntroText
	
### Connections

### Investigation Checks

> [!recite|nbrd no-i]- Easy
>	Introduction for players
>^Easy

> [!recite|nbrd no-i]- Medium
>	Introduction for players
>^Medium

> [!recite|nbrd no-i]- Hard
>	Introduction for players
>^Hard

### Secret Passages

### Other


