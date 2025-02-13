![image](https://github.com/user-attachments/assets/91939ec9-7ade-4d8d-a817-cef9d9284779)


![Powered by NumFOCUS](https://img.shields.io/badge/powered%20by-NumFOCUS-blue)
![Scheduled](https://img.shields.io/badge/Scheduled-grey?logo=github)
![Passing](https://img.shields.io/badge/passing-green)
![Docs Passing](https://img.shields.io/badge/docs-passing-brightgreen)
![Codecov](https://img.shields.io/badge/codecov-99%25-green)
![Release](https://img.shields.io/badge/release-v25.1.1-orange)
![Ruff](https://img.shields.io/badge/Ruff-lightgrey)
![Open in Colab](https://img.shields.io/badge/Open%20in%20Colab-blue?logo=googlecolab)
![DOI](https://img.shields.io/badge/DOI-10.5334/jors.309-blue)
![Contributors](https://img.shields.io/badge/all%20contributors-77-orange)

# LiSimPack: A Python Library for Battery Pack Simulations with PyBaMM

**LiSimPack** is a Python library built on top of **PyBaMM** (Python Battery Mathematical Modelling) for simulating multi-cell battery packs. It allows users to model battery packs with various configurations, including multi-cell setups, thermal management, and voltage balancing. This library integrates seamlessly with PyBaMM, enabling efficient electrochemical simulations for applications in electric vehicles (EVs), energy storage systems, and portable electronics.

## Features
- **Multi-cell Battery Modeling**: Simulate and analyze the behavior of battery packs with multiple cells connected in series or parallel.
- **Thermal Management**: Simulate temperature effects on battery pack performance and incorporate cooling strategies.
- **Voltage Balancing**: Analyze and optimize voltage balancing techniques for improved battery performance and lifespan.
- **Integration with PyBaMM**: Leverage the powerful electrochemical simulations provided by PyBaMM for battery modeling.
- **Customizable Simulation Parameters**: Set up and adjust various parameters, including battery chemistry, current profiles, and more.

## Installation
To install **LiSimPack**, ensure you have Python 3.6+ and the necessary dependencies:

```sh
pip install pybamm
pip install LiSimPack
```

## Usage
### Import LiSimPack and PyBaMM
```python
import lisimpack
import pybamm
```

### Define Battery Pack
```python
# Example: Create a 2-series, 3-parallel battery pack
battery_pack = lisimpack.BatteryPack(n_cells_series=2, n_cells_parallel=3)
```

### Run Simulation
```python
# Set up a simulation with defined current profile and temperature
simulation = lisimpack.Simulation(battery_pack, current_profile="drive_cycle", temperature=25)
simulation.run()
```

### Visualize Results
```python
simulation.plot()
```

## Documentation
For detailed documentation and example use cases, please refer to the official documentation.

## Contributing
We welcome contributions to **LiSimPack**! If you'd like to contribute, please fork the repository, make your changes, and submit a pull request.

## License
**LiSimPack** is licensed under the **MIT License**. See `LICENSE` for more information.

## Acknowledgments
- **PyBaMM**: For providing the core simulation framework for battery modeling.
- Contributors and the open-source community for their continuous support and contributions.

