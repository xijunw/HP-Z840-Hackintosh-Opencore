# HP-Z840-Hackintosh-Opencore
Opencore configuration for Catalina 10.15.7 (Based on opencore 0.7.7, tested 0.7.8 works)

Here I am sharing the opencore configuration files of HP Z840 Hackintosh with Catalina. It should be works for you if you have a similar hardware configuration, or at least allow you to finish OS installation and have a start point from there.

Hardware
* Intel E5 2650 V3 x2
* Nvidia Quadro K4200 (Metal supported)
* SATA SSD through PCIe adaptor
* No NVMe SSD, No Wifi/Bluetooth card
* On board Ethernet: Intel I210 GBE
* On board audio: ALC 221, layout 11

What is working
* Graphic card is natively supported
* Audio is natively supported with layout 11
* Ethernet is natively supported
* DRM (Web media hardware acceleration)
* All USB ports work correctly through USB mapping (USBmap.kext)
* GeekBench score: signle core 717 multi-core 10880 Computation 4750

What is not working
* SAS controller with RAID array not recognized
* Wake up from sleeping causes a reboot since RTSMemFix has not been done
* Mac fan control could not read any fan speed data thus there is no way to control fan speed. 

USB Map for HP Z840
* Front USB3.0 Port 1-4 (Up to down)
*   Port 1: HS13 SSP4
*   Port 2: HS10 SSP4
*   Port 3: HS09 SSP4
*   Port 4: HS14 SSP4
*  Rear USB3.0 Port 1-4 (Left to right)
*   Port 1: HS03 SSP6
*   Port 2: HS04 SSP5
*   Port 3: HS06 SSP2
*   Port 4: HS05 SSP1
*  Rear USB2.0 Port 1-2
*   Port 1: HS11
*   Port 2: HS12

** No EHC1/EHC2/XHCI rename was comitted even it as suggested by the guide. Ports do not work properly after renaming. 
** Both USBmap Tool and Hackintool did not work properly on the target machine for unknown reason. My mapping was hand picked through IORegistryExplorer on a existing map file for X99.

Credit 
* Apple
* Opencore Team
