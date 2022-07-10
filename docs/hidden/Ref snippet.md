---
share: true
category: hidden
---
![[Temporaire]]
# Embed Adjustments
| Attribute  | Description                              |
| ---------- | ---------------------------------------- |
| `nlk`      | Hide the link until hovered over embed   | 
| `lk-l`     | Move link to the left                    |
| `lk-clear` | Make background of the link transparent  |
| `nmg`      | Will remove margins and padding          |
| `full`     | Display the full embed                   |
| `clean`    | Removes borders/etc to hide embed design |

## Heading & Titles

| Attribute                         | Description                              |
| --------------------------------- | ---------------------------------------- |
| &lt;code&gt;nlk&lt;/code&gt;      | Hide the link until hovered over embed   |
| &lt;code&gt;lk-l&lt;/code&gt;     | Move link to the left                    |
| &lt;code&gt;lk-clear&lt;/code&gt; | Make background of the link transparent  |
| &lt;code&gt;nmg&lt;/code&gt;      | Will remove margins and padding          |
| &lt;code&gt;full&lt;/code&gt;     | Display the full embed                   |
| &lt;code&gt;clean&lt;/code&gt;    | Removes borders/etc to hide embed design |
| `no-h5`    | Hide all header 5s in the embedded page |
| `no-h6`    | Hide all header 6s in the embedded page |

# Custom syntax
- `**~~text~~**` : **~~text~~**
- `*~~text~~*` : *~~text~~*
- `**==text==**` : **==text==**
- `*==text==*` : *==text==*
- `**==~~text~~==**` : **==~~text~~==** 
- `__*text*__` : __*text*__
- `*==~~text~~==*`: *==~~text~~==*

# Dataview snippet

1. Embed all image in a folder
```js
dv.list(app.vault.getFiles().filter(file => file.extension === "png" || file.extension === "jpg").filter(file => file.path.includes("**FOLDER HERE FDP**")).map(file => dv.fileLink(file.path) ));
```