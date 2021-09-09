# Pi-hole-for-Android
Pi-hole for ARMv7 (2011-) Android phones 

Assumptions:

- Old Android Phone, rooted
- Developer Options -> Root Accees -> Enabled (Apps and ADB)
- Open Android Web Browser, install APKs and Download image:

  - https://github.com/MrBIMC/SELinuxModeChanger/releases/download/11.0/app-release-v11.apk
  - https://github.com/meefik/linuxdeploy/releases/download/2.6.0/linuxdeploy-2.6.0-259.apk
  - http://desktopecho.com/p4a10.tar.gz (MD5: 23f32cdf1bb57c6396de0d87b3b52ed5)

- Restart Phone (This is **REQUIRED!**)

- Open SElinux Mode Changer:  Set to "Permissive" and "Automatically Start on Boot"
- Open Linux Deploy
     -  Open Properties Menu (Bottom Right)
     -  Distribution: rootfs.tar
     -  Source Path - Usually ${EXTERNAL_STORAGE}/Download/p4a10.tar.gz
     -  Set password for user "android"
     -  Init -> Enable
 - Go back to main window, click Options Menu (Three dots, top right of screen) and click "Install" 
     -  Wait a few minutes while CentOS installs.  
     -  Allow the install to complete before proceeding to next steps.
     -  When install is complete, the Linux Deploy console window will show the following: 

        ```[HH:mm:ss] >>> :: Configuring core/launchroot ...```
        
        ```[HH:mm:ss] >>> deploy```
         
   
 - Open Hamburger Menu (Top Left) and touch "Settings"

    -  Place checkmark on "**Lock Wi-Fi**"
    -  Place checkmark on "**Autostart**"
 
Touch the **-> START** button and confirm when prompted. 

**Pi-hole is now ready to use.**  
 
Your Android device's IP is shown at the top of the Linux Deploy main window.
From your PC, open a web browser to the Android device's IP, or SSH to it on port 2222.
Example: ```ssh -p 2222 android@10.13.12.11```

