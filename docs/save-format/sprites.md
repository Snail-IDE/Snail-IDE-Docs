---
title: sprite format
---

### sprites folder
example contains the default enviroment when making a new project
```
 V sprites
 |  V sprite1
 |  |  V costumes
 |  |  |  costume1.svg
 |  |  V sounds
 |  |  sprite.json
 |  V stage
 |  |  V costumes
 |  |  |  backdrop1.svg
 |  |  V sounds
 |  |  sprite.json
```
note that the stage isnt necessary and can be omitted from the save

### sprite.json
| key | type |
| ----------- | ----------- |
| `name` | `string` |
| `volume` | `percentage: number` |
| `visible` | `boolean` |
| `x` | `number` |
| `y` | `number` |
| `size` | `percentage: number` |
| `direction` | `direction: number` |
| `draggable` | `boolean` |
| `rotation-style` | `"all around" \| "look at" \| "left-right" \| "up-down" \| "don't rotate"` |
| `current-costume` | `number` |
| `variables` | `{ [variableName: string]: any; }` |
| `lists` | `{ [listName: string]: Array<any>; }` |
| `scripts` | [`Array<ScriptObj>`](http://localhost:3000/save-format/sprites#scriptobj) |
| `custom-blocks` | `Array<CutomBlockScriptObj>` |
| `costumes` | `{ [fileName: string]: spriteName; }` |
| `sounds` | `{ [fileName: string]: spriteName; }` |

### ScriptObj
scripts are built from arrays  
the main script array is simply `[x, y, code]`  
the blocks them selves are `[blockID, ...inputs, mutation (optional)]`  
the inputs are the values of the blocks from the scratch interface, rather then the structure from blockly  
statement inputs are just arrays of more blocks, if there is a block inside an input it will also be an array (shaped the exact same as every other block)  
empty inputs are set with `null`

#### example of a script:
```json
[-33, 169, [
    ["event_whenflagclicked"],
    ["motion_pointtowards", "_random_"],
    ["control_forever", [
        ["motion_movesteps", 10],
        ["control_if", ["sensing_touchingobject", "_edge_"], [
            ["sound_play", "Low Boing"]
        ]],
        ["motion_ifonedgebounce"]
    ]]
]]
```
the above code will result in
<img src="/img/docimages/example_save_script.png" alt="Example of the resulting blocks from the above example"></img>
