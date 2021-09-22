# Important Announcements
You asked and we listened! We're happy to announce a beta release of ReLive VR 2.0 which supports streaming from the headset's built-in microphone. You can download it [here](https://github.com/GPUOpen-LibrariesAndSDKs/Radeon-ReLive-VR/releases/tag/2.0.0-beta). This release contains many internal changes and at this point might not be as stable as version 1.0. We have received great feedback from the community for ReLive VR v1 so far, so we're making the beta release of ReLive VR 2.0 publically available in the hope of receiving the same great feedback on it as well - and we will work diligently to iron out any bugs that you report. At this point we are distributing it through Github only, the Sidequest listing still refers to v1.0.26 for the time being.

Please note the following:
- The latest [Adrenalin driver v21.9.2](https://drivers.amd.com/drivers/non-whql-radeon-software-adrenalin-2020-21.9.2-win10-64bit-sep21.exe) is required by ReLive VR 2.0
- Support for Oculus Go and GearVR has been dropped in v2.0 since these 3DoF devices do not provide an optimal user experience, have been out of production for a long time and represent a very small percentage of devices used with ReLive VR. We apologize for any inconvenience to the owners of these devices - you can still continue to use ReLive VR v1.0 with them.
- To enable microphone support, edit the %LOCALAPPDATA%\AMD\OpenVR\settings\settings.json file and change the "Microphone" setting in the "Headset" section to _true_ and restart StreamVR if it is running already. Select the "AMD Streaming Audio Device" as the microphone used by the game in your game settings.

Starting with Adrenalin driver 21.9.1 Quest2 users who use their headsets at 120fps refresh rate (must be enabled in the Quest2 Settings menu) can benefit from using a higher bitrate used for video encoding, which can now be set to as high as 170Mbps (previously capped at 100Mbps). You can set it either through the Web UI, or by editing the settings.json file manually. This applies to both v1.0 and v2.0 of the client app. Please note that we cannot guarantee stable streaming at such a high bitrate in all cases as it depends on your router and your RF environment, so your mileage might vary. If you experience frequent frame drops, image corruption or audio break-up, try lowering the bitrate until streaming becomes stable.

We want to thank all ReLive VR users for your patience and looking forward to your feedback on v2.0! 

# Radeon ReLive VR on Oculus Devices
ReLive VR must be sideloaded to Oculus devices due to Oculus Store policy restrictions. For Vive Focus/Focus Plus devices, install the app from the ([Viveport](https://www.viveport.com/mobileapps/a7bf3400-3652-4cc9-b2da-f0263e1c1f9d "Viveport") appstore.

The following Oculus headsets are supported:
- Oculus Quest
- Oculus Quest2

General information about ReLive VR can be found at [Radeon ReLive VR page](https://www.amd.com/en/technologies/radeon-software-relive-vr "Radeon ReLive VR page")
ReLive VR requires a VR capable AMD graphics card, Windows 10 and 5GHz 802.11ac router. 
For best experience use [Adrenalin driver](https://www.amd.com/en/support "Adrenalin driver") v20.2.1 or newer (required for Oculus Rift Touch controllers emulation on Quest).

## Setup and Troubleshooting
[Setting Up ReLive VR](https://github.com/GPUOpen-LibrariesAndSDKs/Radeon-ReLive-VR/wiki/Setting-up-ReLive-VR)

For more information about configuring, using and [troubleshooting](https://github.com/GPUOpen-LibrariesAndSDKs/Radeon-ReLive-VR/wiki/Troubleshooting) ReLive VR please visit our [Wiki](https://github.com/GPUOpen-LibrariesAndSDKs/Radeon-ReLive-VR/wiki).
