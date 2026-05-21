# STM32 DAC Ramp Waveform Generator

This project demonstrates ramp waveform generation using the STM32 DAC peripheral with Timer interrupt triggering.

The DAC output voltage increases gradually in fixed steps and resets after reaching the maximum value, creating a ramp waveform.


# Project Overview

The project uses:

- STM32 Microcontroller
- DAC1 Peripheral
- TIM6 Timer Interrupt
- STM32 HAL Library

TIM6 periodically triggers DAC value updates to generate a ramp signal.


# Features

- DAC based waveform generation
- Timer interrupt controlled DAC updates
- Ramp waveform output
- STM32 HAL based implementation
- Simple real-time signal generation


# Working Principle

1. TIM6 generates periodic interrupts.
2. Inside the interrupt callback:
   - DAC output value is updated.
   - DAC value increases by a fixed step.
3. When DAC value reaches maximum:
   - Value resets to zero.
4. Continuous ramp waveform is generated at DAC output.


# DAC Logic

dac_value += 200;

if (dac_value >= 4095)
{
    dac_value = 0;
}


# Peripherals Used

- DAC1
- TIM6
- GPIO
- STM32 HAL Drivers


# Software Used

- STM32CubeIDE
- STM32 HAL Library


# Timer Configuration

| Parameter | Value |
|---|---|
| Timer | TIM6 |
| Prescaler | 8000 |
| Period | 100 |
| DAC Resolution | 12-bit |


# Applications

- Signal generation
- Embedded waveform generation
- DAC learning project
- Analog output applications
- Embedded systems practice


# Output

Ramp waveform generated using DAC output pin.

![Output](https://github.com/sayalivadgaonkar18/STM32-DAC-Ramp-Waveform/blob/main/Images/Output.png?raw=true)
