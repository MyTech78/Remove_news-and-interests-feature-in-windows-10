# News and Interests feature in windows 10
This article will describe how to remove the News and Interests feature in windows 10

Microsoft has intrucdced a new feature on windows 10 nameed News and Interrests as part of KB5003214 update.

## Manual Disable

Right-click the Taskbar and select “News and Interests -> Turn off” option to hide or remove the icon from Taskbar.

## Group Policy

Configure the folowing key and select the **Disabled** option.

    Computer Configuration -> Administrative Templates -> Windows Components -> News and interests

Note: as this is a computer side policy a reboot is nedded.

## Registry 

Create a new key named **Windows Feeds** under the bellow reg path.  

    HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows
    
Create a new **DWORD(32-bit)** under the Windows Feeds key named **EnableFeeds** and set its value to **0** to disable News and Interests feature.     









