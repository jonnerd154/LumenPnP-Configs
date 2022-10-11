# LumenPnP-Configs

This repository contains the OpenPnP and Marlin configurations I use for my Opulo LumenPnP.

## Hardware Installed:
 - Original Opulo LumenPnP v2 BYOP Kit
 - Standard v3 Motherboard
   - Jumper wires soldered from DIAG1 on X and Y motor drivers, to their respective axis limit switch inputs
 - X & Y Linear Bearing rails (from @stargirl's mods, combining V2, V3 parts)
 - Sensorless homing on X/Y
 - Drag Chain / Cable Chain (installed using Opulo V3 machine parts)
 - Only Nozzle 1 is populated (not dual nozzle, yet)
 
 Build the Marlin firmware using Visual Studio and the Platform.io / Marlin plugin.

## Special Features Enabled:
 - Up/Down lights are on separate Actuators, and their respective cameras have antiglare and off-after-capture enabled.
 - Optimized camera settling time to 80ms.
 - Nozzle change operations optimized for reasonable speed, without jeopardizing reliability.
 - All vision pipelines use `DetectCircularSymmetry` where appropriate (fids, sprocket holes, nozzles)
 - All axis are using 32-step microstepping control to ensure accuracy of movements to 0.01mm, but without overloading the controller or making ugly sounds/vibrations.
 
## Kinematic Limits:

- X-Axis: 
  - Feed Rate: 500mm/s
  - Acceleration: 5000mm/s^2
  - Jerk: 30000mm/s^3

- Y-Axis: 
  - Feed Rate: 233.333mm/s
  - Acceleration: 5000mm/s^2
  - Jerk: 30000mm/s^3
