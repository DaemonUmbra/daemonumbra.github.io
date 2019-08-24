---
layout: mc_default
---
# Libraries Failed to Download
### There are two common causes of this error, to determine which is yours, open the installer log and search for any mention of ``PKIX``, if there is one, you have the new issue.
---
### New Issue:
The new issue is fixed simply by installing a more recent version of Java.

---
### Old Issue:
1. Use the Jar installer, not the Installer-Win Variant
2. Open Powershell
3. Use this command:
    ```powershell
    Start-Process java -ArgumentList ("-Djava.net.preferIPv4Stack=true","-jar","<name of the installer>") -NoNewWindow
    ```
    again replacing `<name of the installer>` as above.
