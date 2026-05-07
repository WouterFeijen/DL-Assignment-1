# [2AMM10] Deep Learning - Assignment 1 

## Local Environment Setup
This project uses [uv](https://github.com/astral-sh/uv) to manage extremely fast, reproducible virtual environments. Our dependencies are locked to **Python 3.13** to ensure cross-platform compatibility.

### 1. Install uv
If you haven't already, install the `uv` package manager globally. Open your terminal or command prompt and run:

    python -m pip install uv

### 2. Create the Virtual Environment
Navigate to this project's root directory in your terminal and create a virtual environment. We specify Python 3.13 to match our locked requirements:

    uv venv <PATH_TO_VENV_FOLDER>\<VENV_NAME> --python 3.13

*(Note: If you do not have Python 3.13 installed on your system, `uv` is smart enough to automatically download the correct background binaries for you!)*

### 3. Activate the Environment
You must activate the environment before installing packages or running the code.

**For Windows:**

    <PATH_TO_VENV_FOLDER>\<VENV_NAME>\Scripts\activate

**For Mac/Linux:**

    source <PATH_TO_VENV_FOLDER>/<VENV_NAME>/bin/activate

### 4. Install Dependencies
Navigate to this project's root directory in your terminal (where the `requirements.txt` file is located). With the environment active, install the exact, pre-compiled package versions:

    uv pip install -r requirements.txt

*(Note: If your terminal says `uv` is not recognized, add `py -m` in front of the command on Windows, or `python -m` on Mac/Linux).*

**⚠️ Hardware Note (Important):** This environment is explicitly configured to use PyTorch **Nightly** builds with **CUDA 13.2**. 
Because half our team is using RTX 50-series (Blackwell) laptops, the stable PyTorch releases do not yet support our hardware. The `requirements.txt` will automatically pull these specialized nightly versions, which are fully backward-compatible with older cards (like the RTX 3090 or Ada generation GPUs).

### 5. Link to Jupyter
To make this environment available inside Jupyter Notebook/Lab, register it as a kernel by running the following command while the environment is still active:

    python -m ipykernel install --user --name=<VENV_NAME> --display-name "Python 3.13 (<VENV_NAME>)"