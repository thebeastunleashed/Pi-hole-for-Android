# Pi-hole-for-Android (Don't use this! WiP...)
Pi-hole for old (ARMv7) Android phones

Assumptions:

- Old Android Phone, rooted
- Developer Options -> Root Accees -> Enabled (Apps and ADB)
- Open Android Web Browser, Go to 'github.com/desktopecho/Pi-hole-for-Android'
- Install APKs:

  https://github.com/MrBIMC/SELinuxModeChanger/releases/download/11.0/app-release-v11.apk
  https://github.com/meefik/linuxdeploy/releases/download/2.6.0/linuxdeploy-2.6.0-259.apk

- Restart Phone
- Open SElinix Mode Changer:  Set to "Permissive" and "Automatically Start on Boot"
- Open Linux Deploy
     -  Open Properties Menu (Bottom Right)
     -  Distribution: CentOS
     -  Set password for user "Android"
     -  Init -> Enable
     -  GUI -> Enable
     -  GUI -> Desktop Environment -> XTerm 
 - Click Options Menu (Three dots, top right of screen) and click "Install" 
     -  Wait a few minutes while CentOS is installed.
   
 After installation is successful click START
 
Your Android device's IP is shown at the top of the Linux Deploy main window.
From your PC, open a VNC connection to your device's IP on port 5900. 
Example: ```vncviewer.exe 10.73.0.111:5900```

 
