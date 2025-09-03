<%*
const result = await MF.openForm('COUNTDOWN');
const label = result.Label.value;
const startval = result.StartValue.value;
_%>

```widgets
type: counter
text: <% label %>
id: <% label %>
startValue: <% startval %>
```