# Replicate Layout ULP
Replicates the PCB layout of a module.  
Inspired by the similar [replicate_layout](https://github.com/MitjaNemec/Kicad_action_plugins#replicate-layout) script made by Mitja Nemec for KiCad.  

This is an early implementation with some limitations, such as:
- Polygons do not get replicated yet.
- Sometimes replicated traces are not connected to their pad and leave a tiny airwire.
- This script only replicates traces of signals that are fully contained in the module and start with "MODULENAME:".
- When using nested modules, the script adds all possible layers of nesting levels to the list of available target modules.
Take extra care to select only the modules at the desired nesting level!
- The script my change the current layer, drill and wire bend setting.
- Special via configurations may not get replicated correctly.

# Important
This early version probably has some bugs and the script executes many commands which are tedious to undo.  
**==> Make sure to save your PCB before you execute the script!**

# Usage
Select one element with the 'Group' tool, then run the replicate_layout.ulp file.
The selected 'root' element will be the anchor point of the source layout.
Move the modules where you want the layout applied to the "Selected Target Modules" list.
All elements of each target module will get arranged around their same root element as in the source layout.

# Screenshots
![](./screenshots/Slideshow.gif?raw=true)
