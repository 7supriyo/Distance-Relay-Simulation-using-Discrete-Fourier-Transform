# Distance Relay Simulation using DFT

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Simulation](https://img.shields.io/badge/Type-Simulation-orange)

A Python implementation of a numerical distance relay with three-zone mho characteristics using Discrete Fourier Transform (DFT) for phasor estimation.

## Table of Contents
- [Project Description](#project-description)
- [Key Features](#key-features)
- [System Model](#system-model)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)
- [References](#references)

## Project Description

This project simulates a modern numerical distance relay for transmission line protection, featuring:

- Three-zone stepped distance protection
- Mho characteristic implementation
- DFT-based phasor estimation
- Support for multiple fault types (LG, LL)
- Dynamic impedance trajectory visualization

The simulation models a complete power system including source, transmission line, and load impedances, with configurable fault scenarios.

## Key Features

- **Phasor Estimation**: Accurate DFT implementation with one-cycle window
- **Fault Modeling**: Phase-to-ground and phase-to-phase faults
- **Relay Characteristics**:
  - Zone 1: 80% reach, instantaneous trip
  - Zone 2: 120% reach, 0.3s delay
  - Zone 3: 150% reach, 1.0s delay
- **Visualization**:
  - Voltage and current waveforms
  - R-X diagrams with impedance trajectory
  - Relay operating characteristics

## System Model

The simulated system parameters:

| Parameter            | Value                      |
|----------------------|----------------------------|
| System Voltage       | 220 kV (L-L)               |
| Frequency            | 50 Hz                      |
| Line Length          | 100 km                     |
| Line Impedance       | 0.02 + j0.4 Ω/km           |
| Source Impedance     | 1 + j10 Ω                  |
| Load Impedance       | 200 + j150 Ω               |
| Sampling Frequency   | 1 kHz                      |

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/distance-relay-simulation.git
cd distance-relay-simulation
Install required packages:

bash
pip install -r requirements.txt
Usage
Run the main simulation script:

bash
python main.py
Configuration Options
Modify config.py to change system parameters:

python
# Fault parameters
FAULT_TYPE = 'PG'  # 'PG' (phase-ground) or 'PP' (phase-phase)
FAULT_LOCATION = 0.6  # percentage of line length
FAULT_RESISTANCE = 1.0  # ohms
FAULT_START_TIME = 0.2  # seconds
FAULT_DURATION = 0.6  # seconds

# Relay settings
Z1_REACH = 0.8  # 80% of line
Z2_REACH = 1.2  # 120% of line
Z2_DELAY = 0.3  # seconds
Z3_REACH = 1.5  # 150% of line
Z3_DELAY = 1.0  # seconds
Results
The simulation generates two main plots:

Waveforms: Shows voltage and current during fault conditions
Waveforms

R-X Diagram: Displays impedance trajectory and relay zones
R-X Diagram

Example output:

--- Simulation Summary ---
Fault Type: PG
Fault Location: 60.0% (60.0 km)
Fault Resistance: 1.0 Ohms
Fault Start Time: 0.2 s
--- TRIP --- Zone 1 detected at t = 0.2170 s
             Impedance: 12.42 + 24.85j Ohms
             Estimated Fault Distance: 62.12 km
Project Structure
distance_relay_simulation/
│
├── main.py                # Main simulation script
├── config.py              # Configuration parameters
├── requirements.txt       # Dependencies
├── README.md              # This file
├── modules/
│   ├── system_model.py    # Power system modeling
│   ├── fault_model.py     # Fault calculations
│   ├── relay_algorithm.py # Protection logic
│   └── visualization.py   # Plot generation
├── tests/                 # Unit tests
└── results/               # Output figures
Contributing
Contributions are welcome! Please follow these steps:

Fork the repository

Create your feature branch (git checkout -b feature/yourfeature)

Commit your changes (git commit -m 'Add some feature')

Push to the branch (git push origin feature/yourfeature)

Open a Pull Request

License
This project is licensed under the MIT License - see the LICENSE file for details.

References
IEEE Std C37.113-2015, IEEE Guide for Protective Relay Applications to Transmission Lines

J. Lewis Blackburn, Protective Relaying: Principles and Applications

A.G. Phadke, Computer Relaying for Power Systems




1. **Project Overview**: Clear description of what the project does
2. **Key Features**: Highlighted technical capabilities
3. **System Model**: Quick reference for system parameters
4. **Installation/Usage**: Step-by-step instructions
5. **Results**: Example outputs with images
6. **Project Structure**: Directory layout explanation
7. **Contribution Guideli
