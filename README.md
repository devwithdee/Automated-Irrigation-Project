# Automated Irrigation Monitoring System

This project is an Arduino based automated irrigation monitoring system that uses a soil moisture sensor to determine when a plant needs water. When the soil is dry, the system activates a water pump for a set duration. The project also includes an LCD display and keypad interface so users can monitor the system and adjust watering duration.

## Project Overview

The system was designed as a solar powered irrigation prototype using Arduino microcontrollers, soil moisture sensors, a pump, a buck converter, and supporting circuit components. It automates irrigation scheduling based on real time soil moisture readings.

This project won 1st Place at the Weill Cornell High School Research Competition.

## Key Features

- Detects soil moisture levels
- Automatically activates water pump when soil is dry
- Displays soil status and estimated water usage on LCD
- Allows keypad control for watering duration
- Includes manual watering option
- Includes water usage reset option
- Designed to work as part of a solar-powered circuit

## Hardware Used

- Arduino microcontroller
- Soil moisture sensor
- Water pump
- Transistor for pump control
- Buck converter
- Solar panel and battery supply
- 20x4 I2C LCD display
- 4x4 keypad
- Breadboard and jumper wires

## Pin Setup

| Component | Arduino Pin |
| Soil Moisture Sensor | 12 |
| Pump Control | 11 |
| Keypad Rows | 9, 8, 7, 6 |
| Keypad Columns | 5, 4, 3, 2 |
| LCD | I2C address 0x27 |

## Keypad Controls

| Key | Function |
| 1-9 | Set watering duration in 5-second increments |
| 0 | Manual watering |
| * | Reset total water usage |

## How It Works

1. The soil moisture sensor checks whether the soil is dry or moist.
2. If the soil is dry, the Arduino turns on the pump.
3. The pump runs for the selected watering duration.
4. The LCD updates with soil status, watering duration, and estimated water used.
5. The keypad allows the user to adjust watering duration or manually water the plant.

## Notes

Depending on the soil moisture sensor, the dry/wet readings may be reversed. If the pump activates when the soil is wet instead of dry, switch the HIGH and LOW condition in the "manageWatering()" function.

