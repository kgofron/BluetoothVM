# BluetoothVM

* The Bluetooth Thingy:52 settings.

* Find Bluetooth Version on Windows 10

https://www.thewindowsclub.com/how-to-check-bluetooth-version-in-windows-10

* Enable BLE in Ubuntu 18.04 guest on Windows 10 host:

https://scribles.net/enabling-bluetooth-in-virtualbox/

**Thingy.IOC**

https://github.com/epicsNSLS2-sensors/ThingyIOC

**The Bluetooth 5 Nordic stick.**

Flush the generic firmware (Use Programmer app, then install zephyr.hex firmware).
 
=====================================
**USB Device is busy => see #7:**

https://forums.virtualbox.org/viewtopic.php?f=35&t=82639#p390404

https://forums.virtualbox.org/viewtopic.php?f=3&t=92490&p=445326&hilit=bluetooth#p445326

**USB Intel Bluetooth adapter:**
  
```
c:\Program Files\Oracle\VirtualBox>VBoxManage.exe list usbhost
Host USB Devices:

UUID:               0c8ddac2-244c-47a4-898e-f2aae3b995de
VendorId:           0x8087 (8087)
ProductId:          0x0025 (0025)
Revision:           0.2 (0002)
Port:               7
USB version/speed:  2/Full
Manufacturer:       Intel Corp.
Address:            {e0cbf06c-cd8b-4647-bb8a-263b43f0f974}\0000
Current State:      Captured

UUID:               c00bc440-0cf7-4051-ae46-ea2779307803
VendorId:           0x2fe3 (2FE3)
ProductId:          0x0100 (0100)
Revision:           0.17 (0017)
Port:               1
USB version/speed:  2/Full
Manufacturer:       ZEPHYR
Product:            USB-DEV
SerialNumber:       0.01
Address:            {36fc9e60-c465-11cf-8056-444553540000}\0041
Current State:      Captured

UUID:               5e529181-1119-4347-920b-479301a33131
VendorId:           0x2fe3 (2FE3)
ProductId:          0x0100 (0100)
Revision:           0.17 (0017)
Port:               1
USB version/speed:  2/Full
Address:            {e0cbf06c-cd8b-4647-bb8a-263b43f0f974}\0004
Current State:      Captured

UUID:               fd42a9a5-6a4d-4a41-8d9f-c256f5d1880f
VendorId:           0x04b3 (04B3)
ProductId:          0x310c (310C)
Revision:           2.0 (0200)
Port:               1
USB version/speed:  2/Low
Manufacturer:       IBM Corp.
Product:            USB Optical Mouse
Address:            {745a17a0-74d3-11d0-b6fe-00a0c90f57da}\0037
Current State:      Busy

UUID:               7fd3d71c-67df-4050-9185-8d2a580b071d
VendorId:           0x0408 (0408)
ProductId:          0x5251 (5251)
Revision:           0.3 (0003)
Port:               5
USB version/speed:  2/High
Manufacturer:       Quanta Computer, Inc.
Address:            {36fc9e60-c465-11cf-8056-444553540000}\0006
Current State:      Busy
```
==========================================================
```
c:\Program Files\Oracle\VirtualBox>vboxmanage showvminfo
Usage:

VBoxManage showvminfo       <uuid|vmname> [--details]
                            [--machinereadable]
VBoxManage showvminfo       <uuid|vmname> --log <idx>
```
=================================
```
c:\Program Files\Oracle\VirtualBox>vboxmanage showvminfo ubuntu18
Name:                        ubuntu18
Groups:                      /
Guest OS:                    Ubuntu (64-bit)
UUID:                        859183a2-3c16-4bc8-bab4-ed0f560ece5f
Config file:                 C:\Users\kgofron\VirtualBox VMs\ubuntu18\ubuntu18.vbox
Snapshot folder:             C:\Users\kgofron\VirtualBox VMs\ubuntu18\Snapshots
Log folder:                  C:\Users\kgofron\VirtualBox VMs\ubuntu18\Logs
Hardware UUID:               859183a2-3c16-4bc8-bab4-ed0f560ece5f
Memory size                  6525MB
Page Fusion:                 disabled
VRAM size:                   64MB
CPU exec cap:                100%
HPET:                        disabled
CPUProfile:                  host
Chipset:                     piix3
Firmware:                    BIOS
Number of CPUs:              4
PAE:                         enabled
Long Mode:                   enabled
Triple Fault Reset:          disabled
APIC:                        enabled
X2APIC:                      enabled
Nested VT-x/AMD-V:           disabled
CPUID Portability Level:     0
CPUID overrides:             None
Boot menu mode:              message and menu
Boot Device 1:               Floppy
Boot Device 2:               DVD
Boot Device 3:               HardDisk
Boot Device 4:               Not Assigned
ACPI:                        enabled
IOAPIC:                      enabled
BIOS APIC mode:              APIC
Time offset:                 0ms
RTC:                         UTC
Hardw. virt.ext:             enabled
Nested Paging:               enabled
Large Pages:                 enabled
VT-x VPID:                   enabled
VT-x unr. exec.:             enabled
Paravirt. Provider:          Default
Effective Paravirt. Prov.:   KVM
State:                       running (since 2019-04-21T02:35:47.549000000)
Monitor count:               1
3D Acceleration:             enabled
2D Video Acceleration:       disabled
Teleporter Enabled:          disabled
Teleporter Port:             0
Teleporter Address:
Teleporter Password:
Tracing Enabled:             disabled
Allow Tracing to Access VM:  disabled
Tracing Configuration:
Autostart Enabled:           disabled
Autostart Delay:             0
Default Frontend:
Storage Controller Name (0):            IDE
Storage Controller Type (0):            PIIX4
Storage Controller Instance Number (0): 0
Storage Controller Max Port Count (0):  2
Storage Controller Port Count (0):      2
Storage Controller Bootable (0):        on
Storage Controller Name (1):            SATA
Storage Controller Type (1):            IntelAhci
Storage Controller Instance Number (1): 0
Storage Controller Max Port Count (1):  30
Storage Controller Port Count (1):      1
Storage Controller Bootable (1):        on
IDE (1, 0): E: (UUID: 00445644-0000-0000-0000-00000000453a)
SATA (0, 0): C:\Users\kgofron\VirtualBox VMs\ubuntu18\ubuntu18.vdi (UUID: 2c305b7e-4044-4544-8617-352f19e5a356)
NIC 1:                       MAC: 08002762A248, Attachment: NAT, Cable connected: on, Trace: off (file: none), Type: 82540EM, Reported speed: 0 Mbps, Boot priority: 0, Promisc Policy: deny, Bandwidth group: none
NIC 1 Settings:  MTU: 0, Socket (send: 64, receive: 64), TCP Window (send:64, receive: 64)
NIC 2:                       disabled
NIC 3:                       disabled
NIC 4:                       disabled
NIC 5:                       disabled
NIC 6:                       disabled
NIC 7:                       disabled
NIC 8:                       disabled
Pointing Device:             USB Tablet
Keyboard Device:             PS/2 Keyboard
UART 1:                      disabled
UART 2:                      disabled
UART 3:                      disabled
UART 4:                      disabled
LPT 1:                       disabled
LPT 2:                       disabled
Audio:                       enabled (Driver: DSOUND, Controller: AC97, Codec: AD1980)
Audio playback:              disabled
Audio capture:               enabled
Clipboard Mode:              Bidirectional
Drag and drop Mode:          Bidirectional
Session name:                GUI/Qt
Video mode:                  1256x789x32 at 0,0 enabled
VRDE:                        disabled
OHCI USB:                    disabled
EHCI USB:                    disabled
xHCI USB:                    enabled

USB Device Filters:

Index:                       0
Active:                      no
Name:                        Unknown device 2FE3:0100 [0011]
VendorId:                    2fe3
ProductId:                   0100
Revision:                    0011
Manufacturer:
Product:
Remote:                      0
Serial Number:

Index:                       1
Active:                      yes
Name:                        Intel Corp.  [0002]
VendorId:                    8087
ProductId:                   0025
Revision:                    0002
Manufacturer:
Product:
Remote:                      0
Serial Number:

Available remote USB devices:

<none>

Currently Attached USB Devices:

<none>

Bandwidth groups:  <none>

Shared folders:

Name: 'VBoxShare', Host path: 'C:\VBoxShare' (machine mapping), writable, auto-mount

VRDE Connection:             not active
Clients so far:              0

Capturing:                   active
Capture audio:               not active
Capture screens:             0
Capture file:                C:\Users\kgofron\VirtualBox VMs\ubuntu18\ubuntu18.webm
Capture dimensions:          1024x768
Capture rate:                512kbps
Capture FPS:                 25kbps
Capture options:             ac_enabled=false,vc_enabled=true,ac_profile=med

Guest:

Configured memory balloon size: 0MB
OS type:                     Linux26_64
Additions run level:         2
Additions version            6.0.4 r128413

Guest Facilities:

Facility "VirtualBox Base Driver": active/running (last update: 2019/04/21 02:36:05 UTC)
Facility "VirtualBox System Service": active/running (last update: 2019/04/21 02:36:11 UTC)
Facility "Seamless Mode": active/running (last update: 2019/04/21 02:36:05 UTC)
Facility "Graphics Mode": active/running (last update: 2019/04/21 02:36:05 UTC)

```

