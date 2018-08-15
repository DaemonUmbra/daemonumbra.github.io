---
layout: mc_default
---
# Failed to Bind to Port

This message shows when a server is unable to bind to its designated port on your computer/server.
The most common cause is another server is running or did not properly shut down and is still technically bound to that port.

To check for programs running on the desired port:

(Windows)

1. Open Powershell
2. Enter this command, replacing `[Port]` with your port number:
```powershell
Get-Process -Id (Get-NetTCPConnection -LocalPort [Port]).OwningProcess
```
    * If red text appears then Powershell can't see any processes running on that port and it is probably safe to try running the server again ONCE.
    * If you actually get a result then you should have the PID and Name of the process occupying the port
3. If you wish to kill this process (only do this if you are sure), use this command, again replacing `[Port]` with your port number:

```powershell
Stop-Process -Id (Get-NetTCPConnection -LocalPort [Port]).OwningProcess
```
or more simply, use the PID you got from the previous result:
```powershell
Stop-Process -Id [PID from earlier]
```