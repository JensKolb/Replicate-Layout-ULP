# Replicate Layout ULP
Replicates the PCB layout of a module.  
Inspired by the similar [replicate_layout](https://github.com/MitjaNemec/Kicad_action_plugins) script made by Mitja Nemec for KiCad.  

This is an early implementation with some limitations, such as:
- **Only device positions are replicated!**
Wires, vias and polygons do not get replicated yet.
- The rotation and mirroring of each root element is not taken into account when the layout is replicated.
To circumvent this issue, you can place all root elements with the same rotation on the same side, replicate, select all elements of a group, then rotate or mirror the group.
- When using nested modules, the script adds all possible layers of nesting levels to the list of available target modules.
Take extra care to select only the modules at the desired nesting level!
- This early version probably has some bugs. **Make sure to save your pcb before you execute the script!**

# Usage
Select one element with the 'Group' tool, then run the replicate_layout.ulp file.
The selected 'root' element will be the anchor point of the source layout.
All elements of each target module will get arranged around their same root element as in the source layout.
