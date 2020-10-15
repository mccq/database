Using scores on items is a bit more difficult. For security reasons you can't use the score text component in item NBT.

We can use the `set_name` and `set_lore` functions in a loot table.
```json
{
  "pools": [
    {
      "rolls": 1,
      "entries": [
        {
          "type": "minecraft:item",
          "name": "minecraft:diamond",
          "functions": [
            {
              "function": "minecraft:set_name",
              "name": [
                "Points: ",
                { "score": { "name": "@s", "objective": "points" }}
              ]
            },
            {
              "function": "minecraft:set_lore",
              "lore": [
                "Line 1",
                "Line 2"
              ]
            }
          ]
        }
      ]
    }
  ]
}
```

Now we can use the `loot` command to get the item in the game.
```mcfunction
loot give @a loot <loot table>
```
