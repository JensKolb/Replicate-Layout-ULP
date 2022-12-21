# Replicate Layout ULP
Replicates the PCB layout of a module.  
Inspired by the similar [replicate_layout](https://github.com/MitjaNemec/Kicad_action_plugins#replicate-layout) script made by Mitja Nemec for KiCad.  

This is an early implementation with some limitations, such as:
- Polygons do not get replicated yet.
- Special via configurations may not get correctly replicated.
- Sometimes replicated traces are not connected to their pad and leave a tiny airwire.
- When using nested modules, the script adds all possible layers of nesting levels to the list of available target modules.
Take extra care to select only the modules at the desired nesting level!
- The script my change the current layer, drill and wire bend setting.
- This early version probably has some bugs. **Make sure to save your PCB before you execute the script!**

# Usage
Select one element with the 'Group' tool, then run the replicate_layout.ulp file.
The selected 'root' element will be the anchor point of the source layout.
All elements of each target module will get arranged around their same root element as in the source layout.
