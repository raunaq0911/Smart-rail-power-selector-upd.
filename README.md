# Smart Power Rail Selector

A compact hardware project demonstrating a selectable power rail system for electronics prototyping. This project allows safe selection between multiple voltage sources (3.3V, 5V, 12V) with backfeed protection using Schottky Diodes.
## Features
- Selectable output between 3.3V, 5V, and 12V rails
- Schottky diode protection to prevent backfeed
- Current-limited indicator LEDs for each rail
- Compact 2-layer PCB design on a 60mm x 40mm board suitable for prototyping 
- Practical hardware design trade-offs
## Components
- SS14 Schottky diodes for rail protection
- LTST-C190 LEDs: Green (3.3V), Red (5V), Blue (12V)
- Series resistors calculated for ~15mA LED current
- 2-layer PCB with **pin headers** for input/output connections
## Design Considerations
- Voltage drop due to Schottky diodes: ~0.2V at 15mA
- Resistor values selected to maintain ~15mA LED current after diode drop:
  - Green (3.3V): 68Ω
  - Red (5V): 200Ω (split into two series resistors: 100Ω + 100Ω)
  - Blue (12V): 560Ω
- Schottky diodes kept for safety and to demonstrate real-world engineering trade-offs
## Usage
1. Connect 3.3V, 5V, and 12V sources to the input pins (via jumper wires or mating connectors).
2. Use the jumper to select the desired output rail.
3. Observe the corresponding LED for visual confirmation.
4. Connect the load to the output pins.
