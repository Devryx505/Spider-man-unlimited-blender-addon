# SMU Toolkit

> A Blender addon for importing, editing, and injecting BDAE model files (support 0,0,0,934 version of bdae).

![Blender](https://img.shields.io/badge/Blender-4.0%2B-orange?logo=blender&logoColor=white)
![Version](https://img.shields.io/badge/Version-1.0.2-blue)
![License](https://img.shields.io/badge/License-All%20Rights%20Reserved-red)

---

## Overview
community: (https://discord.gg/5y2grpaZ6M)

SMU Toolkit lets you work with BDAE files directly inside Blender. Pull out a mesh, edit it however you want, and write your changes back into the original file  without touching anything the addon doesn't need to.

It handles the parts that actually matter for modding: geometry, skeletons, skinning weights, and materials. Everything else in the file is left exactly as it was.

---

## Features

- **Import**  Brings in mesh geometry, armature, skinning weights, UVs, and material data
- **Inject**  Writes your edits back into the BDAE with automatic `.bak` backups before every write
- **Pre-flight check**  Validates your scene against the original file before you commit anything
- **Material editing**  Edit material names, render modes, and texture assignments per mesh
- **Size-change support**  Handles meshes where vertex or index counts have changed
- **Non-destructive**  Unknown file sections are always preserved

---

## Installation

1. Download the latest `.zip` from [Releases](https://github.com/Spider1Toaster/Spider-man-unlimited-blender-addon/releases)
2. Open Blender and go to `Edit → Preferences → Add-ons`
3. Click **Install** and select the downloaded `.zip`
4. Enable **SMU Toolkit** from the list

The panel shows up in the **N sidebar** under the **SMU** tab.

---

## How to Use

### Importing a model
1. Open the **SMU** tab in the N sidebar
2. Expand **Import**
3. Toggle **Apply Skin on Import** if you want the bind pose applied
4. Click **Import BDAE** and pick your file

### Injecting edits back
1. Expand **Inject**
2. Set the **Original** path to your source BDAE
3. Set the **Output** path where the modified file should go (or use the duplicate button to auto-fill it)
4. Adjust write options to match what you changed
5. Hit **Pre-flight** first to catch any issues, then **Inject**

### Materials
Select a mesh with a material assigned and expand **Active Material** to edit its BDAE name, render mode, and texture slots.

### Output Log
Expand **Output Log** after any operation to see what happened  errors, warnings, and what was written. The **Dump Debug JSON** button exports a full data snapshot if you need to dig deeper.

---
| Option | What it does |
| :--- | :--- |
| **Allow Size Changes** | Handles meshes where vertex or index counts differ from the original |
| **Write Skeleton** | Writes bone transforms from your edited armature rest pose |
| **Write Proportions** | Exports mesh coordinates as a new rest shape and refreshes skin matrices |
| **Write Materials** | Writes material names, render modes, and texture pointers |

---

## Credits

Made by **Spider toaster**,**Devryx** and **Spidey129**

---

## License

All rights reserved. You may use this addon for personal modding purposes and share links to the original release page.

You may **not** redistribute, modify, repackage, or claim credit for this work without written permission from the authors. If you want to contribute or collaborate, reach out first.

See [LICENSE](./LICENSE) for the full terms.
