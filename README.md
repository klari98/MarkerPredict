

---

# Project Setup and Troubleshooting

## Introduction

To run the codes in this project, we created a .toml file, so creating virtual environments and installing dependencies is possible with the Poetry Python package.
This document outlines the steps taken to set up and troubleshoot Poetry with Python, focusing on resolving issues related to virtual environments and Python version compatibility.

## Steps to Set Up and Troubleshoot Poetry

### 1. Verify Python Installation

Ensure that Python 3.9 is correctly installed and accessible:

```powershell
C:\Users\YourUsername\AppData\Local\Programs\Python\Python39-32\python.exe --version
```

This should output Python 3.9.x. If it fails, reinstall Python 3.9.

### 2. Reconfigure Poetry to Use Python 3.9

1. **Remove Existing Virtual Environment**

   ```powershell
   poetry env remove python
   ```

2. **Set Python Version for Poetry**

   ```powershell
   poetry env use C:\Users\YourUsername\AppData\Local\Programs\Python\Python39-32\python.exe
   ```

3. **Reinstall Dependencies**

   If using `poetry install` is not preferred, skip this step. 

### 3. Manually Create and Manage Virtual Environment (If Needed)

1. **Create Virtual Environment**

   ```powershell
   C:\Users\YourUsername\AppData\Local\Programs\Python\Python39-32\python.exe -m venv myenv
   ```

2. **Activate Virtual Environment**

   ```powershell
   .\myenv\Scripts\activate
   ```

3. **Install Poetry in the Virtual Environment**

   ```powershell
   pip install poetry
   ```

4. **Initialize Poetry**

   Navigate to your project directory and run:

   ```powershell
   poetry init
   ```

5. **Add Dependencies**

   Manually add dependencies as needed:

   ```powershell
   poetry add <dependency>
   ```

### 4. Run Jupyter Notebook (If Required)

1. **Add Jupyter Notebook**

   ```powershell
   poetry add jupyter
   ```

2. **Run Jupyter Notebook**

   ```powershell
   poetry run jupyter notebook
   ```

### 5. Troubleshooting Common Issues

1. **Python Executable Issues**

   Verify that the correct Python executable is being used and is functional.

2. **Virtual Environment Errors**

   Ensure that old or conflicting virtual environments are removed.

3. **Configuration Issues**

   Check and reset Poetry’s configuration:

   ```powershell
   poetry config --list
   poetry config --unset virtualenvs.prefer-active-python
   ```

4. **Permissions Errors**

   Run PowerShell or Command Prompt as an Administrator if facing permission issues.

## Summary

- **Verify Python Installation**.
- **Reconfigure Poetry and Set Python Version**.
- **Manually Create and Manage Virtual Environment** if needed.
- **Run Jupyter Notebook** and troubleshoot common issues.

For further assistance, refer to Poetry and Python documentation or seek help from relevant forums.

---

Replace `YourUsername` with your actual Windows username in the file.