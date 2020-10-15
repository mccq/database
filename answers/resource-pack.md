A resource pack is a folder or zip file that can modify assets like textures, models and translations.

### Layout
This is the general layout of a resource pack.
```
📁 resourcepacks
| 📁 <resource pack name>
| | 📄 pack.mcmeta (required)
| | 🖼️ pack.png
| | 📁 assets
| | | 📁 <namespace>
| | | | 📁 blockstates
| | | | 📁 font
| | | | 📁 lang
| | | | 📁 models
| | | | | 📁 block
| | | | | 📁 item
| | | | 📁 shaders
| | | | 📁 texts
| | | | 📁 textures
| | | | | 📁 block
| | | | | 📁 colormap
| | | | | 📁 effect
| | | | | 📁 entity
| | | | | 📁 environment
| | | | | 📁 font
| | | | | 📁 gui
| | | | | 📁 item
| | | | | 📁 map
| | | | | 📁 misc
| | | | | 📁 models
| | | | | 📁 painting
| | | | | 📁 particle
```

### Setup
We start by creating a folder `<resource pack name>` inside the `.minecraft/resourcepacks`. You can give this any name. [Don't know where you can find this folder?](https://minecrafthopper.net/help/finding-minecraft-data-folder/)

Now we create the `pack.mcmeta` file.
```json
{
  "pack": {
    "pack_format": 6,
    "description": "The description of your resource pack"
  }
}
```

Optionally you can add a `pack.png` file. It should have a square resolution, and will work best at 128×128 pixels.

To apply the resource pack go to "Options..." > "Resource Packs..." and select your resource pack. Click "Done" after moving it to the right side of the screen.

Every time you make changes in the resource pack, you need to press `F3 + T` to reload the changes.
