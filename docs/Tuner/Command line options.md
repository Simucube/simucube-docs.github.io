Tuner accepts a few command line arguments for allowing automating some actions and allowing profile switching using external applications. 

```
sc-tuner.exe [options] [<profile file>]
	Launching secondary instance will pass the arguments to the primary instance

Options:
	profile file  - Path to profile file that should be switched to
	                Note that using this to swich profile will discard
	                any changes to the currently active profile
	--start-all   - Start all connected devices. Works only when given to the secondary
	                instance. WILL CAUSE DEVICES TO MOVE.
	--tray        - Don't create a window. Only launch as a tray icon.
	-h/--help     - Print this information and exit.
	-v/--version  - Print software version number and exit.
```

For safety reason (and regulations) --start-all option only allows starting pedals, when there is already Tuner instance running and Tuner is started with the option. This purposefully makes it harder to cause pedals to move without user interaction.

Passing path to profile will cause that profile to be imported, and then Tuner will immediately switch to that profile, discarding all changes to the previously selected profile. If the given profile file is older than or the same as previously imported version of the profile, the file is only used to find the correct profile, but it isn't actually used. This avoids the need to re-export changed profiles for purposes of automated profile switching.

## How to implement hotkeys for switching between profiles

1. Export the profiles that you want to use to some local directory with descriptive names. For hotkey purposes it might be good idea to name exported profile files by names refering to the hotkeys (eg. `hotkey_1.td2p`) so switching the profile opened by the hotkey is easy by simply exporting some other profile and overwriting the file.
2. Create shortcut that starts the Tuner with correct options
   - Copy SimucubeTuner shortcut from desktop to some other directory and rename it
   - Right click it and open its properties.
   - Add command line arguments to Target text input after the path to sc-tuner.exe
   - `"C:\Program Files\SimucubeTuner\sc-tuner.exe" --start--all "C:\Users\Simucube\hotkey_profiles\hotkey1.td2p"`
   - Click ok
3. Now if the shortcut is clicked when Tuner is already open, pedals are started and hotkey1.td2p profile is activated. Test that it works correctly.
4. Use keyboard manufacturer's software, Stream Deck or other tool that allows launching programs with external input and add mapping that launches the previously created shortcut, when a key is pressed.




