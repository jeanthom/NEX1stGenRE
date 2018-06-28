# Comparing  between latest NEX-3 and latest NEX-5 firmwares

Download links :
    * [NEX-3 Firmware upgrade (Windows)](https://www.sony.co.uk/electronics/support/downloads/Z0005462)
    * [NEX-5 Firmware upgrade (Windows)](https://www.sony.co.uk/electronics/support/downloads/Z0005464)

## Diff output

Firmware extracted with fwtool.py,`diff -rq  NEX-3V5_Update1112a/ NEX-5V5_Update1112a/` :

```
Files NEX-3V5_Update1112a/config.yaml and NEX-5V5_Update1112a/config.yaml differ
Files NEX-3V5_Update1112a/firmware.dat and NEX-5V5_Update1112a/firmware.dat differ
Files NEX-3V5_Update1112a/firmware.fdat and NEX-5V5_Update1112a/firmware.fdat differ
Files NEX-3V5_Update1112a/firmware.tar and NEX-5V5_Update1112a/firmware.tar differ
Files NEX-3V5_Update1112a/firmware.tar_unpacked/0100_config/mount.conf and NEX-5V5_Update1112a/firmware.tar_unpacked/0100_config/mount.conf differ
Files NEX-3V5_Update1112a/firmware.tar_unpacked/0101_config_sum/config.sum and NEX-5V5_Update1112a/firmware.tar_unpacked/0101_config_sum/config.sum differ
Files NEX-3V5_Update1112a/firmware.tar_unpacked/0300_partconf/partinf.conf and NEX-5V5_Update1112a/firmware.tar_unpacked/0300_partconf/partinf.conf differ
Files NEX-3V5_Update1112a/firmware.tar_unpacked/0301_partconf_sum/partconf.sum and NEX-5V5_Update1112a/firmware.tar_unpacked/0301_partconf_sum/partconf.sum differ
Files NEX-3V5_Update1112a/firmware.tar_unpacked/0800_appli/avsys/av.bin and NEX-5V5_Update1112a/firmware.tar_unpacked/0800_appli/avsys/av.bin differ
Files NEX-3V5_Update1112a/firmware.tar_unpacked/0800_appli/boot/cas/CA_FRAM.BIN and NEX-5V5_Update1112a/firmware.tar_unpacked/0800_appli/boot/cas/CA_FRAM.BIN differ
Files NEX-3V5_Update1112a/firmware.tar_unpacked/0800_appli/boot/cas/CA_FROM.BIN and NEX-5V5_Update1112a/firmware.tar_unpacked/0800_appli/boot/cas/CA_FROM.BIN differ
Files NEX-3V5_Update1112a/firmware.tar_unpacked/0800_appli/boot/factory/Asys.bin and NEX-5V5_Update1112a/firmware.tar_unpacked/0800_appli/boot/factory/Asys.bin differ
Files NEX-3V5_Update1112a/firmware.tar_unpacked/0800_appli/boot/factory/Hsys.bin and NEX-5V5_Update1112a/firmware.tar_unpacked/0800_appli/boot/factory/Hsys.bin differ
Files NEX-3V5_Update1112a/firmware.tar_unpacked/0800_appli/boot/factory/initreg.bin and NEX-5V5_Update1112a/firmware.tar_unpacked/0800_appli/boot/factory/initreg.bin differ
Files NEX-3V5_Update1112a/firmware.tar_unpacked/0800_appli/usr/bin/app/deviceInfo.xml and NEX-5V5_Update1112a/firmware.tar_unpacked/0800_appli/usr/bin/app/deviceInfo.xml differ
Files NEX-3V5_Update1112a/firmware.tar_unpacked/0800_appli/usr/bin/app/main and NEX-5V5_Update1112a/firmware.tar_unpacked/0800_appli/usr/bin/app/main differ
Files NEX-3V5_Update1112a/firmware.tar_unpacked/0800_appli/usr2/boot/initrd.img and NEX-5V5_Update1112a/firmware.tar_unpacked/0800_appli/usr2/boot/initrd.img differ
Files NEX-3V5_Update1112a/firmware.tar_unpacked/0800_appli/usr2/boot/initrd.img_unpacked/bin/osal.ko and NEX-5V5_Update1112a/firmware.tar_unpacked/0800_appli/usr2/boot/initrd.img_unpacked/bin/osal.ko differ
Files NEX-3V5_Update1112a/firmware.tar_unpacked/0800_appli/usr2/boot/rootfs.img and NEX-5V5_Update1112a/firmware.tar_unpacked/0800_appli/usr2/boot/rootfs.img differ
Files NEX-3V5_Update1112a/firmware.tar_unpacked/0800_appli/usr2/boot/rootfs.img_unpacked/lib/modules/2.6.22.19-alp_nl/extra/osal.ko and NEX-5V5_Update1112a/firmware.tar_unpacked/0800_appli/usr2/boot/rootfs.img_unpacked/lib/modules/2.6.22.19-alp_nl/extra/osal.ko differ
Files NEX-3V5_Update1112a/firmware.tar_unpacked/0800_appli/usr2/boot/rootfs.img_unpacked/version.txt and NEX-5V5_Update1112a/firmware.tar_unpacked/0800_appli/usr2/boot/rootfs.img_unpacked/version.txt differ
Files NEX-3V5_Update1112a/firmware.tar_unpacked/0800_appli/usr2/boot/vmlinux.bin and NEX-5V5_Update1112a/firmware.tar_unpacked/0800_appli/usr2/boot/vmlinux.bin differ
Only in NEX-5V5_Update1112a/firmware.tar_unpacked/0800_appli/usr2: ex_conf_205.h
Only in NEX-3V5_Update1112a/firmware.tar_unpacked/0800_appli/usr2: ex_conf_206.h
Files NEX-3V5_Update1112a/firmware.tar_unpacked/0801_appli_sum/appli.sum and NEX-5V5_Update1112a/firmware.tar_unpacked/0801_appli_sum/appli.sum differ
```

### /0800_appli/usr/bin/app/deviceInfo.xml

```diff
*** NEX-3V5_Update1112a/firmware.tar_unpacked/0800_appli/usr/bin/app/deviceInfo.xml	Thu Dec  8 01:01:37 2011
--- NEX-5V5_Update1112a/firmware.tar_unpacked/0800_appli/usr/bin/app/deviceInfo.xml	Thu Dec  8 01:01:04 2011
***************
*** 10,18 ****
  		<key>Category</key>
  		<integer>5</integer>
  		<key>Feature</key>
! 		<integer>4736</integer>
  		<key>Format</key>
! 		<integer>8</integer>
  		<key>db</key>
  		<dict>
  			<key>name</key>
--- 10,18 ----
  		<key>Category</key>
  		<integer>5</integer>
  		<key>Feature</key>
! 		<integer>7808</integer>
  		<key>Format</key>
! 		<integer>66</integer>
  		<key>db</key>
  		<dict>
  			<key>name</key>
```

### `/0800_appli/avsys/av.bin`

### `/0800_appli/boot/factory/initreg.bin`

### `/0800_appli/boot/cas/CA_FRAM.BIN`

### `/0800_appli/boot/cas/CA_FROM.BIN`

### Files where the differences are compile date strings

The differences are negligible enough to consider the files as functionally identical.

    * `/0800_appli/usr2/boot/initrd.img_unpacked/bin/osal.ko`
    * `/0800_appli/usr/bin/app/main`
