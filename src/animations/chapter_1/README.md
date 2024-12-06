# Setting Up the Virtual Environment for Jupyter

This guide teaches you how to set up a virtual environment (`venv`) to run Jupyter Notebook with isolated dependencies.

## Steps to Set Up the Environment

### 1. Verify Python Installation

First, check if Python 3 is installed on your system. Open a terminal and type:

```bash
python3 --version
```

If you don't have Python 3 installed, download and install it from [python.org](https://www.python.org/downloads/).

### 2. Create a Virtual Environment (venv)

To create the virtual environment, navigate to your project directory and run:

```bash
python3 -m venv manim
```

This will create a directory named `manim` that will contain the virtual environment.

### 3. Activate the Virtual Environment

After creating the virtual environment, you need to activate it. The process depends on your operating system:

#### a. **On Linux or MacOS:**

```bash
source manim/bin/activate
```

#### b. **On Windows:**

```bash
.\manim\Scripts\activate
```

Once the virtual environment is activated, you'll see its name in parentheses in the command prompt, like this: `(manim)`.

### 4. Install Required Dependencies

With the virtual environment activated, you can install the necessary packages for your project. If you're using Jupyter and packages like **Manim**, install them with the following commands:

```bash
pip install jupyter
pip install manim
```

### 5. Install Jupyter Kernel for the Virtual Environment

To use the virtual environment in Jupyter, you'll need to install the Jupyter kernel for it. Run the following command:

```bash
pip install ipykernel
python -m ipykernel install --user --name=manim --display-name "Python (manim)"
```

This will allow you to select the virtual environment in Jupyter.

### 6. Start Jupyter Notebook

Now you can start Jupyter Notebook with the following command:

```bash
jupyter notebook
```

Jupyter will open in your web browser. To select the virtual environment kernel, go to **Kernel > Change Kernel** and choose "Python (manim)".

### 7. Deactivate the Virtual Environment

When you're done using the virtual environment, deactivate it with the following command:

```bash
deactivate
```
