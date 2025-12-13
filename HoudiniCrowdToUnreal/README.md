Disclaimer:

Only works currently for one character at once, but you could export separately multiple with the same workflow.

Houdinin side

1. Install CrowdExport_clean.hda
2. Set the import type to Dopnet if you have a dop crowd or agents if you have a sop crowd
3. Set the Agents or Dop path to the path in the previous step
4. Set the Export directory where the animation files and json will be saved
5. Set the animation naming. It will be numbered like: MyAnimName_1, ..._2
6. Press render. It will export each animation separately and a json data file.
7. Export your crowd character separately. (Rop Fbx character output node for example, animation not needed just the skeletal mesh)

Unreal side 5.1+

1. Go to edit->plugins and enable json blueprint utilities plugin, copy the EUWBP_Crowd.uasset to anywhere in the content folder
2. Import the crowd character you are simulating. 
3. Create a new folder for the animations.
4. Import the animations from the export folder to this folder setting the skeleton to your characters skeleton.
5. Create a blueprint and add a skeletal mesh component to it and set the skeletal mesh parameter to your character.
5. Find EUWBP_Crowd right click and run editor utility. Window will pop up
6. Set the target character asset to the newly created one
7. Set the Crowd json path to the houdini export folder's json file
8. Set the Crowd andim content folder to the folder you imported the anim files
9. Press Import and set the sequencer path and name. 
10. Open the sequencer and play it.