# Installation

## Firmware

Firmwares that Quark has been tested on:

* **v1.0.1** (`UI Version: 20240707`) (shipped with black Smart devices)
* **v1.0.0** (`UI Version: 20240511`) (latest firmware available on TrimUI GitHub)

!!! warning
    Firmwares older than **v1.0.0rc4** (`UI Version: 20240501`) have been confirmed to not work with Quark v1.1.0 *Baryon* and up.

If your Smart has shipped with an older firmware version (i.e. **0.116alpha**), you'll need to update to **v1.0.0** before installing Quark:

1. Download the SD recovery image from the GitHub release link [here](https://github.com/trimui/firmware_smart/releases/tag/v1.0.0)
2. Use an SD card flasher such as the bundled Win32DiskImager (Windows only) or [balenaEtcher](https://etcher.balena.io/) (Windows/Mac/Linux) to flash the image to a spare microSD card
3. Insert the newly created microSD card and boot your Smart. Wait until the LED stops flashing blue.
4. Done! Power off your Smart and eject the microSD card.

## SD card formatting

To install Quark, you'll need a microSD card formatted to the FAT32 file system:

!!! tip
    If your microSD card is 32GB or below in capacity, it should already be formatted to FAT32 from the factory. This step can be skipped if this is the case.

=== "Windows"

    1. Install and launch [Rufus](https://rufus.ie)
    2. Insert your microSD card into your computer (via a built-in slot or USB reader)
    3. Select it within Rufus under *Device*
    4. Under *Boot Selection*, select `Non bootable`
    5. Under File system, select `FAT32 (Default)` or `Large FAT32 (Default)` depending on the size of your microSD card 
    6. Click `START` and confirm that you wish to wipe and format your device

=== "macOS"

    1. Insert your SD card into your computer (via a built-in slot or USB reader)
    2. Launch Disk Utility (*Applications > Utilities > Disk Utility*)
    3. Select the drive you want to format and click *Erase*
    4. For the format, choose `MS-DOS (FAT)` and choose `Master Boot Record` for the scheme and click *Erase*
 
    Alternatively, the command line can be used for formatting:

    ```sh
    # use `diskutil list` to find which disk corresponds to your microSD card
    ~ % sudo diskutil eraseDisk FAT32 MBRFormat /dev/diskN
    ```

=== "Linux"

    1. Insert your SD card into your computer (via a built-in slot or USB reader)
    2. Open a terminal and run the following commands as root (or via sudo)

    ```sh
    $ sudo umount /dev/sdX1 # Use `lsblk` to find which device corresponds to your microSD card.
    $ sudo mkfs.vfat -F 32 /dev/sdX1 # This assumes the microSD card has a single partition
    ```

## Installation

The hard part is now over. With the latest release of Quark downloaded, open it in your favourite archive browser (i.e. 7-Zip) and extract it over the root of your newly formatted microSD card.

Insert your card into your Smart and boot. The first boot procedure may take some time depending on if you've already pre-populated your card with ROMs (see [here](roms.md) for details on how to add ROMs)

Congratulations! You have now installed Quark on your TrimUI Smart!