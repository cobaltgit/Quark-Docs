# Firmware

Firmwares that Quark has been tested on:

* **v1.0.1** (`UI Version: 20240707`) (shipped with black Smart devices)
* **v1.0.0** (`UI Version: 20240511`) (latest firmware available on TrimUI GitHub)

!!! warning
    Firmwares older than **v1.0.0rc4** (`UI Version: 20240501`) have been confirmed to not work with Quark v1.1.0 *Baryon* and up.

If your Smart has shipped with an older firmware version (i.e. **0.116alpha**), you'll need to update to **v1.0.0** before installing Quark:

1. Download the SD recovery image from the GitHub release link [here](https://github.com/trimui/firmware_smart/releases/tag/v1.0.0)
2. Use an SD card flasher such as the bundled Win32DiskImager (Windows only) or [balenaEtcher](https://etcher.balena.io/) (Windows/Mac/Linux) to flash the image to a spare microSD card
3. Insert the newly created microSD card and boot your Smart. Wait until the LED stops flashing blue.