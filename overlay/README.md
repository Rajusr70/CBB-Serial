CBB-Serial Device Tree Overlay
==============================

`CBB-Serial-00A0.dts` is the uncompiled device tree overlay for the
CBB-Serial cape (currently working but not quite complete). 

To install the overlay, first compile it:

```
 # dtc -O dtb -o CBB-Serial-00A0.dtbo -b 0 -@ CBB-Serial-00A0.dts
```

Then add it to the overlay directory:

```
 # mv CBB-Serial-00A0.dtbo /lib/firmware
```

It will then be loaded automatically by the cape manager the next time
the BeagleBone boots with the CBB_Serial EEPROM attached. It can also
be loaded manually:

```
 # echo CBB-Serial > /sys/devices/bone_capemgr.*/slots
```

