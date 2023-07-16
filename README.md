# 2023 Desktop Build

## Summary

Built for some light gaming and simulations. Dual boot Windows 10 and Ubuntu 22.04. [PCPartsPicker's List](https://pcpartpicker.com/user/kckuei/saved/#view=DVDh99)

### Build

![Purdy](/assets/PXL_20230630_040008904.jpg)

* Intel Core i9-13900K 3 GHz 24-Core Processor
* Gigabyte B660M DS3H AX DDR4 Micro ATX LGA1700 Motherboard
* Corsair iCUE H150i ELITE CAPELLIX 75 CFM Liquid CPU Cooler
* G.Skill Trident Z RGB 64 GB (4 x 32 GB) DDR4-3600 CL18 Memory
* Samsung 980 Pro 2 TB M.2-2280 PCIe 4.0 X4 NVME Solid State Drive
* NVIDIA Founders Edition GeForce RTX 4080 16 GB Video Card
* Corsair AX1600i 1600 W 80+ Titanium Certified Fully Modular ATX Power Supply
* Corsair iCUE 4000X RGB ATX Mid Tower Case


### Troublehsooting Notes & Learnings

* Windows 10 Device and Driver Issues
	* Was unable to detect Wi-Fi and PCI devices, and some unknown devices on Windows 10
	* Used device manager > Properties > Hardware ID, then googled the values to find applicable drivers
	* Uknknown devices resolved by installing additional Intel IO/serial drivers
	* To resolve the PCI device issues, I had to update the BIOS from F6 to F23 using @BIOS as Q-FLASH did not work (see [unique features](https://download.gigabyte.com/FileList/Manual/mb_manual_b660-features_n.pdf?v=b1238bb211fec3e5947e111a76c13c62) for more info)
	* To resolve Wi-Fi device issues, I had to install [Gigabyte WLAN+BT AMD WIFI driver](https://www.gigabyte.com/Motherboard/B660M-DS3H-AX-DDR4-rev-1x/support#support-dl) and [Intel Wi-Fi Drivers for Wireless Adapters](https://www.intel.com/content/www/us/en/download/19351/windows-10-and-windows-11-wi-fi-drivers-for-intel-wireless-adapters.html) 
* Ubuntu 22.04 Freeze on Boot from GRUB Issues
	* Kept freezing on the following: [    4.323420] noveau 0000:01:00.0: unknown chipset
	* From GRUB, I was able to select Advanced Ubuntu options and select a Kernel in recovery mode, then resume booting normally
	* In Additional Drivers, changing from Noveau open-source to Nvidia 525 proprietary fixed the issue
	* This is a pretty useful/informative thread for related issues [thread](https://askubuntu.com/questions/162075/my-computer-boots-to-a-black-screen-what-options-do-i-have-to-fix-it)
* Blank screen on boots
	* Monitor cable needs to be connected directly to the GPU if present
	* For debian systems, make sure to installing proprietary drivers when installing the kernel
* Unable to reflash kernel
	* \<DEL\> on boot to enter
	* Changes to BIO settings need to be saved before exiting
* Wow, SSDs are tiny!
 


Yay, DEM!
![yade](/assets/yay-dem.gif)
