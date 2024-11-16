# Setting Up a Virtual Environment for a New Python Project in VS Code

## **What is a Virtual Environment?**
A **virtual environment** is an isolated workspace that contains a specific Python interpreter and its associated libraries. It allows you to manage project dependencies independently from other projects or the system-wide Python installation.

---

## **Why You Need a Virtual Environment**
### Key Benefits:
1. **Dependency Isolation**:
   - Prevents conflicts between libraries required by different projects.
   - Ensures that each project has its own set of dependencies.

2. **Reproducibility**:
   - Allows precise control over dependency versions, making it easier to reproduce and share your project setup.

3. **Avoids Modifying the System Environment**:
   - Keeps the base Python installation clean and unaffected by project-specific packages.

4. **Facilitates Collaboration**:
   - Makes it easier to share the project with others, as the required dependencies can be documented and recreated using `requirements.txt`.

5. **Supports Multiple Python Versions**:
   - Enables projects to use different Python versions on the same system.

---

## **Step-by-Step Guide**

### **1) Install VS Code Jupyter Extension**
- Open VS Code.
- Go to the Extensions Marketplace (Ctrl+Shift+X on Windows).
- Search for and install the **Jupyter** extension.
- (Optional) Also install the **Python** extension for enhanced Python support.

---

### **2) Create a Project Folder and Main File**
1. Create a folder for your project:
   - Example: `market_research_project/`.
2. Add a main file:
   - For Python scripts: `main.py`
   - For Jupyter Notebooks: `main.ipynb`

---

### **3) Create, Activate, & Select Your Virtual Environment**
You can use either **venv** (default) or **Conda** depending on your project needs:

#### **Using venv** (Default Option):
1. Create a virtual environment:
   ```bash
   python -m venv my_project_env
   ```
   Replace `my_project_env` with your environment name (e.g., `market_research_env`).

2. Activate the environment:
   ```bash
   my_project_env\Scripts\activate
   ```
   (For macOS/Linux, use `source my_project_env/bin/activate`.)

3. Confirm activation:
   - Your terminal prompt will change to show `(my_project_env)`.

#### **Using Conda**:
1. Create a Conda environment:
   ```bash
   conda create --name my_project_env python
   ```
2. Activate the environment:
   ```bash
   conda activate my_project_env
   ```
3. Confirm activation:
   - Run `conda info --envs` to see the active environment marked with `*`.

---

### **4) Install Required Packages/Dependencies**
#### **For venv**:
Install packages using `pip`:
```bash
pip install numpy pandas matplotlib
```

#### **For Conda**:
Install packages using `conda`:
```bash
conda install numpy pandas matplotlib
```

---

### **5) For Jupyter: Add the Environment as a Jupyter Kernel**
1. Install the Jupyter kernel package:
   ```bash
   conda install ipykernel
   ```

2. Register the environment as a kernel:
   ```bash
   python -m ipykernel install --user --name=my_project_env --display-name "Python (My Project)"
   ```

   - Replace `my_project_env` with your environment name.
   - The `--display-name` argument is optional and sets a user-friendly name for the kernel.

---

### **6) Select the Python Interpreter for .py or .ipynb Files**

#### **For Python Files (.py):**
1. Open your project in VS Code.
2. Open the Python file you want to work on (`.py` file).
3. Open the **Command Palette** by pressing `Ctrl+Shift+P` (or `Cmd+Shift+P` on macOS).
4. Type and select:
   ```
   Python: Select Interpreter
   ```
5. From the list, choose the virtual environment or Conda environment you created (e.g., `my_project_env`).

#### **For Jupyter Notebooks (.ipynb):**
1. Open your project in VS Code.
2. Open the **Jupyter Notebook file** (`.ipynb`).
3. At the top-right of the notebook interface, find the **Jupyter Kernel Selector** dropdown.
4. Click the dropdown and select the kernel corresponding to the virtual environment or Conda environment you created:
   - The name should match the one you set during kernel registration (e.g., "Python (My Project)").
   - If you don't see it, make sure you've added the environment as a kernel (refer to Step 5).

---

## **Best Practices for Project Isolation**

### **1) Avoid Modifying the Base/Global Environment**
- **Always Activate an Environment**:
  - Before installing packages or running code, activate the environment with `conda activate` or `source .../activate`.
  
- **Double-Check the Active Environment**:
  - Use `conda info --envs` to confirm the active environment (marked with `*`).
  - Verify the Python executable:
    ```bash
    where python
    python -c "import sys; print(sys.executable)"
    ```

- **Never Install Packages Globally**:
  - Ensure no commands like `pip install` are run without activating an environment.

---

### **2) Document Dependencies**
- Save the dependencies of your project to a file for easy reproduction:
  ```bash
  pip freeze > requirements.txt
  ```

- Reinstall dependencies in a new environment:
  ```bash
  pip install -r requirements.txt
  ```

---

## **Recap**
- Virtual environments provide **dependency isolation**, **reproducibility**, and **project organization**.
- Use **venv** for lightweight environments and **Conda** for complex dependency management.
- Always activate your environment and ensure the correct interpreter is selected in VS Code or Jupyter.
