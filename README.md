<p align="center"><img src="https://github.com/K3V1991/How-to-flash-Android-Kernel-and-Recovery/blob/main/Flash.png" width="200"></a>
<h1 align="center"><b>How to flash a Android Kernel and Recovery with ADB & Fastboot</b></h1>
<br />

<p align="center">
<a href="https://liberapay.com/K3V1991" alt="LiberaPay"><img src="https://img.shields.io/badge/Liberapay-F6C915?style=for-the-badge&logo=liberapay&logoColor=black" /></a>
<a href="https://ko-fi.com/k3v1991" alt="Ko-fi"><img src="https://img.shields.io/badge/Ko--fi-F16061?style=for-the-badge&logo=ko-fi&logoColor=white" /></a>
<a href="https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=HW8B98TVDLKWA" alt="PayPal"><img src="https://img.shields.io/badge/PayPal-00457C?style=for-the-badge&logo=paypal&logoColor=white" /></a>
<a href="https://github.com/K3V1991/Donate-Crypto/blob/main/README.md" alt="Crypto"><img src="https://img.shields.io/badge/Bitcoin-000?style=for-the-badge&logo=bitcoin&logoColor=white" /></a>
</p>
<hr />
<br />

## Requirements:
* Windows OS
* USB Driver for your Device or Universal ADB Driver
* Unlocked Bootloader
* ADB & Fastboot++ - [GitHub](https://github.com/K3V1991/ADB-and-FastbootPlusPlus)

## Enable Developer Options & USB Debugging:
1. Install the USB Driver for your Phone or Universal Adb Driver
2. On your Phone, go to Settings > About Phone. Find the Build Number and tap on it 7 times to enable Developer Options
3. Now enter ```System``` > ```Developer Options``` and find ```USB debugging``` and enable it
4. Plug your Phone into the Computer and change it from ```Charge only``` to ```File Transfer``` Mode
5. On your Computer, browse to the Directory where you extracted/installed ADB & Fastboot++ 
6. Use the Open CMD.bat or ADB & Fastboot++ Shortcut to launch a Command Prompt
7. Once you’re in the Command Prompt, enter the following Command:
```
adb devices
```
8. System is starting the ADB Daemon (If this is your first Time running ADB, you will see a Prompt on your Phone asking you to authorize a Connection with the Computer. Click OK.)
9. Succesful enabled USB Debugging

## Unable to connect to ADB:
1. AMD Bug - [XDA Thread](https://forum.xda-developers.com/t/fix-fastboot-issues-on-ryzen-based-pcs.4186321/)
2. Switch Device from "Charging" to "File Transfer" Mode
3. Install the latest Device Driver or Universal USB Driver
4. Try another USB Cable
5. Use another USB Port (USB 3.0 Port to USB 2.0)
6. Try to execute Fastboot Command without connecting your Phone and once it says "waiting for device" plug in your USB Cable
7. Windows: Click "Change advanced power setting" on your chosen Plan and expand "USB Settings". Under "USB Settings" Section, expand "USB selective suspend setting" and change it to "Disabled" for On Battery and Plugged In
8. Try another PC

## How-To:
1. Download and extract/install ADB & Fastboot++
2. Browse to the Directory where you extracted/installed ADB & Fastboot++
3. Place the Kernel or Recovery Image in the Tool Folder
4. Plug your Phone into the Computer
5. Launch a Command Prompt with the Open CMD.bat or ADB & Fastboot++ Shortcut
6. Once you’re in the Command Prompt, enter the following Command:
```
adb devices
```
and hit Enter

7. Rebooting the Device to Bootloader:
```
adb reboot bootloader
```
and hit Enter
<br />

## Flash Kernel:
```
fastboot flash boot <kernel file name>.img
```
and hit Enter
<br />

## Flash Recovery:
```
fastboot flash recovery <recovery file name>.img
```
and hit Enter

## Reboot to System:
```
fastboot reboot
```
and hit Enter
