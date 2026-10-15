# Python Libraries and Setup

This project uses Python libraries for data cleaning, exploratory data analysis, visualization, and statistical hypothesis testing on NYC Taxi Trip data.

## 1. Python Libraries Used

| Library | Import Statement | Purpose |
|---|---|---|
| Pandas | `import pandas as pd` | Data cleaning, DataFrames, grouping, and statistical summaries |
| Matplotlib | `import matplotlib.pyplot as plt` | Creating histograms, pie charts, and plots |
| Seaborn | `import seaborn as sns` | Statistical data visualization |
| SciPy | `import scipy.stats as st` | Hypothesis testing using t-tests |
| Statsmodels | `import statsmodels.api as sm` | Creating Q-Q plots and statistical analysis |
| Warnings | `import warnings` | Managing Python warning messages |
| Sys | `import sys` | Checking the active Python interpreter |

**Note:** `warnings` and `sys` are part of Python's standard library and do not require installation.

## 2. Check Your Python Environment

Before installing packages, check which Python environment is running your notebook.

```python
import sys

print(sys.executable)
```

This displays the path of the Python interpreter currently executing the notebook.

## 3. Install Python Libraries

### Method 1: Install from Jupyter Notebook

Run this in a notebook cell:

```python
import sys
!{sys.executable} -m pip install pandas matplotlib seaborn scipy statsmodels
```

Using `sys.executable` helps install packages into the Python environment used by the current notebook kernel.

### Method 2: Install from the VS Code Terminal

Open **Terminal → New Terminal** and run:

```bash
python -m pip install pandas matplotlib seaborn scipy statsmodels
```

If the terminal and notebook use different Python environments, install the packages using the interpreter path printed by `sys.executable`.

## 4. Import All Libraries

Add these imports at the beginning of your notebook:

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import scipy.stats as st
import statsmodels.api as sm
import warnings
import sys

warnings.filterwarnings("ignore")
```

## 5. Requirements File for GitHub

Create a file named `requirements.txt` in your project folder and add:

```text
pandas
matplotlib
seaborn
scipy
statsmodels
```

To install all project dependencies later, run:

```bash
python -m pip install -r requirements.txt
```

For reproducible results, you can record the installed package versions using:

```bash
python -m pip freeze > requirements.txt
```

Run this command in the same Python environment used by your project.

## 6. How These Libraries Are Used in the Project

- **Pandas:** Reads the CSV dataset, cleans missing values and duplicates, processes timestamps, calculates trip duration, and groups records for analysis.
- **Matplotlib:** Visualizes fare amounts, trip distances, and payment preferences.
- **Seaborn:** Imported for statistical visualization.
- **SciPy:** Performs the independent two-sample t-test to compare average fares between Card and Cash transactions.
- **Statsmodels:** Creates Q-Q plots to examine the distribution of fare amounts.
- **Warnings:** Suppresses warning messages during execution.
- **Sys:** Identifies the active Python interpreter and helps install packages into the correct environment.

## 7. Project Setup Checklist

- [ ] Install Python and configure the correct interpreter.
- [ ] Install the required libraries.
- [ ] Select the matching Python environment or Jupyter kernel in VS Code.
- [ ] Keep the dataset in the expected project location.
- [ ] Add `requirements.txt` to the GitHub repository.
- [ ] Verify that all notebook cells execute successfully.

**Important:** The `statsmodels` package name ends in **s**. Its correct import statement is `import statsmodels.api as sm`.
