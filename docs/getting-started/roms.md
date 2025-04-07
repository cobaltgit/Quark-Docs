# Adding ROMs

ROMs are stored in the `Roms` folder at the root of your SD card, with subfolders for each system: launching a game will launch with the corresponding options for that system (emulator core and CPU speed), or per-game overrides if any have been set.

!!! note
    This site does not host any copyrighted content. **Google is your friend.**

## Multi-disc games

Quark supports M3U playlists for CD-based systems. This can be done manually or by navigating to a CD-based system, pressing X and selecting *Generate M3Us* in the script submenu. 

The script supports generating M3Us named with the Redump (i.e. `Metal Gear Solid (USA) (Disc 1)`) or TOSEC (i.e. `Night Trap (1992)(Sega)(US)(Disc 1 of 2)`) naming schemes.

This will move a game's discs into a hidden folder and generate an M3U playlist for them, producing the following folder structure - an example for Metal Gear Solid for the PS1...

```
# CHD files are also supported by the M3U generator
# Folder structure in SDCARD:/Roms/PS

.Metal Gear Solid (USA)/
    Metal Gear Solid (USA) (Disc 1).bin
    Metal Gear Solid (USA) (Disc 1).cue
    Metal Gear Solid (USA) (Disc 2).bin
    Metal Gear Solid (USA) (Disc 2).cue
Metal Gear Solid (USA).m3u
```

...the contents of the M3U file (`Metal Gear Solid (USA).m3u`) being as follows:

```
.Metal Gear Solid (USA)/Metal Gear Solid (USA) (Disc 1).cue
.Metal Gear Solid (USA)/Metal Gear Solid (USA) (Disc 2).cue
```

Any orphaned single-track `.bin` files will have a corresponding cuesheet generated.

Alternatively, multi-disc PS1 games can be **lossily** compressed into a single `.pbp` file.

### Switching discs

To switch discs when playing a multi-disc CD game:

1. Press HOME and navigate to the *Native Menu*
2. From the RetroArch quick menu, go to *Disc Control*
3. Eject the current disc by selecting *Eject Disc*
4. You should now see a *Current Disc Index* option, which will take you to a submenu where you can select which disc you want to swap to
5. Select the disc you want to swap to and select *Insert Disc*

