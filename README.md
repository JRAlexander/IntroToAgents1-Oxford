# IntroToAgents1-Oxford
Repo for Intro to Agents lecture at Oxford

All links for the lecture are in the resource guide pdf.

## Installation Instructions

### Option 1: Using a Python Virtual Environment

#### **Step 1: Ensure Python is Installed**
Make sure you have Python **3.10 or later** installed. You can check your version by running:

```sh
python --version
```

If you need to install or update Python, download it from [python.org](https://www.python.org/downloads/) or use your package manager (e.g., `brew` for macOS, `apt` for Ubuntu, `choco` for Windows).

---

#### **Step 2: Create a Virtual Environment**
Navigate to your project directory:

```sh
cd introtoagents1-oxford
```

Then create a virtual environment named `intro2agents`:

```sh
python -m venv intro2agents
```

---

#### **Step 3: Activate the Virtual Environment**
- **Windows (Command Prompt or PowerShell):**
  ```sh
  intro2agents\Scripts\activate
  ```
- **macOS/Linux:**
  ```sh
  source intro2agents/bin/activate
  ```

When activated, your terminal prompt should show `(intro2agents)`, indicating that you're inside the virtual environment.

---

#### **Step 4: Install Dependencies**
With the virtual environment active, install all required packages from `requirements.txt`:

```sh
pip install -r requirements.txt
```

---

#### **Step 5: Verify Installation**
Check that everything installed correctly:

```sh
pip list
```

This will display all installed packages.

---

#### **Step 6: Deactivating the Virtual Environment (When Done)**
To exit the virtual environment, simply run:

```sh
deactivate
```

---

#### 🎯 **You’re Ready to Go!**
Your environment is now set up with all necessary dependencies. When working on your project, **always activate your virtual environment** before running Python scripts.

---

## Option 2: Using Miniconda and `environment.yml`

### **Step 1: Install Miniconda**
If you haven’t installed **Miniconda**, you can download it from:

🔗 **[Miniconda Download Page](https://docs.conda.io/en/latest/miniconda.html)**

#### **Installation Steps:**
- **Windows:**
  1. Download the **Miniconda Installer** (`Miniconda3 Windows 64-bit`).
  2. Run the installer and follow the instructions (ensure you check the option to add Conda to your `PATH`).
  3. Restart your terminal (Command Prompt or PowerShell).

- **macOS/Linux:**
  1. Download the **Miniconda Installer** for your OS.
  2. Open a terminal and navigate to the download folder.
  3. Run the installer:
     ```sh
     bash Miniconda3-latest-Linux-x86_64.sh  # Linux
     bash Miniconda3-latest-MacOSX-x86_64.sh  # macOS
     ```
  4. Follow the installation prompts.
  5. Restart your terminal.

To confirm Miniconda is installed, run:
```sh
conda --version
```
---

#### **Step 2: Create a Conda Environment from `environment.yml`**
Navigate to the directory where your `environment.yml` file is located. Then, create the environment using:

```sh
conda env create -f environment.yml
```

This will create a new Conda environment named **IntroAgents2** (as defined in your `environment.yml`).

---

#### **Step 3: Activate the Conda Environment**
After installation, activate your environment using:

```sh
conda activate IntroAgents2
```

If you ever need to deactivate the environment, use:

```sh
conda deactivate
```

---

#### **Step 4: Verify Installed Packages**
Once activated, check if all dependencies are correctly installed:

```sh
conda list
```

This will show all installed packages in the environment.

---

#### **Step 5: Updating the Conda Environment (If Needed)**

If you modify the `environment.yml` file (e.g., add new dependencies), update your environment with:

```sh
conda env update --file environment.yml --prune
```

The `--prune` option removes packages that are no longer listed in the `environment.yml` file.

---

#### **Step 6: Removing the Conda Environment (If Needed)**
If you want to remove the environment:

```sh
conda remove --name IntroAgents2 --all
```

---

#### **Summary of Commands**
| **Action**                          | **Command** |
|-------------------------------------|------------|
| Install Miniconda                   | Download & Install from [Miniconda](https://docs.conda.io/en/latest/miniconda.html) |
| Create an environment from `.yml`   | `conda env create -f environment.yml` |
| Activate the environment            | `conda activate IntroAgents2` |
| Deactivate the environment          | `conda deactivate` |
| List installed packages             | `conda list` |
| Update the environment              | `conda env update --file environment.yml --prune` |
| Remove the environment              | `conda remove --name IntroAgents2 --all` |
