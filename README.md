# URM Simulator

A simple desktop application to simulate and execute programs written in the Unlimited Register Machine (URM) language.

![URM Simulator](docs/img/urm_simulator.png)

*Execution trace of `Z(1); S(1); J(1,1,3)` — an infinite loop stopped by the max-iterations guard.*

## Prerequisites

- Python 3.10+
- [uv](https://github.com/astral-sh/uv) (for managing dependencies and building the project)

## Building from Source

Follow these steps to build the executable from the source code.

**1. Install `uv`**

`uv` is used for a fast and modern Python packaging workflow.

- **macOS (using Homebrew):**
  ```sh
  brew install uv
  ```

- **Linux, macOS (using the official installer):**
  ```sh
  curl -LsSf https://astral.sh/uv/install.sh | sh
  ```

**2. Set up the Environment**

Clone the repository and navigate into the project directory. Then, use `uv` to create a virtual environment and install the required dependencies.

```sh
# Create the virtual environment in a .venv folder
uv venv

# Install the project dependencies (including PyInstaller)
uv pip install -e .
```

**3. Build the Executable**

Once the dependencies are installed, you can build the executable using the `PyInstaller` command from the project's virtual environment.

```sh
# Run PyInstaller
./.venv/bin/pyinstaller --name URM_Machine --onefile --windowed main.py
```

The final executable will be located in the `dist/` directory.
