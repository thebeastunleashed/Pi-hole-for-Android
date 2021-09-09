# Pi-hole-for-Android (Don't use this! WiP...)
Pi-hole for ARMv7 (2011+) Android phones 

Assumptions:

- Old Android Phone, rooted
- Developer Options -> Root Accees -> Enabled (Apps and ADB)
- Open Android Web Browser, Go to 'github.com/desktopecho/Pi-hole-for-Android'
- Install APKs and Download image:

  - https://github.com/MrBIMC/SELinuxModeChanger/releases/download/11.0/app-release-v11.apk
  - https://github.com/meefik/linuxdeploy/releases/download/2.6.0/linuxdeploy-2.6.0-259.apk
  - http://desktopecho.com/p4a10.tar.gz (MD5: 23f32cdf1bb57c6396de0d87b3b52ed5)

- Restart Phone
- Open SElinix Mode Changer:  Set to "Permissive" and "Automatically Start on Boot"
- Open Linux Deploy
     -  Open Properties Menu (Bottom Right)
     -  Distribution: rootfs.tar
     -  Enter location of image (Typically /Downloads/p4aXX.tar.gz)
     -  Set password for user "android"
     -  Init -> Enable
 - Click Options Menu (Three dots, top right of screen) and click "Install" 
     -  Wait a few minutes while CentOS is installed.
   
 After installation is successful click START
 
Your Android device's IP is shown at the top of the Linux Deploy main window.
From your PC, open a VNC connection to your device's IP on port 5900. 
Example: ```vncviewer.exe 10.73.0.111:5900```

 
