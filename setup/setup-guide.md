# Setup Guide

This guide will walk you through setting up your Python data science environment using UV.

## What is UV?

UV is a fast Python package installer and resolver written in Rust. It's a modern alternative to pip that offers:
- **Speed**: 10-100x faster than pip
- **Reliability**: Better dependency resolution
- **Simplicity**: Easy virtual environment management
- **Compatibility**: Works with existing Python tools

## Prerequisites

- **Python 3.10 or higher**: Check your version with `python --version`
- **Terminal/Command Prompt**: PowerShell (Windows), Terminal (macOS/Linux)

## Step 1: Install UV

### Windows (PowerShell)

Open PowerShell and run:

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

### macOS/Linux

Open Terminal and run:

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

> **Important:** After installing UV, **restart your IDE (e.g., VS Code)** before continuing. UV updates your system PATH, but your IDE won't see it until it restarts. Without this step, UV commands will not be available inside the IDE.

### Verify Installation

```bash
uv --version
```

You should see something like `uv 0.x.x`.

## Step 2: Clone the Repository

```bash
# Navigate to where you want the project
cd ~/Documents  # or wherever you prefer

# Clone the repository
git clone <repo-url>
cd FIFA 2026 World Cup Project
```

## Step 3: Create Virtual Environment

A virtual environment keeps your project dependencies isolated from other Python projects.

```bash
uv venv
```

This creates a `.venv` folder in your project directory.

## Step 4: Activate Virtual Environment

### Windows (PowerShell)

```powershell
.venv\Scripts\activate
```

### macOS/Linux

```bash
source .venv/bin/activate
```

You should see `(.venv)` appear in your terminal prompt.

## Step 5: Install Dependencies

With your virtual environment activated:

```bash
uv sync --link-mode=copy
```

This installs all required packages listed in `pyproject.toml`:
- pandas (data manipulation)
- numpy (numerical computing)
- plotly (interactive plotting)
- seaborn (statistical visualization)
- jupyter (notebook interface)
- ipykernel (Jupyter kernel)
- scikit-learn (machine learning)

## Step 6: Set Up Jupyter Kernel

Make sure Jupyter can find your virtual environment:

```bash
python -m ipykernel install --user --name=data-science-fundamentals
```

## Step 7: Open Jupyter Notebooks

### Option 1: VS Code (Recommended)

1. Open VS Code
2. Install the "Jupyter" extension (if not already installed)
3. Open the project folder
4. Navigate to `notebooks/00_test_setup.ipynb`
5. Click "Select Kernel" in the top right
6. Choose `.venv` or "data-science-fundamentals"

### Option 2: Jupyter Lab

```bash
jupyter lab
```

Then navigate to `notebooks/00_test_setup.ipynb` in the browser.

## Step 8: Test Your Setup

Run all cells in `notebooks/00_test_setup.ipynb`. If everything is green ✅, you're all set!

## Common Issues & Solutions

### "uv: command not found"

**Problem**: UV not in your PATH, or your IDE hasn't picked up the updated PATH since UV was installed.

**Solution**:
- Close and reopen your terminal
- **Restart your IDE (e.g., VS Code)** — this is required after installing UV so the IDE can detect it on your PATH
- On Windows, restart PowerShell as Administrator
- Manually add UV to PATH (see UV documentation)

### "No module named 'pandas'"

**Problem**: Packages not installed or wrong environment

**Solution**:
```bash
# Make sure virtual environment is activated
# You should see (.venv) in your prompt

# Reinstall dependencies
uv sync --link-mode=copy
```

### "Kernel not found" in Jupyter

**Problem**: Jupyter doesn't see your virtual environment

**Solution**:
```bash
python -m ipykernel install --user --name=data-science-fundamentals
```

Then restart VS Code or Jupyter and select the correct kernel.

### Import errors after installation

**Problem**: Using wrong Python interpreter

**Solution** (VS Code):
1. Press `Ctrl+Shift+P` (Windows/Linux) or `Cmd+Shift+P` (macOS)
2. Type "Python: Select Interpreter"
3. Choose the one from `.venv` folder

### UV installation fails

**Problem**: Permissions or network issues

**Solution**:
- Run terminal as Administrator (Windows)
- Use `sudo` if needed (macOS/Linux)
- Check your internet connection
- Try manual installation from [UV releases](https://github.com/astral-sh/uv/releases)

## Managing Packages with UV

### Add a new package

1. Add the package to the `dependencies` list in `pyproject.toml`:

```toml
dependencies = [
    "pandas>=2.2.0",
    "your-new-package>=1.0.0",
]
```

2. Sync to install the updated dependencies:

```bash
uv sync --link-mode=copy
```

### List installed packages

```bash
uv pip list
```

### Freeze dependencies

```bash
uv pip freeze > requirements.txt
```

## Deactivating Virtual Environment

When you're done working:

```bash
deactivate
```

## Starting a New Session

Every time you return to work on this project:

1. Navigate to project directory
2. Activate virtual environment (`.venv\Scripts\activate` or `source .venv/bin/activate`)
3. Start coding!

## Additional Resources

- [UV Documentation](https://docs.astral.sh/uv/)
- [Python Virtual Environments Guide](https://docs.python.org/3/tutorial/venv.html)
- [Jupyter Notebook Documentation](https://jupyter-notebook.readthedocs.io/)

---

**Need help?** Ask your instructor during the session!
