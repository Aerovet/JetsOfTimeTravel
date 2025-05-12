# JetsOfTimeTravel
Jets of Time Randomizer for Handheld Devices

Credit to all the developers of the [jetsoftime](https://github.com/Pseudoarc/jetsoftime/tree/master) repo who have done all the hard work of developing the core capability of the Chrono Trigger randomizer. The JetsOfTimeTravel application is simply a GUI interface that implements the `jetsoftime` randomizer so that seeds can be generated locally on a handheld device.  The GUI does not currently implement all the options of available in the `jetsoftime` randomizer, but allows for presets, as well as game mode adjustment, difficulty settings, item/shop configuration, and optional game flags. This project is still in its early stages of development and has only been tested on a limited set of devices.  However, this application should be able to run on any handheld device which has pygame support or EmulationStation as its front end.  Here are some steps to get you started:

## Setup and Use Instructions

### Requirements
- Chrono Trigger rom that is compatable with `jetsoftime`.
- Handheld which supports pygame or EmulationStation as its front end.
- Handheld which can run the Chronot Trigger rom (shouldn't be a problem).

If you are new to handhelds, and need some good primers on where to get started on setting up your handheld to run SNES roms or EmulationStation, "Good Russ" from [Retro Game Corps](https://retrogamecorps.com/category/guides/) most likely has you covered.  


### Setup (To be updated once a release is available)
- Clone the `JetsOfTimeTravel` repo on a local PC.
- Run command `git submodule update --init`.
- Open up `jetsoftime.pygame` in a text editor and update the following:
    - Update the `snes_rom_path` to be the absolute path to your snes rom folder on your handheld.  The Chrono Trigger rom should be also be in this folder.
    - Update the `rom_file` to match the file name of the Chrono Trigger rom within the `snes_rom_path`.
- Transfer the entire JetsOfTimeTravel repo into the pygame folder on the device.
    - Can be done via `scp -r JetsOfTimeTravel <handheld device address>`
- Update the game list on the device (or restart the device).
- Run `jetsoftime` game on the pygame menu to launch the application.

### Usage
- The application is relatively simple.  It consists of two columns of buttons, the left are different menu buttons, the right are different option buttons for the selected menu button.
- Default settings are loaded on initialization, but there are several presets available, such as `Race` and `Lost Worlds`.  These are the same presets which are available in the standard `jetsoftime` applications.  Once a preset is selected, it can be further editted by navigating to the different menu options.  Keep in mind that if you customize all option, and then select a new preset, everything will revert back to the preset settings.  Its best to set the presets first before proceeding with remaining randomizer settings.
- Utilizing the randomizer assumes some familiaraty with the randomizer options in general.  If you need more information on what each randomizer settings does, refer to the [Jets Of Time wiki](https://www.wiki.ctjot.com/doku.php?id=flags).
- Once all randomizer settings are entered, select the `Generate` menu button to generate the rom.  During rom generation, menu navigation is locked.  Depending on the device, rom generation can take up to about 10-30 seconds.  When the rom is generated, to the right of the `Generate` button blue text will show the name of the rom to indicate that generation is complete.  Once this text disapears, menu navigation will be unlocked.
- Multiple roms can be generated in one session.
- Once finished, exit the application and update the device gamelist (or restart) so that the generated roms are recognized.
- Fire up your jetsoftime seed, safe travels!

### Limitations
- Not all randomizer options are available at this time, such as customing boss randomization pool, or mystery setting probabilities.  If you require this level of customization, then the rom should be generated off the standard `jetsoftime` applications then transfered to the handheld device.
- The GUI does not have force flags capability for forcing flags back on.  However, it does force flags off if certain options are selected.  If selecting a flag does not do anything, its because another flag is blocking it from being selected.
