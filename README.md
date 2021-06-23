# News and Interests feature in windows 10
This article will describe how to remove the News and Interests feature in windows 10

Microsoft has introduced a new feature on windows 10 named News and Interests as part of KB5003214 update.

### Manualy

Right-click the Taskbar and select **“News and Interests -> Turn off”** option to hide or remove the icon from Taskbar.


### Group Policy

Configure the following setting and select the **Disabled** option.

    Computer Configuration / Administrative Templates / Windows Components / News and interests

Note: As this is a computer side policy a reboot is needed.


### Registry 

Create a new reg key named **Windows Feeds** under the bellow reg path.  

    HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows
    
Create a new **DWORD(32-bit)** under the Windows Feeds key named **EnableFeeds** and set the value to **0**   
