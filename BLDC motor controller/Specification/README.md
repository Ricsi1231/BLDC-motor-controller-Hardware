# BLDC motor controller Specification

- BLDC Motor Controller Hardware General Description:
    - Operating voltage range: 12V - 44V.
    - Built-in bulk capacitance (200µF) for stable motor control and power supply. External precharge circuit required when connecting multiple boards.
    - Multiple voltage rails (3.3V, 3.3VA, 5V, 12V) for stable power supply.
    - Field-Oriented Control (FOC) for BLDC motor operation.
    - Current handling: 30A continuous, 100A peak.
    - Compatible with multiple BLDC motor types.
    - Supports RS485 and CAN communication protocols.
    - Hall sensors for closed-loop control.
    - Temperature monitoring for motor and MOSFETs.
    - Motor cooling capability.
    - Status indicator LEDs.
- Components:
    - **Buck converter**: LMR36506-Q1 - Converts 6S battery voltage to 5V and 12V, providing 600mA for fan and external peripherals.
    - **Buck converter**: TPS62172 - Converts 5V to 3.3V system voltage with 500mA output.
    - **LDO**: LP2992 - Converts 5V to 3.3V analog voltage with 250mA maximum output.
    - **MCU**: STM32G474RET6 - Low-power, high-performance MCU optimized for battery-powered applications.
    - **Motor controller**: DRV8353 - Advanced motor control IC with high current capability, controlling N-Channel MOSFETs.
    - **N-Channel MOSFETs**: TPW1R306PL,L1Q - Two MOSFETs per channel.
    - **NTC**: NTCS0402E3473FXT - Temperature sensor for MOSFETs.
    - **NTC**: TBD - Temperature sensor for motor.
    - **Encoders:** ASS5047P & AS5048B - Commutation and disambiguation encoders.
    - **CAN transceiver**: TCAN334GDCNT.
    - **RS485 transceiver**: SP3494.
    - **Cooling fan PWM driver**: DGD0216.
    - **Debug LEDs**: Two status indicators (red and green) for user feedback.
    - **Power connector**: 2× XT60.
    - **Input connectors**: One motor temperature sensing connector.
    - **Output connectors**: One 3-pin motor phase connector, one cooling connector.
    - **I/O connectors**: Two encoder connectors, two 3-pin CAN connectors, two 3-pin RS485 connectors, one SWD connector for debugging and firmware updates.
    
    ### STM32-based Firmware
    
    - Uses STM32 HAL library for efficient development.
    - Implemented in C++ to manage project complexity.
    - Class-based driver implementation for each device.
    - Separate classes for control algorithms including PID.
    - FreeRTOS implementation for task management.
    - Documented with block diagrams for architecture and functionality.
    - Layered architecture design.
    - Comprehensive error handling with device cross-monitoring.
    - Configurable settings with RS485 & CAN messaging support.
    - DMA and interrupt handling for I2C, SPI, UART, CAN, GPIO, and PWM.
    - Optimized memory management to prevent leaks.
    - Unit testing for all modules.