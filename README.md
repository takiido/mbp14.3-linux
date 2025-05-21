## Files for Macbook Pro 15" 2017 Touchbar (14,3)

- ✅ [Wifi](#wifi)
- ✅ [Bluetooth](#bluetooth)
- ✅ [USB](#usb)
- ✅ [External display (HDMI)](#external-display)
- ✅ [Built-in display]#(built-in-display)
- ✅ [Keyboard](#keyboard)
- ✅ [Sound](#sound)

### Bluetooth

Works out of the box

### USB

Works out of the box

### External Display

Works out of the box

### Built-in Display

Works out of the box

### Keyboard

Still figuring out how to make backlight work.

### Wifi

Copy config file to /usr/lib/firmware/brcm/

```bash
$ uname -a
Linux inferno 6.14.6-arch1-1 #1 SMP PREEMPT_DYNAMIC Fri, 09 May 2025 17:36:18 +0000 x86_64 GNU/Linux

$ lspci -nn -d 14e4:
03:00.0 Network controller [0280]: Broadcom Inc. and subsidiaries BCM43602 802.11ac Wireless LAN SoC [14e4:43ba] (rev 02)
```
### Sound

~~Still figuring out how to make sub work.~~
✅ After some tricks with ALSA and JamesDSP sound is much better than in Bootcamp but probably not as good as on MacOS.

I'm not sure which one of these really helped but that's the list:

1. #### Commands:

```bash
sudo pacman -S sof-firmware
```

```bash
sudo pacman -S pipewire pipewire-alsa pipewire-pulse pipewire-jack wireplumber
```

```bash
systemctl --user enable --now pipewire pipewire-pulse wireplumber
```

```bash
sudo pacman -S alsa-card-profiles
```

```bash
systemctl --user restart pipewire
```

```bash
pw-metadata -n settings 0 clock.force-quantum 2048
```

```bash
sudo pacman -S alsa-ucm-conf
```

```bash
   pacman -S wget make gcc linux-headers-generic
   ```
```bash
clone [snd_hda_macbookpro](https://github.com/davidjo/snd_hda_macbookpro)
```

```bash
./install.cirrus.driver.sh
```

2. #### JamesDSP:
- Dynamic bass boost: 15db
- Equalizer: Acoustic

3. #### reboot
