#### Page Sections:
-Configuration Options for ERCFv2.5:
  - [Necessary Updates](#---necessary-configuration-updates-for-v25)
  - [Filament Cutter Options](#---filament-cutter-options)
  - [Filament Sensor Options](#---filament-sensor-options1)
  - [Pregate Sensor Options](#---pregate-sensor-options)

## ![#f03c15](https://github.com/moggieuk/Happy-Hare/wiki/resources/f03c15.png) ![#c5f015](https://github.com/moggieuk/Happy-Hare/wiki/resources/c5f015.png) ![#1589F0](https://github.com/moggieuk/Happy-Hare/wiki/resources/1589F0.png) Necessary Configuration Updates for v2.5

1.  Open the file `config / mmu / base / mmu.cfg`. At the top of the file, add your Local MCU's CANBus UUID. If you are using USB to connect, Happy Hare should have detected and filled your serial number in for you. If not, add it in at this point. Save and close the file.

2. Open the file `config / mmu / base / mmu_hardware.cfg`. If you are using a beefy NEMA17 motor for Direct Drive, you need to increase your motor currents starting on line 128. You want the current to be set to 70% of the motor's rated current, up to the stepper driver's max rated current. That's usually 1.6amps for BOM motors and EZ Drivers.

3. Still in the file `config / mmu / base / mmu_hardware.cfg`. If you are using Direct Drive, comment out or remove the Gear Ratio on line 143. If you are using legacy Geared Drive, you need the Gear Ratio to be set to match your physical gear ratio, usually 80:20 or 60:20. These numbers represent the number of teeth on the 80- or 60-tooth gears, and the 20-tooth pulley. Save and close the file.

## ![#f03c15](https://github.com/moggieuk/Happy-Hare/wiki/resources/f03c15.png) ![#c5f015](https://github.com/moggieuk/Happy-Hare/wiki/resources/c5f015.png) ![#1589F0](https://github.com/moggieuk/Happy-Hare/wiki/resources/1589F0.png) Filament Cutter Options

If you are using a Filament Cutter, you must update `config / mmu / base / mmu_parameters.cfg` line 334. Change the `form_tip_macro` value to `_MMU_CUT_TIP`.

Next, you will need to go through the entire file `config / mmu / base / mmu_macro_vars.cfg`. Read it, understand it, and change all of the options to suit your unique build and needs. The values you use depend on which extruder / toolhead you are using. There are also instructions for semi-automatic calibration for almost all of the cutter and toolhead length values in the Happy Hare Wiki's [Blobbing and Stringing page](https://github.com/moggieuk/Happy-Hare/wiki/Blobbing-and-Stringing)!

## ![#f03c15](https://github.com/moggieuk/Happy-Hare/wiki/resources/f03c15.png) ![#c5f015](https://github.com/moggieuk/Happy-Hare/wiki/resources/c5f015.png) ![#1589F0](https://github.com/moggieuk/Happy-Hare/wiki/resources/1589F0.png) Filament Sensor Options

If you are using a toolhead with either an Extruder sensor (before the Extruder gears), a Toolhead sensor (after the Extruder gears), or both, you need to set those up.

1. Open the file `config / mmu / base / mmu_hardware.cfg`. Add the pin number(s) that your sensor(s) are connected to on lines 278-279. Save and close the file.

2. If you are using an Extruder Sensor specifically: Open the file `config / mmu / base / mmu_parameters.cfg`. Update the `extruder_homing_endstop` to use the value`extruder`. Save and close the file.

There are instructions for nearly-automatic calibration for almost all of the cutter and toolhead length values in the Happy Hare Wiki's [Blobbing and Stringing page](https://github.com/moggieuk/Happy-Hare/wiki/Blobbing-and-Stringing). Automatic calibration will make your life easier, you should do it.

## ![#f03c15](https://github.com/moggieuk/Happy-Hare/wiki/resources/f03c15.png) ![#c5f015](https://github.com/moggieuk/Happy-Hare/wiki/resources/c5f015.png) ![#1589F0](https://github.com/moggieuk/Happy-Hare/wiki/resources/1589F0.png) Pregate Sensor Options

Coming soon! I don't use these yet, so I need help writing this section!



### ERCF Setup Steps:
- [Flashing Your Local MCU](https://github.com/Enraged-Rabbit-Community/ERCFv2.5/blob/main/Documentation/Flashing-Local-MCU.md)
- [Installing Happy Hare](https://github.com/Enraged-Rabbit-Community/ERCFv2.5/blob/main/Documentation/Installing-Happy-Hare.md)
- Happy Hare Configuration
- [Calibrating Your Hardware](https://github.com/Enraged-Rabbit-Community/ERCFv2.5/blob/main/Documentation/Calibrating-Your-Hardware.md)
- [Installing KlipperScreen Happy Hare](https://github.com/Enraged-Rabbit-Community/ERCFv2.5/blob/main/Documentation/Installing-KlipperScreen.md)
- [Slicer Configuration](https://github.com/Enraged-Rabbit-Community/ERCFv2.5/blob/main/Documentation/Slicer-Setup.md)
- [Further Mods to Consider](https://github.com/Enraged-Rabbit-Community/ERCFv2.5/blob/main/Documentation/Further-Mods.md)

### Useful References:
- [Hardware Configuration](https://github.com/Enraged-Rabbit-Community/ERCFv2.5/blob/main/Documentation/Hardware-Configuration.md)
- [MMU Calibration](https://github.com/Enraged-Rabbit-Community/ERCFv2.5/blob/main/Documentation/MMU-Calibration.md)
- [Basic Operation](https://github.com/Enraged-Rabbit-Community/ERCFv2.5/blob/main/Documentation/Basic-Operation.md)
- [Setup Calibration](https://github.com/Enraged-Rabbit-Community/ERCFv2.5/blob/main/Documentation/Setup_Calibration.md)
- [Slicer Setup](https://github.com/Enraged-Rabbit-Community/ERCFv2.5/blob/main/Documentation/Slicer-Setup.md)
- [Endstops, Movement and Homing](https://github.com/Enraged-Rabbit-Community/ERCFv2.5/blob/main/Documentation/Movement-and-Homing.md)
- [Happy Hare Parameters](https://github.com/Enraged-Rabbit-Community/ERCFv2.5/blob/main/Documentation/Happy-Hare-Parameters.md)
- [Macro Configuration](https://github.com/Enraged-Rabbit-Community/ERCFv2.5/blob/main/Documentation/Macro-Configuration.md)
