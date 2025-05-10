# Git Project Template with Virtual Environment and LSTM Support

This repository provides a structured template for Python projects that utilize virtual environments and potentially include LSTM (Long Short-Term Memory) neural network components. The project is configured with proper Git version control settings to maintain a clean and efficient development environment.

The repository is set up with specific Git ignore patterns to exclude virtual environment files and LSTM-related directories, ensuring that only essential source code and project files are tracked in version control. This setup is particularly useful for machine learning projects where separating environment dependencies and model artifacts from source code is crucial.

## Repository Structure
```
.
├── .gitignore          # Git ignore configuration file for excluding virtual environment and LSTM directories
└── README.md           # Project documentation and setup instructions
```

## Usage Instructions
### Prerequisites
- Git (version 2.0 or higher)
- Python (version 3.6 or higher recommended)
- pip (Python package installer)

### Installation
1. Clone the repository:
```bash
git clone https://github.com/DarshanCHMSR/lstm.git
cd lstm
```

2. Create a virtual environment:
```bash
# On MacOS/Linux
python3 -m venv lstm

# On Windows
python -m venv lstm
```

3. Activate the virtual environment:
```bash
# On MacOS/Linux
source lstm/bin/activate

# On Windows
lstm\Scripts\activate
```

### Quick Start
1. After activating the virtual environment, you can start adding your project files
2. The `.gitignore` file will automatically exclude:
   - The `lstm/` virtual environment directory
   - The `lstm/` directory for LSTM-related files

### Troubleshooting
#### Virtual Environment Issues
- If you see `command not found: python3`:
  1. Ensure Python is installed on your system
  2. Verify Python installation:
  ```bash
  python --version
  # or
  python3 --version
  ```

- If virtual environment activation fails:
  1. Delete the existing virtual environment:
  ```bash
  rm -rf myenv  # On MacOS/Linux
  rmdir /s /q myenv  # On Windows
  ```
  2. Recreate the virtual environment following the installation steps

#### Git Issues
- If files in `myenv/` or `lstm/` are being tracked despite `.gitignore`:
  1. Clear Git cache:
  ```bash
  git rm -r --cached .
  git add .
  git commit -m "Remove ignored files"
  ```

## Data Flow
The repository manages project files and dependencies through a straightforward workflow.

```ascii
[Source Code] -----> [Git Tracking]
     ^
     |
[Excluded by .gitignore]
  - myenv/
  - lstm/
```

Key interactions:
- Git tracks all files except those specified in `.gitignore`
- Virtual environment (`myenv/`) maintains isolated Python dependencies
- LSTM directory (`lstm/`) can store model files and related artifacts
- Source code and configuration files are version controlled
- Dependencies are managed separately through requirements.txt (when added)

