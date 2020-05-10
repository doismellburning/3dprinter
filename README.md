# Notes for my 3D printer setup

Geeetech i3 Pro B

## Firmware

http://www.geeetech.com/forum/viewtopic.php?t=17046

http://www.geeetech.com/forum/download/file.php?id=2819&sid=fc975f0e5d66e14affed7246893af3ac

NOTE instruction at top of page - threaded rod, so:

```
M92 Z400
M500
```

Building firmware: http://www.geeetech.com/forum/viewtopic.php?f=13&t=17181 (TL;DR use Arduino GUI)

### Dumping old firmware

```
$ avrdude -p atmega2560 -c stk500v2 -P /dev/ttyUSB0 -b 115200 -U flash:r:PRINTER_ORIGINAL.hex
```

## Slicer settings

Slic3r from Ubuntu Focal


## Misc old notes

* http://www.geeetech.com/forum/viewtopic.php?t=68464 - settings for Cura
* CLI slice: `CuraEngine slice -v -j  ../Cura/resources/definitions/Geeetech_i3.def.json -o GH_small_test_block.gcode -l GH_small_test_block.STL`

