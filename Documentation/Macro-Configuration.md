## ![#f03c15](https://github.com/moggieuk/Happy-Hare/wiki/resources/f03c15.png) ![#c5f015](https://github.com/moggieuk/Happy-Hare/wiki/resources/c5f015.png) ![#1589F0](https://github.com/moggieuk/Happy-Hare/wiki/resources/1589F0.png) Macro Configuration (mmu\_macro\_vars.cfg)

This is where you'll likely spend most of your time tuning the MMU after the initial setup is done.  It allows for configuration of all the supplied default macros in one place.

You will need to consult the [Configuring mmu\_macro\_var.cfg](Configuring-mmu_macro_vars.cfg) reference page for full details, but essentially the file is broken up into sections where each section contains the configuration for the respective macro. These include:

| Section | Macro Filename | Description |
| ------- | -------------- | ----------- |
| \_MMU\_SOFTWARE\_VARS | `base/mmu_software.cfg` | Controls the behavior of the print start and finalization |
| \_MMU\_STATE\_VARS | `base/mmu_state.cfg` | Customization of behavior when state changes |
| \_MMU\_LED\_VARS | `base/mmu_leds.cfg` | Configuration of LED actions |
| \_MMU\_SEQUENCE\_VARS | `base/mmu_sequence.cfg` | Control the movement of the toolhead during a tool change |
| \_MMU\_CUT\_TIP\_VARS | `base/mmu_cut_tip.cfg` | Controls the tip cutting procedure |
| \_MMU\_FORM\_TIP\_VARS | `base/mmu_form_tip.cfg` | Control Happy Hare's implementation of tip forming |
| \_MMU\_CLIENT\_VARS | `optional/client_macros.cfg` | Customization of Happy Hare's pause, resume and cancel\_print macros |

<br>

### More essential config setup:
- [Basic Operation](https://github.com/Enraged-Rabbit-Community/ERCFv2.5/blob/main/Documentation/Basic-Operation.md)
- [Hardware Configuration](https://github.com/Enraged-Rabbit-Community/ERCFv2.5/blob/main/Documentation/Hardware-Configuration.md)
- [MMU Calibration](https://github.com/Enraged-Rabbit-Community/ERCFv2.5/blob/main/Documentation/MMU-Calibration.md)
- [Setup Calibration](https://github.com/Enraged-Rabbit-Community/ERCFv2.5/blob/main/Documentation/Setup_Calibration.md)
- [Slicer Setup](https://github.com/Enraged-Rabbit-Community/ERCFv2.5/blob/main/Documentation/Slicer-Setup.md)
- [Endstops, Movement and Homing](https://github.com/Enraged-Rabbit-Community/ERCFv2.5/blob/main/Documentation/Movement-and-Homing.md)
- [Happy Hare Parameters](https://github.com/Enraged-Rabbit-Community/ERCFv2.5/blob/main/Documentation/Happy-Hare-Parameters.md)
- Macro Configuration
