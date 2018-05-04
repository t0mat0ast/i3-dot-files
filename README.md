# i3-dot-files

some basic changes to i3 and i3blocks file to get a working status bar and multimedia keys for brightness and volume. Use a package called light with the i3 config to change brightness with multimedia keys.

place the files in .config folder in /home.

If tap to click isnt working then do :: 

     Check out the xinput command. xinput list will give you a list of input devices; find the ID of the one which looks like a touchpad. Then do xinput list-props <device id>, which should tell you what properties you can change for the input device. You should find one called something like Tapping Enabled and a number in parens after it (e.g : libinput Tapping Enabled (276). Finally, run xinput set-prop <device id> <property id> 1, and tapping should work.

To make the change permanent, find a way to run that command on startup. One way would be to add exec xinput set-prop <device id> <property id> 1 to ~/.i3/config.
