![Logo](/readme_images/logo_sm.jpg)
# Expatria Technologies EST Breakout Boards
<img src="/readme_images/IMG_0117.jpg" width="800">

Expatria Technologies Flexi-HAL EST Accessory boards

Expatria's controller boards (GRBLHAL2000 and FlexiHAL) incorporates community driven elements from the PrintNC Electronic Standardization (EST) Project. As part of this project, two additional breakout boards have been created for the user controls and limits/probe inputs. These are simple boards and could easily be milled and hand assembled, but fabrication files for each are available in the CAM_Outputs folder. The inputs are accessible via the RJ45 connectors on the Flexi-HAL mainboard and on the GRBLHAL2000.

### Limit and Sensor Breakout

<img src="/readme_images/limit_mod_render.jpg" width="150">

By default both GRBL and the GRBLHAL2000 expect NPN NC limit switches.  PNP switches are not supported. NO switches can also be used on any switch input

The first four axes have single limit inputs that can be accessed via the RJ45 limit breakout connector.  A sample design for a breakout panel is included in the CAM_Outputs folder.  GRBL always knows the direction of travel so individual min and max pins are not required.  Auto-squaring is supported by enabling ganged axes in GRBLHAL and setting the appropriate pins.

In addition to the limit signals, there are two probe input pins on the limit RJ45 breakout connector and the main PCB that are multiplexed via XOR logic and share a single input pin on the microcontroller.

For the dual-input signal there is no need to terminate unused ports.

The RJ45 pinout:

<img src="/readme_images/limit_rj45_pinout.jpg" width="150">

When using an open-air touch plate with the limit BoB, an optocoupler module is reccommended.

### User Button Breakout
<img src="/readme_images/User_mod_render.jpg" width="400">

Standard GRBL functions are mapped to 4 inputs.  These signals are primarily intended to be used via the user RJ45 connector.  For convenience, the HALT and DOOR signals are also exposed via 3 wire connections on the main PCB.  When multiplexed these signals must be NO logic.

The RJ45 pinout:

<img src="/readme_images/user_rj45_pinout.jpg" width="150">

### Encoder Breakout
<img src="/readme_images/encoder_render.jpg" width="400">

The encoder breakout board allows you to use the encoder inputs as auxilliary inputs.  The inputs are pulled up to 5V and should be connected to NPN outputs.  These high-speed inputs should be kept short and connection to the controller is via the RJ45 connection so that the integrity of differential transmission is preserved.

The RJ45 pinout:

<img src="/readme_images/encoder_rj45_pinout.jpg" width="150">

The terminal plug pinout:

<img src="/readme_images/encoder_bob_pinout.png" width="400">
