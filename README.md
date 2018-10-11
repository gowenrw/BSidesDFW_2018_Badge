# BSidesDFW_2018_Badge
BSidesDFW 2018 Badge Design Files

This design is based on the Throwing Star LAN TAP by Michael Ossmann <mike@ossmann.com>
More information about that design is located here:
http://greatscottgadgets.com/

The PCB requires the following components to make it a functional LAN TAP:
* 4x RJ45 Connectors: Amphenol RJHSE-5080 (unshielded) or RJHSE-5380 (shielded)
* 2x 220pF through-hole capacitors with .1" lead spacing (e.g. Xicon 140-50P2-221K-RC)

The original KiCad design files that were sourced by Michael Ossmann are from 2011 and used an older version of Kicad.
This caused many library errors when trying to read the files in a more recent version of KiCad.

To minimize the library errors I used KiCad version 4.0.7 which has a similar library structure to the original and then I found the few older files it was looking for as well.  Then, once I had it working I copied all the libraries used to local files in the project directory and rewrote the schematic and pcbnew configurations to call these local libraries.  Hopefully this allows it to be read and used in later versions of KiCad without issue.

Here is the layout of the project directory:
* ./ - The root directory contains the main KiCad files for the project
  * <filename>.pro: project file. Holds parameters that apply to the entire project (schematic and PCB layout).
  * <filename>.sch: schematic file.
  * <filename>.kicad_pcb: the new PCB layout file.
  * <filename>.net: netlist in "Pcbnew" format
  * <filename>.bak: backup of schematic file.
  * <filename>.kicad_pcb-bak: backup of the new PCB layout file.
  * <filename>-cache.lib: a local cache copy of all the symbols used in the schematic
  * fp-lib-table: Footprint library list
* ./lib_sh - This directory contains schematic library files
  * <filename>.lib: schematic symbols library file.
* ./lib_fp - This directory contains footprint module directories
  * <dirname>.pretty: footprint module directory
    * <filename>.mod: footprint module file
* ./3d_models - This directory contains footprint 3d model files
  * <filename>.wrl: VRML 3D model used in the 3D viewer to represent parts.
* ./gerber - This directory contains gerber formatted files for manufacturing
* ./datasheets - This directory contains datasheets for components in the design
* ./images - This directory contains images of the design exported from KiCad
* ./pdf - This directory contains pdf documents of the design exported from KiCad

This is what the badge will look like for conference attendees (red pcb):

![Alt text](/images/BSidesDFW_2018_Badge-RED-FRONT.png?raw=true "Front")
![Alt text](/images/BSidesDFW_2018_Badge-RED-BACK.png?raw=true "Back")

Staff and Speakers and Sponsors will all have different colored badges.
Examples of these different colored badges are in the images directory.

As always it was a blast to work on a new badge.
  
-- [@alt_bier](https://twitter.com/alt_bier)
