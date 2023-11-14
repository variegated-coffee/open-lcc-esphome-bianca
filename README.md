# Open LCC ESP32-S3 firmware for Lelit Bianca based on ESPHome

This is meant as a companion firmware to the [open-lcc/rp2040-bianca](https://github.com/open-lcc/rp2040-bianca) firmware. The Open LCC hardware has two microcontrollers, the RP2040, which controls commmunication with the Gicar Control Board, and the ESP32-S3, which communicates with the world. This firmware is based on ESPHome, because it was an easy way to get started with it. In the future, a more custom firmware might be more performant an easier to use in some cases, but as of writing, this is the firmware that exists.

This project is basically a large ESPHome yaml configuration. You are meant to modify this. 

## Compatibility

This firmware is compatible with Open LCC Board R1A through R2B. Furthermore, it's *known* to be compatible with the Bianca V2, but it's strongly suspected that it is compatible with Bianca V1, and Bianca V3 (with exception for the
 new Power LED). If you have a Bianca V3 and is interested in installing this project, let me (@magnusnordlander) know and we can work together on getting it fully compatible.

## Disclaimer

Considering this plugs in to an expensive machine it bears to mention: Anything you do with this, you do at your own risk. Components have been fried already during the course of this project. Your machine uses both line voltage power, high pressured hot water, steam and other dangerous components. There is a risk of both damaging the machine, personal injury and property damage, the liability for which you assume yourself. This is not the stage to get on board with this project if you aren't willing to deal with those risks.

## Status

Consider this project beta quality.

### Versioning
This project uses Semver. The major version number is increased whe RP2040 <-> ESP32 protocol version is increased (as that is a BC break).

## Project goals

Create a firmware for using the Open LCC in a Lelit Bianca to its fullest extent.

### Extension boards
The Open LCC hardware has QWIIC interfaces to allow for extension. Specifically, the ESP32-S3 has one QWIIC interface. The ESPHome ecosystem supports a number of different components that can be connected via I2C.

## Building

The project is built using the regular ESPHome build chain. It includes options to upload firmware both over USB and over Wi-fi.

## Licensing

The firmware in itself is MIT licensed. If you include components licensed under the GPL (such as the serial bridge component), the firmware becomes GPL licensed. If you're just using the firmware yourself, this doesn't really matter. If you're distributing the firmware 
