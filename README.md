 

# CH32V003 RISC-V MCU: Detailed Summary

## Overview
The CH32V003 is an ultra-low-cost RISC-V microcontroller (MCU) manufactured by WCH. It offers a compelling combination of performance, features, and affordability, making it suitable for a wide range of embedded applications.

## Key Features
- **Core**: 32-bit "RISC-V2A" architecture
- **Clock Speed**: Up to 48 MHz
- **Memory**: 2KB SRAM
- **Storage**: 16KB flash (reprogrammable)
- **Package Options**: TSSOP20, QFN20, SOP16, SOP8
- **Pricing**: Reported to be under 10 cents in quantity (exact quantity unspecified)

## Detailed Specifications

### CPU
- 32-bit RISC-V2A core
- Maximum clock frequency: 48 MHz

### Memory and Storage
- SRAM: 2KB
- Flash: 16KB (reprogrammable, not OTP)

### GPIO
- Up to 18 General Purpose Input/Output pins
- Interrupt support on GPIO pins

### Communication Interfaces
- 1x USART (Universal Synchronous/Asynchronous Receiver/Transmitter)
- 1x I2C (Inter-Integrated Circuit)
- 1x SPI (Serial Peripheral Interface)

### Analog Features
- 10-bit ADC (Analog-to-Digital Converter)
- Up to 8 ADC channels

### Debug Interface
- 1-Wire debug interface

### DMA
- General purpose DMA (Direct Memory Access) controller

### Timers
- 1x 16-bit advanced timer
- 1x 16-bit general-purpose timer
- 2x watchdog timers
- 1x 32-bit system timer

### Additional Features
- 64-bit chip unique ID
- Power-on Reset (POR)
- Programmable voltage detector

### Power
- Supply voltage: 3.3V or 5V
- Low power modes: Sleep and Standby

## Available Variants
Four variants of the CH32V003 are currently available:
1. CH32V003F4P6
2. CH32V003F4U6
3. CH32V003A4M6
4. CH32V003J4M6

These variants primarily differ in the number of available GPIOs and package types.

## Development Tools and Resources
- SDK with C code samples provided by WCH
- MounRiver Studio IDE for development
- Small development board based on CH32V003F4P6 for evaluation
- Documentation available (primarily in Chinese)
- Source code comments in English

## Market Position
While not the absolute cheapest microcontroller on the market, the CH32V003 offers a unique combination of features at its price point. Unlike many comparably priced MCUs that use OTP (One-Time Programmable) flash, the CH32V003 provides reprogrammable flash memory, enhancing its flexibility and reusability in development contexts.

## Limitations and Considerations
- Limited documentation in English (primarily Chinese)
- Relatively new product, which may affect ecosystem maturity and third-party support

## Conclusion
The CH32V003 RISC-V MCU presents an attractive option for embedded systems designers looking for a low-cost, feature-rich microcontroller. Its combination of processing power, peripheral options, and reprogrammable flash at a sub-10 cent price point makes it particularly suitable for cost-sensitive applications or projects requiring high-volume production.


### sample program that demonstrates many of the features of the CH32V003 RISC-V MCU. 

This program will showcase GPIO, UART, SPI, I2C, ADC, and timer functionality.

demo.md

I've created a sample program that demonstrates many of the features of the CH32V003 RISC-V MCU. This program showcases the following features:

1. GPIO: Toggles an LED connected to GPIOC Pin 0.
2. ADC: Reads an analog value from ADC channel 0.
3. UART: Sends the ADC value over UART.
4. SPI: Transmits a dummy byte (0xAA) over SPI.
5. I2C: Performs a dummy write to an I2C device (address 0x3C).
6. Timer: Uses Timer 2 for a millisecond delay function.

Here's a brief explanation of the program:

1. The program initializes all the peripherals in the `main()` function.
2. In an infinite loop, it performs the following actions:
   - Toggles the LED
   - Reads the ADC value
   - Sends the ADC value over UART
   - Transmits a byte over SPI
   - Performs an I2C write operation
   - Waits for 1 second using the timer-based delay function

3. Each peripheral has its own configuration function, which sets up the necessary registers and enables the peripheral.

4. The `delay_ms()` function uses Timer 2 to create precise millisecond delays.

This program demonstrates the basic usage of many features of the CH32V003 MCU. However, please note that this is a simplified example and doesn't include error handling or more advanced features. In a real-world application, you would need to add proper error checking and potentially use interrupts for more efficient operation.

Also, keep in mind that you might need to adjust some configurations (like pin assignments) based on your specific hardware setup and requirements.

 
