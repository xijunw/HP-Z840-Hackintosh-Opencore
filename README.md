# HP-Z840-Hackintosh-Opencore
Opencore configuration for Catalina

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
* Wake up from sleeping causes a reboot since RTSmemFix has not finished and I have no intention to finish it. The machine will be kept runing for computation.
* Mac fan control could not read any fan speed data thus there is no way to control fan speed. 

Credit 
* Apple
* Opencore Team
