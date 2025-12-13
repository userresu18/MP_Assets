# Instructions for Houdini and Unreal Workflow

## Disclaimer:
- Only works currently for one character at once, but you could export separately multiple with the same workflow.

---

## Houdini Side

1. **Install** `CrowdExport_clean.hda`.
2. Set the **import type** to `Dopnet` if you have a dop crowd or `agents` if you have a sop crowd.
3. Set the **Agents or Dop path** to the path in the previous step.
4. Set the **Export directory** where the animation files and JSON will be saved.
5. Set the **animation naming**. It will be numbered like: `MyAnimName_1`, `MyAnimName_2`, etc.
6. Press **Render**. This will export each animation separately and a JSON data file.
7. Export your crowd character separately (for example, using the Rop Fbx character output node, animation is not needed, just the skeletal mesh).

---

## Unreal Side (5.1+)

1. Go to **Edit → Plugins** and enable the **JSON Blueprint Utilities** plugin.
2. Copy the `EUWBP_Crowd.uasset` to anywhere in the content folder.
3. **Import the crowd character** you are simulating.
4. Create a **new folder for the animations**.
5. **Import the animations** from the export folder to this new folder, setting the skeleton to your character's skeleton.
6. Create a **Blueprint** and add a skeletal mesh component to it, then set the skeletal mesh parameter to your character.
7. Find **EUWBP_Crowd**, right-click, and run the **Editor Utility**. A window will pop up.
8. Set the **Target Character Asset** to the newly created one.
9. Set the **Crowd JSON Path** to the Houdini export folder's JSON file.
10. Set the **Crowd Animation Content Folder** to the folder where you imported the animation files.
11. Press **Import** and set the **Sequencer Path and Name**.
12. Open the **Sequencer** and press **Play**.

---

