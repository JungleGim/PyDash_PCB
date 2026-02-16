# PyDash_PCB - Information
This readme covers the printed circuit board or PCB portion of the PyDash. For the App design, Enclosure design, or OS design, see the below repositories:
- [PyDash_PCB](https://github.com/JungleGim/PyDash_PCB)
- [PyDash_App](https://github.com/JungleGim/PyDash_App)
- [PyDash_OS](https://github.com/JungleGim/PyDash_OS)
- PyDash_Enclosure
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

- USB port is routed but not functional; app design requires additional features
- Update mounting holes for CM4 to solder pads for use of solder-on standoffs to attach CM4
- Scope out board assembly cost

# Methodology
## History
TBD: quick detail starting with the arduino + daughter board on the 5in display as a proof of concept

## Key Considerations and Constraints
TBD: power supply and other notes (approx 350mA draw when running)
TBD: PWM backlight notes
TBD: display notes (especially different considerations)

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
