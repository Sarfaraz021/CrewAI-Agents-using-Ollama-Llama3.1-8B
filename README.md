# CrewAI-Agents-using-Ollama-Llama3.1-8B

## Troubleshooting Installation Issues

### Error: Microsoft Visual C++ 14.0 or greater is required

#### Why This Happens
The package `chroma-hnswlib` depends on native C++ extensions, so it needs a C++ compiler to build the package. Windows systems often lack the necessary build tools by default, which causes issues during the installation of packages requiring compilation.

#### How to Fix It

**Option 1: Install Microsoft C++ Build Tools**

1. **Download and Install Build Tools:**
    - Go to [Microsoft C++ Build Tools](https://visualstudio.microsoft.com/visual-cpp-build-tools/).
    - Download the installer and run it.
2. **In the installer, select:**
    - `Desktop development with C++` workload.
    - Ensure that `MSVC v142 - VS 2019 C++ x64/x86 build tools` and `Windows 10 SDK` are selected.
3. **After installation, restart your computer.**

**Option 2: Install Precompiled Wheels (Workaround)**

You can try installing a precompiled version of `hnswlib` to avoid the need for compilation:

# Installation
**Option 3: Upgrade pip, setuptools, and wheel**

Sometimes, updating your tools can fix the issue:

```bash
pip install --upgrade pip setuptools wheel
```

**Option 4: Use the --no-build-isolation Flag**

If the issue persists, try using the following command:

```bash
pip install crewai --no-build-isolation
```

### Prerequisites

Before installing `crewai`, ensure you have Python 3.12 installed and create a virtual environment. Then, install the required libraries:

1. **Install Python 3.12:**
    - Download and install Python 3.12 from the [official website](https://www.python.org/downloads/).

2. **Create a virtual environment:**
    ```bash
    python -m venv myenv
    ```

3. **Activate the virtual environment:**
    - On Windows:
        ```bash
        myenv\Scripts\activate
        ```
    - On macOS and Linux:
        ```bash
        source myenv/bin/activate
        ```

4. **Install the required libraries:**
    ```bash
    pip install -r requirements.txt
    ```

### Installation

To install the `crewai` package, use the following command:

```bash
pip install crewai
```

To install the `crewai` package, use the following command:

```bash
pip install crewai
```
