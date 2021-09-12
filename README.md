# Pi-hole-for-Android
Pi-hole for ARMv7 (2011 and newer) Android devices.

Requirements:

- Android device, rooted
- In Developer Options -> Root Accees -> Enabled (Apps and ADB)
- Open browser on device and downalod+install the two APKs below.  You can also download these from the Play Store if you prefer:

  - https://github.com/MrBIMC/SELinuxModeChanger/releases/download/11.0/app-release-v11.apk
  - https://github.com/meefik/linuxdeploy/releases/download/2.6.0/linuxdeploy-2.6.0-259.apk

-  Download the Pi-hole for Android disk image (**v1.1** / Sept 13, 2021):

   - http://desktopecho.com/p4a11.tar.gz (MD5: 21a7662f81b8ccf6d4c11d8db8963e23)

- Restart Phone (This is **REQUIRED!**)

- Open SElinux Mode Changer:  Set to "Permissive" and "Automatically Start on Boot"
- Open Linux Deploy
     -  Open Properties Menu (Bottom Right)
     -  Distribution: rootfs.tar
     -  Source Path - This varies depending on the device, ie: ${EXTERNAL_STORAGE}/Download/p4a11.tar.gz
     -  Set password for user "android"
     -  Init -> Enable
 - Go back to main window, click Options Menu (Three dots, top right of screen) and click "Install" 
     -  Wait a few minutes while CentOS installs.  
     -  Allow the install to complete before proceeding to next steps.
     -  When install is complete, the Linux Deploy console window will show the following: 

        `````[HH:mm:ss] >>> :: Configuring core/launchroot ...`````
        
        `````[HH:mm:ss] >>> deploy`````
         
   
 - Open Hamburger Menu (Top Left) and touch "Settings"

    -  Place checkmark on "**Lock Wi-Fi**"
    -  Place checkmark on "**Autostart**"
 
Touch the **-> START** button and confirm when prompted. 

**Pi-hole is now ready to use.**  
 
Your Android device's IP is shown at the top of the Linux Deploy main window.  You can iteract wih the Pi-hole instance in three ways:

 -  Open a web browser to the Android device's IP address.  Example: ```http:10.13.12.11/admin```

 -  SSH to the instance on port 22.  Example: ```ssh -p 2222 android@10.13.12.11```

 -  RDP to the device's IP address to open an XTerm.  Example ```mstsc.exe /v:10.13.12.11```
