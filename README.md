# survivalML
Tutorials for survival analysis using Machine Learning Methods  

# Installation Guide

This project requires **Python ≥ 3.10** and the following packages:

* `numpy`
* `pandas`
* `matplotlib`
* `scikit-learn` (imported as `sklearn`)
* `scikit-survival` (imported as `sksurv`)
    Documentation & Installation: https://scikit-survival.readthedocs.io/en/stable/index.html
* `torch` (PyTorch)
    Documentation & Installation: https://pytorch.org/get-started/locally/
* `pycox`  
    Documentation & Installation: https://github.com/havakv/pycox

> **Note:** `random` is part of Python’s standard library and does NOT need to be installed.

---

## 1. Check Your Python Version

```bash
python --version
# or
python3 --version
```

Make sure the version is **3.10 or higher**.

---

# Option A (Recommended): Using `venv` + `pip`

## Step 1: Create a Virtual Environment

You can call `.venv` whatever you want, but make it helpful. For example, my virtual environment is called `surv-env`. 

### macOS / Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### Windows (PowerShell)

```powershell
py -3.10 -m venv .venv
.\.venv\Scripts\Activate.ps1
```

You should now see `(.venv)` in your terminal prompt.

---

## Step 2: Upgrade pip

```bash
python -m pip install --upgrade pip setuptools wheel
```

---

## Step 3: Install Core Scientific Packages

```bash
python -m pip install numpy pandas matplotlib scikit-learn
```

---

## Step 4: Install scikit-survival

```bash
python -m pip install scikit-survival
```

> If installation fails due to compiler issues, consider using the Conda instructions below.

---

## Step 5: Install PyTorch (`torch`)

PyTorch installation depends on:

* Your operating system
* Whether you want CPU or GPU (CUDA) support

Go to the official PyTorch installation page and select your configuration:

👉 [https://pytorch.org/get-started/locally/](https://pytorch.org/get-started/locally/)

Then copy and run the command it provides.

---

## Step 6: Install PyCox (`pycox`)

⚠️ **Important:** PyTorch must be installed before installing `pycox`.

Install using:

```bash
python -m pip install git+https://github.com/havakv/pycox.git
```

---

## Step 7: Verify Installation

Run the following test:

```bash
python - <<'PY'
import numpy as np
import pandas as pd
import matplotlib
import sklearn
import sksurv
import torch
import pycox
import random

print("All packages imported successfully!")
PY
```

If no errors appear, installation is complete.

---

# Option B: Using Conda (Recommended for scikit-survival)

If you use Anaconda or Miniconda:

```bash
conda create -n surv310 python=3.10 -y
conda activate surv310
conda install -c conda-forge numpy pandas matplotlib scikit-learn scikit-survival -y
```

Then install PyTorch (see official site):

👉 [https://pytorch.org/get-started/locally/](https://pytorch.org/get-started/locally/)

Finally install PyCox:

```bash
python -m pip install git+https://github.com/havakv/pycox.git
```

---

# Common Issues

### ImportError After Installation

Make sure:

* Your virtual environment is activated
* `pip` corresponds to the same Python version:

```bash
which python      # macOS/Linux
where python      # Windows
python -m pip --version
```

### Do NOT Install

```
pip install random
```

`random` is already included in Python.

---

# Required Python Version

```
Python >= 3.10
```

---
