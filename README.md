

# Distance Relay Simulation using Discrete Fourier Transform

This project implements a three-zone mho characteristic relay for transmission line protection. The relay includes appropriate time delays to simulate realistic behavior. The simulation models various fault conditions, calculates apparent impedance, and demonstrates the relay's decision-making process.

## Key Features
- **Three-Zone Mho Characteristic Relay**: Implements a relay scheme that covers multiple zones of protection with defined time delays.
- **Fault Simulation**: Models various fault conditions (e.g., line-to-line, line-to-ground faults) to test the relay's performance.
- **Apparent Impedance Calculation**: Uses power system parameters to compute apparent impedance under different fault scenarios.
- **Decision-Making Process**: Demonstrates the relay's logic in detecting faults and issuing trip signals.

## Components
1. **Simulation Framework**:
   - Developed using Jupyter Notebooks for interactive simulations.
   - Python scripts for numerical computations and control logic.

2. **Discrete Fourier Transform**:
   - Calculates fundamental frequency components of the fault signals.
   - Filters noise and harmonics to ensure accurate impedance calculation.

3. **Visualization**:
   - Graphical representation of fault conditions, impedance trajectory, and relay zones.
   - Helps in analyzing the relay's response under various scenarios.

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/7supriyo/Distance-Relay-Simulation-using-Discrete-Fourier-Transform.git
   cd Distance-Relay-Simulation-using-Discrete-Fourier-Transform
   ```
2. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```
3. Open the Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
4. Execute the cells in the provided notebook to run the simulation.


![download](https://github.com/user-attachments/assets/f55aaa2f-d82d-4377-a835-4d8cba8f92e1)


## Applications
- Demonstrates the use of distance relays for power system protection.
- Provides insights into the impact of fault conditions on system stability.
- Useful for educational purposes and as a simulation tool for relay engineers.

## Contributions
Contributions are welcome! Feel free to open issues or submit pull requests to improve the project.

## License
This project is licensed under the [MIT License](LICENSE). Please see the LICENSE file for details.

---
