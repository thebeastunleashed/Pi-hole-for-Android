# Pi-hole for Android
**Pi-hole for ARMv7 (2011 and newer) Android devices.**

![IMG_2229](https://user-images.githubusercontent.com/33142753/133272103-28c6eba3-d1f7-4e29-9c5b-7d96d9f94e9e.jpg)

Pi-hole is a Linux network-level advertisement and Internet tracker blocking application which acts as a DNS sinkhole intended for use on a private network. It is designed for low-power embedded devices with network capability, most well-known being the Raspberry Pi.

This customized [Linux Deploy](https://play.google.com/store/apps/details?id=ru.meefik.linuxdeploy&hl=en_US&gl=US) image works on any rooted Android device with an ARMv7 class (or newer) CPU.  This typically includes any devices made in the past 10+ years. Form factor is not important; it could be a phone, tablet, HDMI stick or **any device running Android**.

**Requirements:**

- Android device that has been rooted
- Developer Options -> Root Access -> **Enabled for Apps**

**Instructions:**

- Open web browser on device and download+install the two APKs below.  You can also download these from the Play Store if you prefer:

  - **https://github.com/meefik/linuxdeploy/releases/download/2.6.0/linuxdeploy-2.6.0-259.apk**

-  Download the Pi-hole for Android disk image: (**v1.2 / Sept 14, 2021**)

   - **http://desktopecho.com/p4a12.tar.gz** (MD5: e5b396d17b8dcf844962284aeabfa662)

- Open **Linux Deploy** and change ONLY these settings:
     -  Open Properties Menu (Bottom Right)
     -  Distribution: **rootfs.tar**
     -  Source Path - This varies depending on the device, ie: **${EXTERNAL_STORAGE}/Download/p4a12.tar.gz**
     -  Set password for user **android**
     -  Init -> **Enable**
 - Go back to main window, click **Options** Menu (Three dots, usually at top right of screen) and click **Install**
     -  Wait a few minutes while CentOS installs.  
     -  Allow the install to complete before proceeding to next steps.
     -  When install is complete, the Linux Deploy console window will show the following: 

        `````[HH:mm:ss] >>> :: Configuring core/launchroot ...`````
        
        `````[HH:mm:ss] >>> deploy`````
    -  If you see an errror message in the Linux Deploy console, you probably didn't enter the location of **p4a12.tar.gz** correctly.  **You need to fix this before you can continue.**
          
 - Open the 'Hamburger menu' (Three dashes at top left) and touch **Settings**
    -  Place checkmark on **Lock Wi-Fi**
    -  Place checkmark on **Autostart**
    
Touch the **[ > START ]** button and confirm. 

-----------------------------------------------------------
**INSTALLATION COMPLETE - PI-HOLE IS RUNNING ON YOUR ANDROID DEVICE!**

-----------------------------------------------------------
Your Android device's IP is shown at the top of the Linux Deploy main window.  You can interact with the Pi-hole instance in three ways:

 - Open a web browser to the Android device's IP address **-->** ```http://10.13.12.11/admin```

 - SSH to the instance on port 22 **-->** ```ssh android@10.13.12.11```

 - RDP to the device's IP address from a Windows machine **-->** ```mstsc.exe /v:10.13.12.11```

**Additional Info**

You can restart (or "bounce") the Pi-hole instance in Linux Deploy by pressing **[ STOP ]** and waiting a few seconds for the instance to indicate all services are stopped.  Restart the instance by pressing **[ > START ]**

When a Pi-hole instance starts up, the default setting is to let it automagically configure networking.  If you change networks on the Android device simply restart the instance for Pi-hole to pick up the new settings.

Alternatively, set a static assignment by commenting-out two lines in ```/etc/rc.local``` (You will see which ones when you open the file in an editor.)  After the lines are commented out with a hash "#" you can manually add your IP, subnet and interface name to ```/etc/pihole/setupVars.conf```

The Pi-hole instance on Android otherwise behaves like it is running on a 'real' Raspberry-Pi or a standard PC.  Consult the extensive documentation online to learn how to fully leverage Pi-hole's functionality.
