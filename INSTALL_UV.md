# Installation Guide with UV

## Setup Instructions

### 1. Create a Virtual Environment

```bash
# Create a new virtual environment
uv venv

# Activate the environment
source .venv/bin/activate  # On Linux/macOS
# or
.venv\Scripts\activate     # On Windows
```

### 2. Install Dependencies

```bash
# Install all packages from requirements_uv.txt
uv pip install -r requirements_uv.txt

# Install llama_cpp_python separately (requires special build configuration)
uv pip install "llama_cpp_python>=0.2.78" --config-settings="cmake.args=-DLLAMA_BLAS=ON"
```

### 3. Verify Installation

```bash
# Launch Jupyter Lab to start working with the notebooks
uv run jupyter lab
```

## Quick Start (One Command)

```bash
# Create venv, install dependencies, and launch Jupyter Lab
uv venv && source .venv/bin/activate && \
uv pip install -r requirements_uv.txt && \
uv pip install "llama_cpp_python>=0.2.78" --config-settings="cmake.args=-DLLAMA_BLAS=ON" && \
uv run jupyter lab
```
