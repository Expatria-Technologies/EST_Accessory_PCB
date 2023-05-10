# GRBLHAL2000 for PrintNC EST

![Logo](/readme_images/logo_sm.jpg)

Expatria Technologies EST Breakout Boards

Expatria's controller boards (GRBLHAL2000 and FlexiHAL) incorporates community driven elements from the PrintNC Electronic Standardization (EST) Project. As part of this project, two additional breakout boards have been created for the user controls and limits/probe inputs. These are simple boards and could easily be milled and hand assembled, but fabrication files for each are available in the CAM_Outputs folder. The inputs are accessible via the RJ45 connectors on the Flexi-HAL mainboard. In addition, the Flexi-HAL is intended to be used with the Expatria Real-Time jog controller or similar peripheral:


### Limit and Sensor Breakout

<img src="/readme_images/limit_mod_render.jpg" width="150">

By default both GRBL and the GRBLHAL2000 expect NPN NC limit switches.  PNP switches are not supported. NO switches can also be used on any switch input

The first four axes have single limit inputs that are accessed via the RJ45 limit breakout connector.  A sample design for a breakout panel is included in the CAM_Outputs folder.  The fifth (M4 or B axis) limit input is multiplexed via XOR logic between two 3 wire connections to allow for future flexibility.  GRBL always knows the direction of travel so individual min and max pins are not required.  Auto-squaring is supported by enabling ganged axes in GRBLHAL and setting the appropriate pins.

In addition to the B limit, there are two probe input pins on the limit RJ45 breakout connector that are also multiplexed via XOR logic.

For both of the dual-input signals there is no need to terminate unused ports.

The RJ45 pinout:

<img src="/readme_images/limit_rj45_pinout.jpg" width="150">

### User Button Breakout
<img src="/readme_images/User_mod_render.jpg" width="400">

Standard GRBL functions are mapped to 4 inputs.  These signals are primarily intended to be used via the user RJ45 connector.  For convenience, the HALT and DOOR signals are also exposed via 3 wire connections on the main PCB.  When multiplexed these signals must be NO logic.  A sample design for a button panel utilizing clear PETG buttons is included in the CAM_Outputs folder.

The RJ45 pinout:

<img src="/readme_images/user_rj45_pinout.jpg" width="150">

### Encoder Breakout
<img src="/readme_images/User_mod_render.jpg" width="400">

Standard GRBL functions are mapped to 4 inputs.  These signals are primarily intended to be used via the user RJ45 connector.  For convenience, the HALT and DOOR signals are also exposed via 3 wire connections on the main PCB.  When multiplexed these signals must be NO logic.  A sample design for a button panel utilizing clear PETG buttons is included in the CAM_Outputs folder.

The RJ45 pinout:

<img src="/readme_images/user_rj45_pinout.jpg" width="150">