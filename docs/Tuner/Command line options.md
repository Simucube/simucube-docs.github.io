Tuner accepts a few command line arguments for allowing automating some actions and allowing profile switching using external applications. 

```
sc-tuner.exe [options] [profile file...]
  Launching secondary instance will pass the arguments to the primary instance

Options:
  profile file(s)         - Path to one or more profile files that should be imported to the local database.
  --start-all             - Start all connected devices. Works only when given to the secondary
                            instance. WILL CAUSE DEVICES TO MOVE.
  --load uuid1,uuid2..    - Load profiles using unique identifiers. Profile identifiers must be followed in comma separated list.
                            NOTE: Will overwrite any unsaved changes!
  --tray                  - Don't create a window. Only launch as a tray icon.
                            If given to secondary instance, then primary instance window won't be brought on top.
  --no-minimize-to-tray   - Close application once the main window is closed.
  --help                  - Print this information and exit.
  --version               - Print software version number and exit.

```

For safety reason (and regulations) --start-all option only allows starting pedals, when there is already Tuner instance running and Tuner is started with the option. This purposefully makes it harder to cause pedals to move without user interaction.

Passing path to profile will open up the import dialog. From there you can decide whether to import and optionally also active the profile. Follow the steps provided in the dialog.

## Create shortcut for profiles

1. Go to overview
2. Top left corner is a "hamburger" menu, click it and select "Create shortcut for profiles..." button.
	- All currently active profiles will be included in the shortcut.
3. Select the location where you want to save the shortcut file.
4. Now if the shortcut is clicked, Tuner is started if it isn't already running and included profiles are activated. Test that it works correctly.
5. Use keyboard manufacturer's software, Stream Deck or other tool that allows launching programs with external input and add mapping that launches the previously created shortcut, when a key is pressed.
6. `--start-all` option can also be added to start pedals if they aren't in active state already, but it is usually better to make separate shortcut for that functionality.
   - Right click the shortcut file and open its properties.
   - Add command line arguments to Target text input after the path to sc-tuner.exe
   - e.g. `"C:\Program Files\SimucubeTuner\sc-tuner.exe" --tray --start-all --load uuidacb0cc3c-34e9-47f3-ad22-4364849f5020`
   - Click ok


---




