# News and Interests feature in windows 10
This article will describe how to disable or change the News and Interests feature in windows 10.

Microsoft has introduced a new feature on windows 10 named News and Interests as part of KB5003214 update.
This can cause additional network traffic and take up valuable space on your taskbar, bellow are some of the options to change its behaviour.  

### Manualy

Right-click the Taskbar and select **“News and Interests -> Turn off”** option to hide or remove the icon from Taskbar.


### Group Policy

Configure the following setting and select the **Disabled** option.

    Computer Configuration / Administrative Templates / Windows Components / News and interests

Note: As this is a computer side policy a reboot is needed.


### Registry 

Feeds registry hive settings are located under: 
        
        HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Feeds

To turn off the feeds without disabling it (useful if you want to give the users the ability to re-enable it)

change/create a new **DWORD(32-bit)** named **ShellFeedsTaskbarViewMode** and set the value to **2**

To show only the icon without text.

change/create a new **DWORD(32-bit)** named **ShellFeedsTaskbarViewMode** and set the value to **1**

To show icon and text.

change/create a new **DWORD(32-bit)** named **ShellFeedsTaskbarViewMode** and set the value to **0**
