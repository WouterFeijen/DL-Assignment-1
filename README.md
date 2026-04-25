# [2AMM10] Deep Learning - Assignment 1 

# Local Environment Setup
This project uses [`uv`](https://github.com/astral-sh/uv) to manage extremely fast, reproducible virtual environments. Our dependencies are locked to **Python 3.13** to ensure cross-platform compatibility.

## 1. Install `uv`
If you haven't already, install the `uv` package manager globally. Open your terminal or command prompt and run:
```bash
python -m pip install uv
```

## 2. Create the Virtual Environment
Navigate to this project's root directory in your terminal and create a local virtual environment. We specify Python 3.13 to match our locked requirements:
```
uv venv <PATH_TO_VENV_FOLDER>\<VENV_NAME> --python 3.13
```

*(Note: If you do not have Python 3.13 installed on your system, `uv` is smart enough to automatically download the correct background binaries for you!)*

## 3. Activate the Environment
You must activate the environment before installing packages or running the code.
**For Windows:**
```<PATH_TO_VENV_FOLDER>\<VENV_NAME>\Scripts\activate```

**For Mac/Linux:**
```source <PATH_TO_VENV_FOLDER>/<VENV_NAME>/bin/activate```

## 4. Install Dependencies
Navigate to this project's root directory in your terminal (where the `requirements.txt` file is located). With the environment active, install the exact, pre-compiled package versions:
```
uv pip install -r requirements.txt
```
(note: add "py -m" in front if path is not set for uv)

## 5. Link to Jupyter
To make this environment available inside Jupyter Notebook/Lab, register it as a kernel by running the following command while the environment is still active:
```
python -m ipykernel install --user --name=<VENV_NAME> --display-name "Python 3.13 (<VENV_NAME>)"
```


Yes, this is completely correct in terms of the technical steps! You have successfully captured the entire workflow. 

There are just a few minor formatting and cross-platform tweaks you might want to adjust to make it perfect for your team:

1. **Heading Consistency:** Your Step 1 uses an `###` heading, but Steps 2 through 5 use `##`. It looks much cleaner if they all use the same heading level.
2. **Code Block Formatting in Step 3:** In Step 3, the code backticks are on the same line as the commands, which can sometimes cause Markdown rendering issues on platforms like GitHub or GitLab. 
3. **Cross-Platform Note in Step 4:** You added the helpful note about using `py -m uv`. Since `py` is a Windows-only command, Mac/Linux teammates who run into the same PATH issue would need to use `python3 -m uv` or `python -m uv` instead. 

Here is the fully polished raw text, with consistent headings, clarified notes, and using the 4-space indentation for code blocks (to avoid the backtick glitch you mentioned earlier):

***

# [2AMM10] Deep Learning - Assignment 1 

## Local Environment Setup
This project uses [uv](https://github.com/astral-sh/uv) to manage extremely fast, reproducible virtual environments. Our dependencies are locked to **Python 3.13** to ensure cross-platform compatibility.

## 1. Install uv
If you haven't already, install the `uv` package manager globally. Open your terminal or command prompt and run:

    python -m pip install uv

## 2. Create the Virtual Environment
Navigate to this project's root directory in your terminal and create a virtual environment. We specify Python 3.13 to match our locked requirements:

    uv venv <PATH_TO_VENV_FOLDER>\<VENV_NAME> --python 3.13

*(Note: If you do not have Python 3.13 installed on your system, `uv` is smart enough to automatically download the correct background binaries for you!)*

## 3. Activate the Environment
You must activate the environment before installing packages or running the code.

**For Windows:**

    <PATH_TO_VENV_FOLDER>\<VENV_NAME>\Scripts\activate

**For Mac/Linux:**

    source <PATH_TO_VENV_FOLDER>/<VENV_NAME>/bin/activate

## 4. Install Dependencies
Navigate to this project's root directory in your terminal (where the `requirements.txt` file is located). With the environment active, install the exact, pre-compiled package versions:

    uv pip install -r requirements.txt

*(Note: If your terminal says `uv` is not recognized, add `py -m` in front of the command on Windows, or `python -m` on Mac/Linux).*

## 5. Link to Jupyter
To make this environment available inside Jupyter Notebook/Lab, register it as a kernel by running the following command while the environment is still active:

    python -m ipykernel install --user --name=<VENV_NAME> --display-name "Python 3.13 (<VENV_NAME>)"