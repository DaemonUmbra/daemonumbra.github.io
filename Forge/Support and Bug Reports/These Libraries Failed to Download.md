---
layout: mc_default
---
# Libraries Failed to Download
## This issue has been solved in later versions of the 1.12.2 installer.

If you encounter this error during the installation of your Forge Client or Server, try the following steps:

1. Use the Jar installer, not the Installer-Win Variant
2. Open a Command Prompt/Terminal Window
    * Windows:
        1. Open the folder in Windows Explorer/File Explorer
        2. With nothing selected, hold shift and right-click anywhere that won't select anything
        3. Click "Open Command Window Here" or "Open Powershell Window Here" (Only one of these will be available)
3. The command:
    * If using CMD:
        ```bat
        java -Djava.net.preferIPv4Stack=true -jar <name of the installer>
        ```
        replacing `<name of the installer>` with the complete file name of the installer, including the .jar file extension.
    * If using Powershell, you have two options:
        * Type cmd and press enter to switch to a Command Prompt that will use the existing Powershell window and use the command above as normal
        * Use this Powershell-Specific command:
            ```powershell
            Start-Process java -ArgumentList ("-Djava.net.preferIPv4Stack=true","-jar","<name of the installer>") -NoNewWindow
            ```
            again replacing `<name of the installer>` as above.
