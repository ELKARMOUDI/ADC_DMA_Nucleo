# STM32F411 Nucleo ADC with DMA

![STM32F411](https://img.shields.io/badge/STM32F411-Nucleo-blue)
![ADC](https://img.shields.io/badge/ADC1-DMA_Mode-green)

Continuous potentiometer reading using ADC1 with DMA for maximum efficiency.

## Features
- **DMA-Enabled** ADC conversions
- **Zero CPU Overhead** data collection
- **PA0 Analog Input** for potentiometer
- **84-cycle Sampling** (optimal speed/accuracy)
- **Circular Buffer** mode

## Hardware Setup
| Component | Connection | Nucleo Pin |
|-----------|------------|------------|
| Potentiometer | VCC → 3.3V | - |
| | GND → GND | - |
| | WIPER → PA0 | CN7 pin 10 |

## Technical Details
### ADC/DMA Configuration 
```c
ADC Clock: 8MHz (16MHz PCLK2 / 2)
Sampling Time: 84 cycles
DMA: Circular mode, 16-bit transfers
Buffer: sensorValue[1] (single-element)
