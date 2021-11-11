# godot-blender-bvh-importer

## Blender (BVH) Importer Addon for Godot

This addon for Godot will automatically import any `.bvh` file in your project directory.

![JfbaPTM1eA](https://user-images.githubusercontent.com/32321/141242591-1496cbbd-18d5-429e-bba3-449ed9db0daf.gif)

Changes to the file will be automatically picked up, and your scene updated.

## How to Use:


**TL,DR**:

- Add this addon to your Godot `addons` directory, activate it, and make sure the Blender path is correct in project settings.
- Now bvh files in the project directory magically auto-import and auto-update


**Longer Version**:

You will need Godot 3.4 and Blender 2.93.5

Beware: Godot Engine through Steam has sandboxing issues. Try official versions on [itch.io](https://godotengine.itch.io) or [Github](https://github.com/godotengine/godot/releases/tag/3.4-stable).

1. Open this project in Godot Engine 3.4. (or add the `addons` directory to your project)
2. May not be needed: Go to <kbd>Project Settings > Plugins</kbd> and make sure the plugin `BVH` is activated.
3. May not be needed: Go to <kbd>Project Settings > General > Filesystem > Import > Blender</kbd> (or just search for `blender` at the top) and make sure the path to Blender is set. If Blender is in your global path (for example, if you use [scoop](https://scoop.sh/) to install Blender, or you are on Linux/Mac), you can just leave the default `blender`.
4. Save bvh files to the project folder.
5. Switch to Godot, and see the bvh file getting auto-imported
6. From the imported file, you can now create an inherited scene (double click the file and Godot will propose to create an inherited scene for you).

If you change your bvh file, remember to close your inherited scene in Godot (without saving it), or else you won't be able to see the changes.

## Known Bugs

- It seems the editor can sometimes hang on exit if scenes are left open and unsaved
- If a scene is open, and the bvh file is updated, changes will not be reflected until the scene is reopened (known Godot limitation)
