# awesome-dc32-badge
A respository of information and links to promote support and continued development of the DEFCON 32 badge. This repository is not associated with Entropic Engineering (creators of the badge hardware), Dmitry Grinberg (creator of the uGB firmware and rePALM), or DEFCON (designers of the badge artwork and case). 

--------------------

## Table of contents

- [FAQ]($faq)
- [Guides](#guides)
  - [General Guides](#general)
- [Official Releases](#official)
  - [Firmware](#firmware)
  - [Software](#software)
  - [Resources](#resources)
- [Community Developed](#community)
  - [Firmware](#commfirmware)
  - [Software](#commsoftware)
  - [Physical Modifications](#commmods)
- [External links](#external-links)
- [Communities / Forums](#communities--forums)

--------------------
## FAQ

- Q. My badge shows "No valid FAT partition found" when I try to load other GB/GBC ROMs?
  - A. The stock SD cards provided by DEFCOM are very poor quality and have a high failure rate. You can attempt to format the SD card by using the [official SD formatter found here](https://www.sdcard.org/downloads/formatter/), and manually add folders named 'ROM' and 'SAVE' to the root of the SD card. If the badge can still not detect it, you will need to purchase a third party SD card and format it with a FAT# filesystem (not exFAT).  

## Guides

### General

**[`^        back to top        ^`](#awesome-dc32-badge)**

Various resources from around the community to help with troubleshooting, development, etc.

- [DC32 Badge Hacking Google Doc](https://docs.google.com/document/d/1Jff1UbKaRGoHoAug1c0r6a4Y-MYruvgVORGG8c63sNQ) - The purpose of this document is to be a collective note gathering location for the DC32 Badge Challenge
- [Gameboy Interface to access Badge Features](https://docs.google.com/document/d/1COY5n0HhBcBq7ILwsKtOjV-_0-arNPkk_qBH9PI9fms) - GB hardware has a few unused IO regs in the IO reg range (0xFF00..0xFF7F). They are reused in this badge to expose extra functionality that GB-proper lacks. This document details how to use these features.

## Official

### Firmware

**[`^        back to top        ^`](#awesome-dc32-badge)**

Firmwares released by DmitryGR. No licenses assumed or granted unless granted directly by the author.

- [uGB 1.3.1g Compiled](https://discord.com/channels/867438418212683796/1262488625799495732/1271177820298674280) - Stock firmware originally installed on the badges, saves are not functional on this firmware. 
- [uGB 1.3.1g Source Code](https://cdn.discordapp.com/attachments/1262488625799495732/1271175312012480512/defcon_badge.tar.bz2?ex=66c0edc3&is=66bf9c43&hm=174d8e7c02c12762ec74cde20103b29705f163aeca7854a19823e1f5150bee18&) 
- [uGB 1.5 Compiled](http://dmitry.gr/images/defcon_update_1.5.0.tar.bz2) - Official patch that fixes game saves and downclocks the SD card.
- [uGB 1.5 Source Code](http://dmitry.gr/images/defcon_code_1.5.0.tar.bz2)
- [uGB 1.6 Compiled](https://discord.com/channels/867438418212683796/1262488625799495732/1271971778985590805) - Added menu item to send rickroll infra red signal. Added explicit menu item to show entropic support screen.
- [rePalm NO RAM MOD](https://dmitry.gr/images/rePalmDefcon_NOPSRAM.bin) - Stock badge can only use a minimal build as RP2350’s 512KB of RAM is rather tight for PalmOS 5.2 with a  320x240 display. To save RAM, the display is limited to 8bpp
- [rePalm PSRAM MOD](https://dmitry.gr/images/rePalmDefcon_withPSRAM.bin) - Badges with a 8MByte APMemory PSRAM installed (there is a footprint on the board, go wild) gets a fuller build with support for games, video playback, and 16bpp screen.

### Software

- [DC32 Badge Game Source](https://github.com/CosmicBonBon/DC32BadgeGame) - Written by CosmicBonBon, source files provided and encouraged for modding and expansion of the game.

### Resources

- [DEF CON Media Server Badge Resources](https://media.defcon.org/DEF%20CON%2032/DEF%20CON%2032%20badge/) - Official DEFCOM file server with their provided copies of code and documentation.
- [Raspberry Pi PicoSDK Board Definitions](https://github.com/raspberrypi/pico-sdk/blob/master/src/boards/include/boards/defcon32_badge.h) 

## Community

**[`^        back to top        ^`](#awesome-dc32-badge)**

### <a id="commfirmware" /> Firmware

- [DEFCON 32 Firmware from jaku](https://github.com/jaku/DEFCON-32-BadgeFirmware) - Provides custom firmware for DEFCON badges, including MoonMaster, NoRom, AllItems, and Original, with detailed flashing instructions for UF2 and BIN formats.
- [DEFCON32 Badge Doom](https://github.com/kilograham/rp2040-doom/releases/tag/defcon32_v1) - Provides instructions to install Doom on the DEFCON 32 Badge, including steps to back up and restore original firmware, and details on gameplay and button configurations.
- [DEFCON 32 Badge - MicroPython PoC](https://github.com/Phaeilo/dc32_badge_micropython) - Some example code to drive the hardware of the Defcon 32 badge with MicroPython.
- [DEFCON 32 Badge Color Shifting Demo](https://github.com/skintigh/defcon32_badge_demo) - Author ported a demo they wrote in the 1990s in Turbo Pascal to run on this year's badge.

### <a id="commsoftware" /> Software

- [CalvinLL Flashy Rom](https://github.com/Calvin-LL/defcon-32-badge-flashy-rom) - This is a simple ROM for the DEF CON 32 Badge that makes the LEDs flash in random colors.
- [BSoDEFCON ROM](https://github.com/rootabeta/BSoDEFCON) - A little joke Blue Screen of Death simulator (BSOD) for the DEF CON 32 badge, with various versions of the screen and different operating systems - plus various fancy LED flashing modes.

### <a id="commmods" /> Physical Modifications

- 3D models
  - [DEFCON 32 Badge Buttons](https://www.printables.com/model/977477-defcon-32-badge-buttons)
  - [Defcon 32 badge D-pad and AB-buttons](https://makerworld.com/en/models/588650?from=search#profileId-509911)

## External Links

**[`^        back to top        ^`](#awesome-dc32-badge)**

- [GBVideoPlayer2](https://github.com/LIJI32/GBVideoPlayer2) - Enhances GBVideoPlayer with higher resolution, 3-bit stereo PCM audio, video compression, and easier encoding, requiring specific hardware or accurate emulators for playback.
- [DEF ROM Firmware Generator](https://defrom.lol/) - Upload Game Boy or Game Boy Color ROMs to create custom firmware in UF2 or BIN format.

## Communities / Forums

**[`^        back to top        ^`](#awesome-dc32-badge)**

- [DC32 Badge Hacking Discord](https://discord.gg/z7HvmSQx) - Most comprehensive resource on badge troubleshooting, custom development, and discussion. Make sure you check the pinned posts and use the search feature!
