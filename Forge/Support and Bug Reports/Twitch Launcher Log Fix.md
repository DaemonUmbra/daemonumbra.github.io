---
layout: mc_default
---
# Twitch Launcher Log Fix

These instructions are Windows only, I need to do more research to get this working on other OS's

1. Find the version of Forge that the pack is using
2. Locate the JSON for this version in Curse's versions folder
3. Open that JSON and between the last line of text and the last curly brace ( } ), put this line: `"logging": {}`  
    e.g:
    ```json
    {
        "other stuff": "Blah blah blah",
        "mainClass":  "net.minecraft.launchwrapper.Launch"
    }
    ```

    to
    ```json
    {
        "other stuff": "Blah blah blah",
        "mainClass":  "net.minecraft.launchwrapper.Launch",
        "logging":  {}
    }
    ```
    Note the comma in the second one.
4. This is important, DO NOT LAUNCH THE PACK WITH TWITCH, use the batch file linked below, to do this:
    1. Put the batch file in /Curse/Minecraft/Install/, right next to Minecraft.exe
    2. Double click it and it should open the launcher with your most recent pack selected
    3. Run Minecraft as normal and Forge's logs should generate correctly

<a href="../../Downloadable Files/Open MC Here.bat" download>Download Open MC Here.bat</a>  
Open MC Here.bat contents:

```bat
minecraft.exe --workDir %~dp0
```

This batch file uses the same launch argument that Twitch does to tell Minecraft's launcher where to look for its files, as they are not in the standard location, however it does this without resetting the version JSONs to Twitch's slightly broken ones (they are missing one line that breaks Forge's logging).