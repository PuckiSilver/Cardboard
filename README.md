# Cardboard
**Package data packs with resource packs as mods for Forge, Fabric and Quilt**

## Prerequisits
1. You need to have [Python](https://www.python.org/downloads/) installed
2. Install [PyYaml](https://pyyaml.org) using
   ```cmd
   pip install PyYaml
   ```

## Packaging a data pack
1. Make sure that your data pack is a `.zip`-file with the `pack.mcmeta` in the **top-most level**
2. Both the `data` **and** `assets` folder should also be in the **top-level** of the zip-file
3. Drag the data pack's **zip-file onto** [`cardboard.py`](cardboard.py)
   - optionally select the zip-file and a [config-file](#config), applying both directly
4. Follow the instructions in your terminal

In the same location as your data pack, a jar-file with the same name will be created

This is the data pack packaged as a mod that works with Forge, Fabric and Quilt

> **Note**: Loading the mod using Fabric or Quilt requires [Fabric API](https://modrinth.com/mod/fabric-api) or [Quilted Fabric API](https://modrinth.com/mod/qsl)

## Config
When converting a data pack, you will be prompted to provide some more information to be included in files for the mod loaders

| Config option | Default | Explanation |
| - | - | - |
| name | Filename | The human readable name of your pack |
| id | Filename with limited charset | The internal unique name of your pack |
| description | Description in pack.mcmeta | A short description |
| version | 1.0.0 | The version of the pack |
| authors | empty | Who made the pack, separate multiple using commas |
| license | All rights reserved | A license or a link to a license |
| homepage | empty | The packs homepage or projectpage |
| issues | empty | A link to the issue tracker of this pack |
| sources | empty | A link to the open sources of this pack |

You can also provide a `.yml`- or `.yaml`-file that includes these options as keys

Any key that is not included in the config will be set to it's default
