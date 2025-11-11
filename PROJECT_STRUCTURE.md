# Project Structure

This document outlines the recommended directory structure for the Roaree Benchmark Club repository.

## 📁 Directory Organization

```
roareebenchmark/
├── .github/                    # GitHub-specific files
│   ├── ISSUE_TEMPLATE/        # Issue templates
│   └── pull_request_template.md
├── benchmarks/                 # Benchmark implementations
│   ├── benchmark_name/
│   │   ├── README.md          # Benchmark documentation
│   │   ├── data/              # Benchmark datasets
│   │   ├── scripts/           # Evaluation scripts
│   │   └── results/           # Benchmark results
│   └── ...
├── src/                       # Source code
│   ├── evaluation/            # Evaluation frameworks
│   ├── metrics/               # Metric implementations
│   ├── models/                # Model wrappers and interfaces
│   └── utils/                 # Utility functions
├── tests/                     # Unit and integration tests
│   ├── test_benchmarks/
│   ├── test_evaluation/
│   └── test_utils/
├── notebooks/                 # Jupyter notebooks for analysis
│   ├── exploratory/           # Exploratory data analysis
│   └── results/               # Results visualization
├── docs/                      # Documentation
│   ├── guides/                # How-to guides
│   ├── methodology/           # Methodology documentation
│   └── api/                   # API documentation
├── data/                      # Data directory (gitignored)
│   ├── raw/                   # Raw datasets
│   └── processed/             # Processed datasets
├── models/                    # Model storage (gitignored)
│   ├── checkpoints/           # Model checkpoints
│   └── pretrained/            # Pretrained models
├── results/                   # Results directory (gitignored)
│   ├── experiments/           # Experiment results
│   └── figures/               # Generated figures
├── configs/                   # Configuration files
│   └── experiment_configs/    # Experiment configurations
├── scripts/                   # Utility scripts
│   ├── setup/                 # Setup scripts
│   └── analysis/              # Analysis scripts
├── .gitignore                 # Git ignore rules
├── CODE_OF_CONDUCT.md         # Code of conduct
├── CONTRIBUTING.md            # Contribution guidelines
├── CONTRIBUTORS.md            # List of contributors
├── LICENSE                    # License information
├── README.md                  # Main readme
├── SECURITY.md                # Security policy
├── requirements.txt           # Python dependencies
├── setup.py                   # Package setup
└── pyproject.toml            # Modern Python project config
```

## 📂 Directory Purposes

### `/benchmarks/`
Contains individual benchmark implementations. Each benchmark should have its own subdirectory with:
- `README.md`: Description, methodology, and usage
- `data/`: Dataset or data loading scripts
- `scripts/`: Evaluation and analysis scripts
- `results/`: Benchmark results and leaderboards

### `/src/`
Core source code for the project:
- `evaluation/`: Framework for running evaluations
- `metrics/`: Custom metric implementations
- `models/`: Model wrappers for different LLM APIs
- `utils/`: Shared utility functions

### `/tests/`
Test suite following the structure of `/src/`:
- Unit tests for all source modules
- Integration tests for benchmarks
- Test fixtures and utilities

### `/notebooks/`
Jupyter notebooks for analysis and visualization:
- `exploratory/`: Data exploration and initial analyses
- `results/`: Results visualization and reporting

### `/docs/`
Project documentation:
- `guides/`: Tutorials and how-to guides
- `methodology/`: Detailed methodology documentation
- `api/`: API reference documentation

### `/data/` (gitignored)
Data storage (not committed to repository):
- `raw/`: Original datasets
- `processed/`: Cleaned and processed datasets
- Store large datasets externally (e.g., Google Drive, S3)

### `/models/` (gitignored)
Model storage (not committed to repository):
- `checkpoints/`: Model checkpoints
- `pretrained/`: Downloaded pretrained models
- Store large models externally

### `/results/` (gitignored)
Experiment results (not committed to repository):
- `experiments/`: Individual experiment outputs
- `figures/`: Generated visualizations
- Summary results can be committed in `/benchmarks/*/results/`

### `/configs/`
Configuration files:
- Experiment configurations (YAML/JSON)
- Model configurations
- Evaluation settings

### `/scripts/`
Standalone scripts:
- `setup/`: Environment setup and installation
- `analysis/`: Data analysis and processing

## 📝 File Naming Conventions

### Python Files
- Use `snake_case` for file names
- Test files: `test_*.py`
- Use descriptive names: `evaluate_benchmark.py` not `eval.py`

### Notebooks
- Use descriptive names with dates: `2025-11-11_initial_analysis.ipynb`
- Prefix with number for ordering: `01_data_exploration.ipynb`

### Configuration Files
- Use clear, descriptive names
- Include purpose: `bert_evaluation_config.yaml`

### Data Files
- Include version or date: `dataset_v1.csv`
- Document data sources in README

## 🔧 Configuration Files

### `requirements.txt`
Pin major versions, allow minor updates:
```
torch>=2.0.0,<3.0.0
transformers>=4.30.0,<5.0.0
```

### `pyproject.toml`
Modern Python project configuration (recommended):
- Package metadata
- Build system requirements
- Tool configurations (black, pytest, mypy)

### `setup.py`
For package installation and distribution

## 📊 Data Management

### Large Files
- **Do not commit** files larger than 10MB
- Use Git LFS for files between 10MB-100MB
- Store files >100MB externally
- Document external storage locations

### Datasets
- Keep raw data immutable
- Document preprocessing steps
- Version processed datasets
- Include data licenses and citations

## 🧪 Testing Organization

- Mirror the structure of `/src/` in `/tests/`
- One test file per source file
- Use fixtures for common setup
- Include integration tests for benchmarks

## 📚 Documentation Standards

### Code Documentation
- Docstrings for all public functions/classes
- Type hints for function signatures
- Inline comments for complex logic

### README Files
- Every major directory should have a README
- Include purpose, usage, and examples
- Link to related documentation

## 🔄 Version Control

### Branches
- `main`: Stable, production-ready code
- `develop`: Integration branch for features
- `feature/*`: Individual feature branches
- `hotfix/*`: Critical bug fixes

### Commits
- Use clear, descriptive commit messages
- Reference issues: `Fixes #123`
- Group related changes

## 🚀 Getting Started

New members should:
1. Clone the repository
2. Create a virtual environment
3. Install dependencies: `pip install -r requirements.txt`
4. Run tests: `pytest tests/`
5. Read benchmark READMEs to understand existing work

## ❓ Questions?

- Check the documentation in `/docs/`
- Ask in team discussions
- Contact core team members

---

*This structure is a recommendation and may evolve as the project grows.*

*Roar, Lions, Roar! 🦁*
