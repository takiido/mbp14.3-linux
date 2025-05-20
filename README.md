## Files for Macbook Pro 15" 2017 Touchbar (14,3)

- ✅ Wifi
- ✅ Bluetooth
- ✅ USB
- ✅ External display (HDMI)
- ✅ Built-in display
- ✅ Keyboard
- ✅ Sound

### Wifi

Copy config file to /usr/lib/firmware/brcm/

```bash
$ uname -a
Linux inferno 6.14.6-arch1-1 #1 SMP PREEMPT_DYNAMIC Fri, 09 May 2025 17:36:18 +0000 x86_64 GNU/Linux

$ lspci -nn -d 14e4:
03:00.0 Network controller [0280]: Broadcom Inc. and subsidiaries BCM43602 802.11ac Wireless LAN SoC [14e4:43ba] (rev 02)
```
### Sound

Still figuring out how to make sub work

1. pacman -S wget make gcc linux-headers-generic
2. clone [snd_hda_macbookpro](https://github.com/davidjo/snd_hda_macbookpro)
3. ./install.cirrus.driver.sh
4. reboot
