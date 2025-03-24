# Contributing to objdetect

Thank you for considering contributing to the objdetect library! This document outlines the process for contributing to the project and how to set up your development environment.

## Development Environment

This project uses [nbdev](https://nbdev.fast.ai/) for development. All code is written in Jupyter notebooks and then exported to Python modules.

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/HasanGoni/2025-object-detection.git
   cd 2025-object-detection
   ```

2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install the package and development dependencies:
   ```bash
   pip install -e ".[dev]"
   ```

4. Install nbdev:
   ```bash
   pip install nbdev
   ```

5. Set up git hooks:
   ```bash
   nbdev_install_hooks
   ```

## Development Workflow

1. Create a new branch for your feature or bug fix:
   ```bash
   git checkout dev
   git pull
   git checkout -b feature/your-feature-name
   ```

2. Make your changes in the Jupyter notebooks in the `nbs/` directory.

3. Build the library to export the notebooks to Python modules:
   ```bash
   nbdev_build_lib
   ```

4. Run the tests:
   ```bash
   nbdev_test
   ```

5. Build the documentation:
   ```bash
   nbdev_build_docs
   ```

6. Commit your changes with clear, descriptive commit messages:
   ```bash
   git add .
   git commit -m "Add feature: brief description"
   ```

7. Push your branch to GitHub:
   ```bash
   git push -u origin feature/your-feature-name
   ```

8. Create a pull request to the `dev` branch.

## Code Style

- Follow PEP 8 guidelines
- Write docstrings for all functions, classes, and methods
- Include type hints for parameters and return values
- Write tests for new functionality

## Adding New Features

1. **New models**: Add new notebooks in the `nbs/` directory with the model implementation
2. **Data support**: Extend the dataset classes to support new datasets
3. **Utilities**: Add new utility functions to appropriate notebooks

## Updating Documentation

- Update the notebooks with clear explanations and examples
- Run `nbdev_build_docs` to update the documentation site
- Make sure all public functions have proper docstrings

## Updating the Changelog

When making changes, add an entry to the "Unreleased" section in CHANGELOG.md following the Keep a Changelog format.

## Pull Request Process

1. Update the README.md and documentation with details of changes
2. Update the CHANGELOG.md with details of changes
3. Ensure all tests pass and documentation builds correctly
4. The PR will be merged once it receives approval from the maintainers

## Questions or Issues?

If you have questions or issues, please create an issue on GitHub.

Thank you for contributing to objdetect!