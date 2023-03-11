This tutorial will show how to protect against BadUSB attacks by enabeling password promts when accessing administrator mode

From this:

![[run-as-adminPromt.webp]]

To this

![[run-as-adminPasswordPrompt.webp]]

### Configuration

We need to edit the windows registry. To do that open **registry editor**
The registry we are goint to edit is **ConsentPromptBehaviorAdmin**

The HKEY = `Computer\HKEY_LOCAL_MACHINE` if you want to config it for all users
The KEY = `SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System`

Full URL: ( Combined HKEY and KEY )
`Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System`

Then we need to set the value of `ConsentPromptBehaviorAdmin` to `1`
read more at [microsoft documentation](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-gpsb/341747f5-6b5d-4d30-85fc-fa1cc04038d4) 

![[admin-passwordPrompt-Registry-ConsentPromptBehaviorAdmin.webp]]

**YOUR DONE** try to run PowerShell as Administrator and see if it worked. 
