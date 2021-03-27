# Latest Announcements
Regretfully, the latest [Adrenalin 2020 Edition 21.3.1 driver](https://drivers.amd.com/drivers/radeon-software-adrenalin-2020-21.3.1-win10-64bit-mar24.exe) has introduced a regression that leads to a crash in SteamVR in certain circumstances. We have identified the root cause and are working on the fix. In the meantime, if you are experiencing this crash, you can avoid it by following these simple steps:

- Open the c:\Users\<your user name>\AppData\Local\AMD\OpenVR\settings\settings.json file in a text editor, or if you are using the ReLive VR Web UI, navigate to the Streaming tab
- Set the EncoderResolution width and height (Encoder Resolution in the Web UI) to 1472x1472 for RX470/480/580/590/5500 and Vega/Radeon VII or 1600x1600 for RX5x00/6x00.
- Set the EyeResolution width and height (Render Resolution in the Web UI) to 1600x1600 for for RX470/480/580/590/5500 and Vega/Radeon VII or to 1900x1900 for RX5x00/6x00.
- Save the settings.json file or click on the Apply button in the Web UI.
- Restart SteamVR.
You can experiment with different values, just make sure that the values for Render Resolution are greater than the values for the Encoder Resolution.

We apologize for the inconvenience and are working to deliver the fix as quickly as possible.

# Radeon ReLive VR on Oculus Devices
ReLive VR must be sideloaded to Oculus devices due to Oculus Store policy restrictions. For Vive Focus/Focus Plus and Daydream-compatible devices, install the app from the respective appstore ([Viveport](https://www.viveport.com/mobileapps/a7bf3400-3652-4cc9-b2da-f0263e1c1f9d "Viveport") or [Google Play](https://play.google.com/store/apps/details?id=com.amd.wirelessgvr&hl=en_CA "Google Play")).

The following Oculus headsets are supported:
- Oculus Quest
- Oculus Go
- GearVR with Samsung Galaxy S7 or newer

General information about ReLive VR can be found at [Radeon ReLive VR page](https://www.amd.com/en/technologies/radeon-software-relive-vr "Radeon ReLive VR page")
ReLive VR requires a VR capable AMD graphics card, Windows 10 and 5GHz 802.11ac router. 
For best experience use [Adrenalin driver](https://www.amd.com/en/support "Adrenalin driver") v20.2.1 or newer (required for Oculus Rift Touch controllers emulation on Quest).

## Setup and Troubleshooting
[Setting Up ReLive VR](https://github.com/GPUOpen-LibrariesAndSDKs/Radeon-ReLive-VR/wiki/Setting-up-ReLive-VR)

For more information about configuring, using and [troubleshooting](https://github.com/GPUOpen-LibrariesAndSDKs/Radeon-ReLive-VR/wiki/Troubleshooting) ReLive VR please visit our [Wiki](https://github.com/GPUOpen-LibrariesAndSDKs/Radeon-ReLive-VR/wiki).
