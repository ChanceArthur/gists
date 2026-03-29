SteamOS on my Asus motherboard is not able to sleep with the Logi Bolt receiver plugged in, even with S4/S5 USB power disabled in BIOS. This udev rule fixes that. This should apply to other motherboards and Linux distros as well.

Run the following commands:
```bash
$ echo 'ACTION=="add|change", SUBSYSTEM=="usb", DRIVERS=="usb", ATTRS{idVendor}=="046d", ATTRS{idProduct}=="c548", ATTR{power/wakeup}="disabled"' | sudo tee /etc/udev/rules.d/99-logi-bolt-sleep.rules
$ sudo udevadm trigger
```