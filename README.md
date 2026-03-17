# PyDash_PCB - Information
This readme covers the printed circuit board or PCB portion of the PyDash. For the App design, Enclosure design, or OS design, see the below repositories:
- [PyDash_OS](https://github.com/JungleGim/PyDash_OS)
- [PyDash_App](https://github.com/JungleGim/PyDash_App)
- [PyDash_PCB](https://github.com/JungleGim/PyDash_PCB)
- [PyDash_Enclosure](https://github.com/JungleGim/PyDash_Enclosure)
- [PyDash_Builder](https://github.com/JungleGim/PyDash_Builder)

## Introduction
The PyDash_PCB is a daughter board that contains the hardware required for a rPi compute module (CM4) to function as a processor to display information on a 7in screen.

Additional details on the design considerations, required packages, and key features are included in the "Methodology" section of this readme.

# Project Status
## Revlog
- Rev 0: 06/02/2024
	- Initial issue
- Rev1a: 05/19/2025
	- Fixed button numbering to be appropriate when viewing the screen
- Rev2a: 02/15/2026
	- updates realted to Rev2.0a rebuild - includes new features and code architecture
	- Added micro SD socket for users to load dash config files
	- Updated USB port to USBC
	- Removed touch lines from screen and removed USB mux - no plans to utilize touch in future
	
## Future Development
The below is a list of wants/needs for future revisions; loosely listed in order of importance.

- Update mounting holes for CM4 to solder pads for use of solder-on standoffs to attach CM4
- Scope out board assembly cost

# Methodology
## History
TBD: quick detail starting with the arduino + daughter board on the 5in display as a proof of concept

## Key Considerations and Constraints
The following sections are some notes on the various considerations or any constraints when designing the display.

### Power Supply
As built, with the sourced display and components in the BOM, the display uses approximately 350-400mA when operation, at 100% backlight.

### Display
The chosen display is a 7inch 1024x600 IPS display sourced from waveshare [link](https://www.waveshare.com/70h-1024600.htm?sku=22671). The display is fastened to the carrier PCB via double-sided foam tape. The 40pin FPC jack directly connects to the HDMI output from the CM4.

To control the backlight via PWM, drive the "BL_en" pin high. The PWM signal is scaled from 1024 (100%) to 0 (0) for brightest to darkest.

Any HDMI compatable display should be able to be used with this design. While the FPC cable was a design choice, any other HDMI connection should be appropriate, depending on the chosen display.

Additional considerations for the HDMI hardware and driver configuration is contained in the "PyDash OS" readme.

#### PCB stackup
JLC PCB stackups for TDMS impedence considerations

* Chosen stackup: JLC04121H-3313 – 1oz (0.035mm) outer layer
	+ Chosen stackup option
	+ Top to inner 1 and inner 2 to bot separation is 0.1
	+ requires 0.18mm trace width for single-ended impedence target
	+ 0.3mm separation for differential impedence target

* Other available options with calculated requirements
	+ JLC04121H-7628 - 1oz (0.035mm) outer layer
		* Top to inner 1 and inner 2 to bot separation is 0.2
		* requires 0.3mm trace width for single-ended impedence target
		* 0.25mm separation for differential impedence target
	+ JLC04121H-1080 Stackup – 1oz (0.035mm) outer layer
		* Top to inner 1 and inner 2 to bot separation is 0.0764
		* requires 0.13mm width
		* 0.20mm separation for differential impedence target

# Known bugs and bug fixes
No current known bugs

# FAQ section
No current FAQ

# Copyright and licensing information
## GNU GPLv3
This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program.  If not, see <https://www.gnu.org/licenses/>.

## Additional disclaimer
The information included is provided "as is", without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose and non-infringement. In no event shall the authors or copyright holders be liable for any claim, damages or other liability, whether in an action of contract, tort or otherwise, arising from, out of or in connection with the software or the use or other dealings in the software or tools included in this repository.

# General Notes and References
While I am an engineer by trade, my area of focus is not computer architecture or system engineering. Likely some people have already looked at various aspects of the codebase and just shook their heads. That being said, I've compiled a list of considerations and notes for the project that have helped me along the way. These are listed below, in no particular order.

## References
Throughout the project, I have used many references, related to various aspects/items of the project. These are all compiled in the list below, in no particular order
- TBD any notable references
