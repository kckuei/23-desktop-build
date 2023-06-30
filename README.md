# '23 Desktop Build Notes

## Summary
* Objective: construct a faster rig with dedicated GPU for running some DEM simulations and CUDA/ML fun

In summary, 

* I used PCpartsPicker to choose the parts & check compatibility
* Assembly in ~2 evenings, with ~2 more evenings for debugging and getting up and running
* Time consuming parts were figuring out how to route the cables and debugging blank screen/boot issues
* Running Ubuntu 22.04 on it
* I lo0ve the light show! Might needs some curtains!

![Purdy](/assets/PXL_20230630_040008904.jpg)


### Build

Here's the parts [list](https://pcpartpicker.com/user/kckuei/saved/#view=DVDh99):

* Intel Core i9-13900K 3 GHz 24-Core Processor
* Gigabyte B660M DS3H AX DDR4 Micro ATX LGA1700 Motherboard
* Corsair iCUE H150i ELITE CAPELLIX 75 CFM Liquid CPU Cooler
* (2) G.Skill Trident Z RGB 64 GB (2 x 32 GB) DDR4-3600 CL18 Memory
* Samsung 980 Pro 2 TB M.2-2280 PCIe 4.0 X4 NVME Solid State Drive
* NVIDIA Founders Edition GeForce RTX 4080 16 GB Video Card
* Corsair AX1600i 1600 W 80+ Titanium Certified Fully Modular ATX Power Supply
* Corsair iCUE 4000X RGB ATX Mid Tower Case

### Learnings/Troublehsooting

* Blank screen on boots
	* Did you forget the CPU power cable? : )
	* Monitor cable needs to be connected to the GPU (if present), not mobo
	* Power connector to the GPU needs to be securely attached
	* Also, seems sensitive to bends in the cable
	* For debian systems, make sure you select the option for installing proprietary drivers when installing the kernel (would have saved me a lot of time)
* Unable to reflash kernel
	* Did you remember to actually save the BIOS settings before exiting? : )
	* \<DEL\> on boot to enter
* Why are there so many RTX cards under different manufacturers?
	* Appparently when NVIDIA develops a card, they license it out to other MFGs to build, which is good for competition and consumers.
	* These cards can come in their own flavors, and might be optimized or stylized differently. 
	* MFG's have their own rep when it comes to reliability and RMA processes as well, so you get to choose! 

