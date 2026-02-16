# PyDash PCB - Project Tracker
project tracker for WIP issues, what's currently being worked on, and anything that may need to move to the actual README file

## Version
Version: 2.0a - TBD
Build Date: N/A

# WIP Version TODO list
## HDMI
The below are design updates that need to be performed for the HDMI related components
* Each TMDS signal shall have single ended impedance of 50 Ω ± 10%	
	- Current is 0.2mm which is over impedance on a 0.2mm stackup
	- TODO: update trace width as its own preset. Consider one of the below based on the available stack-ups
		+ JLC04121H-7628 => requires 0.3mm width
		+ JLC04121H-3313 => requires 0.18mm width
		+ JLC04121H-1080 => requires 0.13mm width
	- Notes:
		+ JLC04121H-7628 Stackup – 1oz (0.035mm) outer layer
			* Top to inner 1 and inner 2 to bot separation is 0.2
		+ JLC04121H-3313 Stackup – 1oz (0.035mm) outer layer
			* Top to inner 1 and inner 2 to bot separation is 0.1
		+ JLC04121H-1080 Stackup – 1oz (0.035mm) outer layer
			* Top to inner 1 and inner 2 to bot separation is 0.0764

* Each TMDS pair shall have differential impedance of 100 Ω ± 5%.
	- Current is 0.2/0.25 which is over differential impedance on a 0.2mm spaced stackup
	- TODO: update pair spacing as its own preset
	- Notes on available 100ohm differential stack-up options:
		+ JLC multilayer 1oz outer
			* 0.1mm width and 0.1mm separation minimum – 2 layer
			* 0.09mm width and 0.09mm separation - multilayer
		+ JLC04121H-7628
			* 0.3mm width + 0.25mm separation
		+ JLC04121H-3313
			* 0.18mm width + 0.25mm separation (barely in spec)
			* 0.18mm width + 0.4mm separation
		+ JLC04121H-1080
			* 0.13mm width + 0.2mm separation

* TMDS pairs in each HDMI channel shall have matching lengths of ± 3mm.
	- currently out of spec (by a lot, 69 vs 78).
	- TODO: equalize lengths between pairs

## Misc
* Updated BOM

# Development Finishing
(None)

# Future Updates
Include any items below in the appropriate README.md file section
(none)