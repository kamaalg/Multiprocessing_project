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
``
