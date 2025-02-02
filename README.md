# ZMK Configuration Template
Bluetooth firmware configuration for Cyboard keyboards using ZMK firmware.
More information can be found here: [ZMK Documentation](https://zmk.dev/docs).

# Get Set Up
1. Click "[use this template](https://github.com/new?template_name=zmk-user-config-template&template_owner=Cyboard-DigitalTailor)" to create a copy of this repository for your own use.
2. Replace `config/imprint.keymap` with the appropriate default from `config/default keymaps/` based on the physical layout of your board.
3. Commit and push the changes, and verify that the default firmware builds properly.

# Changing your Keymap

### ZMK Studio
1. Navigate to [zmk.studio](https://zmk.studio)
2. Make changes, which are instantly applied.
> 💡 **Note:** changes made with ZMK Studio will **not** be backed up to your repository, but rather stored on your keyboard.  This is the easiest method of changing layouts quickly, but if you want to directly edit the code later with the other methods, you may need to re-make your layout, as there is not yet a way to export the configuration from Studio back into firmware source files.

### ZMK Keymap Editor
1. Navigate to [nickcoutsos.github.io/keymap-editor/](https://nickcoutsos.github.io/keymap-editor/)
2. Sign into github and link to this repository.
3. Make changes to the layout and press "Commit Changes."
[more information can be found here](https://github.com/nickcoutsos/keymap-editor/wiki/Features)

### Directly edit text files in this repository
1. Make the desired edits to `config/imprint.keymap`, commit, and push them.

# Flashing the firmware to your Cyboard
1. GitHub will automatically run an Action to build your firmware when you push changes. this takes approximately 2 minutes for most changes.
2. Once the Action is successful, there will be a firmware Artifact in the Action which you can download and unzip.
3. Connect the "central" (left) half of your Cyboard to your computer via USB.
4. Put your Cyboard in bootloader mode by double tapping the reset button next to the USB C port. Pro Tip:  The keycap puller that comes with your Cyboard will fit in the reset hole!
5. Copy the .uf2 file into the USB device named `ASSIMILATOR`.
6. You're done! You can now disconnect your Cyboard from your computer.

# Hardware Notes for Older Versions Using nice!nanos:
The battery switch is a physical disconnect switch, so your battery **will not charge** if the switch is off (away from the USB port).  The switch is intended as a way to disconnect the battery for travel to avoid accidental keypresses that would drain the battery while it is in your bag.  For most other times, it can just be left connected (towards the USB port), and your Cyboard will sleep after 15 minutes of inactivity to conserve battery.
