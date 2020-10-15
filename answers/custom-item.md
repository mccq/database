To create a new item you need to re-use an existing item ID and give it a custom model and name. This is done with NBT and a resource pack for the custom model.

```mcfunction
give @s apple{CustomModelData:1,give:{Name:'{"text":"Banana","italic":false}'}}
```
This will give you a custom item, but it doesn't have a custom texture yet. You will need a [resource pack](@resource-pack).

Since the apple was used as item, you need to overwrite that item model in the resource pack.

Create a file `assets/minecraft/models/item/apple.json`. This file will tell the game that if an apple item has a custom model data of 1, it will use a different model: `minecraft:item/banana`.
```json
{
  "parent": "item/generated",
  "textures": {
    "layer0": "item/apple"
  },
  "overrides": [
    {
      "predicate": {
        "custom_model_data": 1
      },
      "model": "minecraft:item/banana"
    }
  ]
}
```

Then create the model file `assets/minecraft/models/item/banana.json`.
```json
{
  "parent": "item/generated",
  "textures": {
    "layer0": "minecraft:item/banana"
  }
}
```

The final thing is to add a texture for the item. This goes in `assets/minecraft/textures/item/banana.png`.
