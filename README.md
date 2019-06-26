# Radeon ReLive VR on Oculus Devices
ReLive VR must be sideloaded to Oculus devices due to Oculus Store policy restrictions. For Vive Focus/Focus Plus and Daydream-compatible devices, install the app from the respective appstore ([Viveport](https://www.viveport.com/mobileapps/a7bf3400-3652-4cc9-b2da-f0263e1c1f9d "Viveport") or [Google Play](https://play.google.com/store/apps/details?id=com.amd.wirelessgvr&hl=en_CA "Google Play")).

The following Oculus headsets are supported:
- Oculus Quest
- Oculus Go
- GearVR with Samsung Galaxy S7 or newer

General information about ReLive VR can be found at [Radeon ReLive VR page](https://www.amd.com/en/technologies/radeon-software-relive-vr "Radeon ReLive VR page")
ReLive VR requires a VR capable AMD graphics card, Windows 10 and 5GHz 802.11ac router. 
For best expirience use [Adrenalin driver](https://www.amd.com/en/support "Adrenalin driver") v19.6.2 or newer (required for Oculus Rift Touch controllers emulation on Quest).
## Enabling Radeon ReLive VR on the PC
Ensure that Radeon ReLive components of Adrenalin driver are installed. Install them during driver installation or, if the driver is already installed, do the following:
- Ensure that Steam and SteamVR are installed on the PC.
- Start Radeon Settings.
- Click on the *ReLive* tab at the bottom of the Radeon Settings window and toggle the *ReLive* switch ON.
- Install ReLive if prompted.
- Click on the *Game & VR Streaming* tab in Radeon Settings and toggle the *SteamVR Integration* switch ON.
- Start SteamVR.
- Perform Room Setup for Standing Experience. When prompted to calibrate the floor, enter your height in either centimeters or inches (170cm or 67" work well for most people).

## Side-loading the ReLive VR app on Oculus Quest and Oculus Go
- Set up the headset and create an Oculus account (most likely you have already done this)
- Install the *Oculus* app on your smartphone or tablet from Google Play or Apple Appstore
- Register as Oculus Developer. On your PC go to the  [Oculus Developer Dashboard](https://dashboard.oculus.com "Oculus Developer Dashboard") and click on the *Create New Organization* button. Add your Oculus account as a developer to the organization you have created.
- Open the Oculus mobile app, select your Oculus Quest or Go headset and go to the *Settings* tab. Tap on *More Settings* and enable *Developer Mode* (if you do not see the *Developer Mode*  option, try rebooting your phone). Restart your headset.
- On your PC [download](https://developer.oculus.com/downloads/package/oculus-go-adb-drivers/ "download") the Oculus USB driver. Once the download finishes, extract the zip file into a folder and install the driver by right-clicking on the *android_winusb.inf* file and select *Install* from the pop-up menu.
- Download [ADB, the Android Debugger](https://developer.android.com/studio/releases/platform-tools "ADB, the Android Debugger") and unzip it to a folder on your PC.
- Connect your headset to the USB port of your PC.
- Download the latest ReLive VR [APK file](https://github.com/GPUOpen-LibrariesAndSDKs/Radeon-ReLive-VR/raw/master/ReLiveVR-Oculus-1.0.11.apk "APK file") from this repo.
- Navigate to the folder where you unzipped ADB in Windows Explorer, and type `cmd` + Enter in the address bar. This will open the command prompt window. In this window type the `adb install -r <path to apk>` command and hit the *Enter* key. Replace `<path to apk>` with the actual path where you have downloaded the ReLive VR apk. For example, if you downloaded *ReLiveVR-Oculus-1.0.8.apk* to *C:\Users\JohnDoe\Downloads*, the command should look like this: `adb install -r "c:\Users\JohnDoe\Downloads\ReLiveVR\ReLiveVR-Oculus-1.0.8.apk"`. This will install the ReLive VR app onto your headset. You should see the "Success" message once the loading process is complete.
- In your headset select *Library* and then *Unknown Sources*. Reboot the headset if *Unknown Sources* does not appear under *Library*.
- Now you should be able to see and launch the AMD ReLive VR application.

## Side-loading the ReLive VR app on GearVR
- Dock the phone into the GearVR headset and follow the on-screen prompts to install the Oculus software (most likely you have done this already).
- Copy the latest ReLive VR [APK file](https://github.com/GPUOpen-LibrariesAndSDKs/Radeon-ReLive-VR/raw/master/ReLiveVR-Oculus-1.0.11.apk "APK File") to your phone using any method (USB, download via Google Drive, Dropbox, etc).
- Install the [Injector for GearVR app](https://play.google.com/store/apps/details?id=com.zgsbrgr.gearvr.injector&hl=en_CA "Injector for GearVR app") on your phone. Launch the Injector app and tap on *SELECT APK*. Navigate to the location where you have placed the ReLive VR APK and tap on it. Follow the on-screen prompts to install the ReLive VR app.
- Launch the app and dock the phone into the GearVR headset.

## Configure the PC for Oculus Quest
Radeon ReLive VR emulates a wired headset, making VR applications think that they are working with HTC Vive, HTC Vive Pro or Oculus Rift and the corresponding controllers. While GearVR and Oculus Go come with a single 3DoF (degrees of freedom) hand controller that are best emulated as Vive controllers, Oculus Quest is shipped with two 6DoF controllers that resemble the Oculus Touch controllers very closely. Therefore, we recommend to configure your PC to emulate Oculus Rift for Quest and Vive or Vive Pro for Go and GearVR. By default ReLive VR will emulate the HTC Vive headset.
To change the headset being emulated, follow these simple steps:
- Open Windows Explorer, type `cmd` and press *Enter* in the address bar. Once the command prompt window opens, type the following command `echo %LOCALAPPDATA%` and hit *Enter*. It will print the path to your local user data folder - take a note of it. 
- In Windows Explorer, click on the *View* tab and check the *Hidden items* checkbox. Navigate to the folder you noted in the previous step, find the *AMD\OpenVR\settings* folder and right-click on the *settings.json* file inside (if the folder or the file isn't there, just enable *SteamVR Integration* in Radeon Settings and start SteamVR). Select *Open with* from the menu and open the file with *Notepad*.
- In the "*Application*" section find the line that reads `"HeadsetProfile" : "HTC Vive",` and change "*HTC Vive*" to "*Oculus Rift CV1*", preserving case and spaces. Save the file and restart SteamVR.

## Configure the WiFi Connection
You will need a Wireless-AC 5GHz router with a Gigabit Ethernet LAN port to use ReLive VR. Wireless-N or 100Mbps Ethernet **do not** provide enough throughput for good wireless VR experience.
- Connect the PC to the LAN port of your 5GHz router with an Ethernet cable (Cat-6 is recommended).
- Configure your headset/phone to connect to the 5GHz SSID of your router. AC routers broadcast at least two (sometimes more) distinct SSIDs - one for the 2.4GHz band and one (or more) for the 5GHz one. The 5GHz SSIDs are usually denoted by the '5', '5G' or 'AC' suffix in the default name.

## Running the App
- Start SteamVR on your PC. If you are running it for the first time, Windows Firewall might ask to allow incoming traffic to SteamVR/vrserver.exe. Allow it for the network type you're using (Private, Domain or Public).
- Start the ReLive VR for Oculus app on your headset. You might have to wake up your controller(s) by pressing the Oculus button on it. The headset would find the PC on the network and connect automatically. You should find yourself in SteamVR Home.

## Controller Emulation and Button Mappings

Oculus Quest controllers' keys map to Oculus Touch controls one-to-one.

GearVR and Oculus Go controllers have less buttons than the Vive controllers. The following limitations apply:
- Controller position is emulated using the elbow model
- The *grip* button of the Vive controller is not available on GearVR/Go controllers
- A click on the top edge of the trackpad maps to the press of the *System* button on the original Vive controller
- A click on the bottom edge of the trackpad maps to the press of the *Menu* button on the original Vive controller
- There is no analog *trigger* button. Games requiring analog trigger might have limited functionality
- The *Back* button on the GearVR/Go remote exits the app
