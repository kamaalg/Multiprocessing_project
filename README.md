# Sensitivity Analysis and LAKE Model Parallelization

This project provides a comprehensive framework for running sensitivity analyses and executing the LAKE model in parallel. The scripts automate the setup, execution, and management of LAKE model runs, including creating directories, copying necessary files, and processing output.

---

## Table of Contents
- [Features](#features)
- [Prerequisites](#prerequisites)
- 
- [Project Structure](#project-structure)
- [Contact](#contact)

---

## Features
- **Parallel Execution**: Run multiple LAKE model simulations in parallel, saving significant computation time.
- **Automatic Directory Creation**: Create structured directories for setup, data, and results.
- **File Management**: Copy and manage necessary files automatically.
- **Sensitivity Analysis**: Generate parameter samples and perform sensitivity analysis.
- **Error Handling**: Robust error checking during model runs.

---

## Prerequisites

1. Python 3.x
2. Required Python packages:
   - `numpy`
   - `scipy`
   - `multiprocessing`
   - `shutil`

Install dependencies using pip:
```bash
pip install numpy scipy

```

---

## Usage
```python
from sensitivity_analysis import SensitivityAnalysis

# Initialize the SensitivityAnalysis instance
sa = SensitivityAnalysis(work_dir="model_output", path_to_model_dir="LAKE-LAKE3.0")

# Create 5 directories for the LAKE model
sa.create_directories_auto(number_directories=5)

# Generate setup and driver files for the created directories
sa.generate_and_write_files(num_files=5)
# Run the LAKE model for a specific project directory
sa.run_model(rundirectory="model_output", project_directory="LAKE0")
# Define parameter names and their corresponding target values
params = ["param1", "param2"]
target_values = [[value1, value2], [value3, value4]]

# Perform sensitivity analysis for 5 projects
sa.create_and_run_sensitivity_analysis(
    number=5,                  # Number of projects
    p_name=params,             # Parameter names
    target_values=target_values,  # Target values for parameters
    rundirectory="model_output"  # Directory for running the analysis
)
```

---

## Project Structure
```
  ├── SensitivityAnalysis
  │   ├── sensitivity_analysis.py  # Main script
  │   ├── model_output             # Output directory
  │   └── LAKE-LAKE3.0             # LAKE model directory
  │       ├── setup
  │       ├── data

  │       ├── results
  │       └── lake.out
   ```
## Contact

For questions or further information, please contact:

- **Name**: Kamal Gurbanov  
- **Email**: [kamalgurbanov916@gmail.com](mailto:kamalgurbanov916@gmail.com)

