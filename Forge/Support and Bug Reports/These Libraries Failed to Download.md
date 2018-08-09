---
layout: mc_default
---
# Libraries Failed to Download

If you encounter this error during the installation of your Forge Client or Server, try the following steps:

1. Use the Jar installer, not the Installer-Win Variant (Windows-Only, obviously)
2. Open a Command Prompt/Terminal Window
    * Windows:
        1. Open the folder in Windows Explorer/File Explorer
        2. With nothing selected, hold shift and right-click anywhere that won't select anything
        3. Click "Open Command Window Here" or "Open Powershell Window Here" (Only one of these will be available)
3. In the Window type: `java -Djava.net.preferIPv4Stack=true -jar [name of the installer].jar`, replacing [name of the installer] with the complete file name of the installer, including the .jar file extension.
    * In Powershell the above command will not work due to syntax differences, so you have two options:
        * Type cmd and press enter to switch to a Command Prompt that will use the existing Powershell window and use the command above as normal
        * Use this Powershell-Specific command: `Start-Process java -ArgumentList ("-Djava.net.preferIPv4Stack=true","-jar","[name of the installer]") -NoNewWindow`, again replacing [name of the installer] as above.
