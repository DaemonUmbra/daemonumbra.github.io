---
layout: mc_default
---
# Twitch Launcher Log Fix

These instructions are Windows only, I need to do more research to get this working on other OS's

1. Take note of the Forge version the pack uses and close the Twitch launcher as well as any open Mojang launcher instances
2. Locate your Twitch Launcher installation
3. Locate the "versions" folder
4. Locate the folder corresponding to the version of Forge that your active pack uses
5. That folder will have a JSON file, in that file you will need to insert this line: "logging":{}
    - Note that at least one comma will be required to keep the JSON valid.
        -  If this is added as the first line the comma will close off the line.
        -  If this is at the end the previous line will need to be closed off with a comma.
        -  If this is put in the middle then both commas will be needed.
6. DO NOT LAUNCH THE PACK WITH TWITCH
7. Use the appropriate script to launch Minecraft by putting it next to the Mojang launcher executable and running the script
    -  These scripts use the same launch argument Twitch does, however they will not undo our changes to the version JSON.
        -  Windows: <a href="../../Downloadable Files/Open MC Here.bat">Open MC Here.bat</a>
        -  Mac: [Coming Soon]
8. The log files will be in ``\Documents\[Twitch or Curse]\Instances\[Pack Name]\logs``

Open MC Here.bat contents:
```bat
minecraft.exe --workDir %~dp0
```