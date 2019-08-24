---
layout: mc_default
---
# Finding Logs

When posting an issue on the Forge forums there usually isn't much anyone can do to help you if you do not provide logs.

**Forge Version 1.12.2-14.23.2.2629 and newer:**  
Post ``debug.log``

**Older versions:**  
Update

---

**Mojang Launcher:**  
When using the Mojang launcher one of these files will be found in [``.minecraft\logs``](https://minecraft.gamepedia.com/.minecraft#Locating_.minecraft").

**Twitch Launcher:**  
The Twitch Launcher's logging configurations override Forge's, follow these steps to get ``debug.log``:
1. Take note of the Forge version the pack uses as well as the location of the pack itself.
    * If you have not installed Forge manually, do so now with that version of Forge.
        * Disregard any <Unnamed Installation\> installations, they are bugged.
2. Locate your Twitch Launcher installation
3. Start the Minecraft Launcher located in the Install folder
4. Create a new Launcher Installation
    1. Select the correct version of Forge from the Version dropdown
        * Note: Pre-1.13 version of Forge get shoved to the bottom of the list
    2. Select the pack location as the Game Directory
5. Launch the pack by select your new installation and clicking play.
6. ``debug.log`` will now be generated in the logs folder of your modpack instance.

**Fallback ("No logs are generated"):**  
If you don't see logs generated in the usual place, provide the ``launcher_log.txt`` from <a href="https://minecraft.gamepedia.com/.minecraft#Locating_.minecraft">``.minecraft``</a>