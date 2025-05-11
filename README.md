# JetsOfTimeTravel
Jets of Time Randomizer for Handheld Devices

## Setup and Use Instructions

### Assumptions
- Assuming you have a Chrono Trigger rom (legally obtained) and have it working on a hand held...
- Assuming you have the ability to run pygames (anbernic devices already setup to do this)...

### Setup
- Update the `snes_rom_path` to be the absolute path to your snes rom folder.  The Chrono Trigger rom should be in this folder
- Update the `rom_file` to match the file name of the Chrono Trigger rom
- Do a `gitsubmodule update --init`, since `jetsoftime` is a dependency
- scp the entire JetsOfTimeTravel repo into the pygame folder on the device
- Update the game list on the device (or restart the device)
- Run `jetsoftime` game on the pygame menu
- This will launch the GUI interface.

### Usage
- On the left side are different menu buttons, when selected will bring up different option buttons
- There are presets available, when selected will auto populate the settings to the presets.  These can then be further edited
- In general, go through the different menu categories to configure the different randomizer options
- The capability is good to generate randomized runs for most use cases, but does not have the same capabilities of the desktop or web applications
- If more customization is desired, generate the roms using desktop/web applications and scp them to handheld
