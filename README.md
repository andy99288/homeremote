# Home Remote Integration for Hubitat

Until an API connection can be made between Home Remote and Hubitat, these files are available for use and hopefully someone with coding skills can modify them to make them better.

At this point, these instructions are very limited.   If there is interest in working on this project, or people find the instructions to be vague they will be updated.  Please leave all comments on the Hubitat community thread. 

1) The hubitatapp code should be pasted into the Apps Code section of Hubitat.  OAuth needs to be enabled. 
2) Add the user app in Hubitat under the Apps section. 
3) Select the devices you want to use in Home Remote (note that the system can handle a lot more device types than initially shown, they have just been commented out of the app code as I don't have these device types and have no idea if they work correctly.) 
4) Done/Ok your way out of the app.  Then, in another window, bring up the hubitat log.  Leave it open and go back into the app.  Select the "Connection Info" button at the bottom of the page to show the info you need to make the connection in your log.  It may not work the first time - you can try the refresh token button in the app to get a new token in case it hasn't been created yet, and/or going back in and out of the app until you get the necessary info in the log.  
5) Goto http://thehomeremote.com/ and get the designer software.  
6) To set up the connection in Home Remote designer, right click on devices found in the explorer, add a new source, plugin, and give it a name (Hubitat would be appropriate).
7) When the script page pops up, paste the code from the pluginscript found on this page and save it.   
8) Right click on the new hubitat device in explorer, cick open, and enter the settings.  This is where you put the connection info.   You need to add an item with "URL" for name. The type will already be filled with "PluginSetting", and under Value put the hubitat URL you got from the log.  Create a second item for "AccessToken" and put the bearer token in the value field.  Save all this. 
9) Go back to the explorer, right click on devices, and choose Sychronize Devices.  The devices you authorized in Hubtitat should show up. 
10) Start designing! See http://thehomeremote.com/ for documentation/community forums.   Basically, you add a control and assign its state to a device you have added.   

The app and or connection between the two needs improvement.  An API interface would be preferrable.   Right now, and I'm looking for help developing it, the HTTP connection you set up above is a bit slow and seems to bog down the hubitat if you add a lot of devices.  

This app was based on, and still shows the original header information, for The Home Remote app for SmartThings.  
