## EmbedCore - BLDC Motor Controller

EmbedCore motor controller is a high-power brushless motor controller. It was specifically designed to be integrated in Autonomus Mobile Robot wheel actuators. Motor controller can be intagreted to other applications.
BLDC Motor Controller is also my final thesis work at Subotica Tech - College of Applied Sciences.

***

## SPECIFICATIONS

| Parameter | EmbedCore BLDC Controller V1.0 | 
| --- | --- |
| Voltage Input | 12-44V |
| Peak Electrical Power | TBD |
| Mass | TBD |
| Peak Phase Current | 100A |
| Communication | 5Mbps CAN-FD & RS485 |
| Cooling | 12V Fan |
| Positioning | 2x Onboard 14-bit Encoders |
| Control rate | 15-30kHz |
| PWM Switching Rate | 15-60kHz |
| MCU | STM32G474 |
| Dimensions | 67 x 76.5mm |

***

## DIRECTORY STRUCTURE

```
BLDC motor controller
├── 3D                             # 3D render pictures of the board
├── Datasheets                     # Main component datasheets
├── Specification                  # Specification description about the project
├── Documentation
│   |── Schematic                  # PDF Schematic
│   |── PCB                        # PCB Documentation in PDF
│   |── Computations               # Computations for the components
├── lib
    |── 3d_models                  # Component 3D models
    |── lib_fp                     # Footprint libraries
    |── lib_sym                    # Symbol libraries
├── Logos                          # EmbedCore logo
├── Manufacturing
│   |── Gerber                     # Gerbers files
│   |── BOOM                       # Bill of matirials
│   |── Component Postions         # Components positions for PCB assembly
│   |── Drill files                # Drill files for assembly
├── Templates                      # Title block templates
```

## FIRMWARE

Associated firmware is in [BLDC Motor Controller - Firmware](https://gitlab.com/autonomus-mobile-robot/firmware) repository.

## Lisence
The project is under Apache License 2.0 lisence.

## Support
If you need help about this board, you can reach me at this mail: embedcore7@gmail.com

***
