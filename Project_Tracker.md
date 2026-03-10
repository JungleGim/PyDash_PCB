# PyDash PCB - Project Tracker
project tracker for WIP issues, what's currently being worked on, and anything that may need to move to the actual README file

## Version
Version: 2.0a - TBD
Build Date: N/A

# WIP Version TODO list
## HDMI
* TMDS pairs in each HDMI channel shall have matching lengths of ± 3mm.
	- currently out of spec (by a lot, 69 vs 78).
	- TODO: equalize lengths between pairs

## Misc
* Updated BOM
	- Generate the final BOM with updated part nubmers and sources where appropriate

# Development Finishing
* radius PCB edges
	- The current PCB has simplied square edge cuts. For some reason the latest KiCad release was unable to export the bord as an STL with the radiused edges, even when snapping to the connection points
	- For now, a simplified squared outline and cutout were used to aid in developing the enclosure
	- Before finalization, the edges should be radiused

# Future Updates
Include any items below in the appropriate README.md file section
(none)

* JLC PCB stackups for TDMS impedence considerations
	- JLC04121H-3313 Stackup – 1oz (0.035mm) outer layer
		+ Chosen stackup option
		+ Top to inner 1 and inner 2 to bot separation is 0.1
		+ requires 0.18mm trace width for single-ended impedence target
		+ 0.3mm separation for differential impedence target
	- Other options for notes:
		+ JLC04121H-7628 - 1oz (0.035mm) outer layer
			* Top to inner 1 and inner 2 to bot separation is 0.2
			* requires 0.3mm trace width for single-ended impedence target
			* 0.25mm separation for differential impedence target
		+ JLC04121H-1080 Stackup – 1oz (0.035mm) outer layer
			* Top to inner 1 and inner 2 to bot separation is 0.0764
			* requires 0.13mm width
			* 0.20mm separation for differential impedence target