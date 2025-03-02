# Data-eyes - Developer Guide

This document is intended for developers who want to contribute to the Data-eyes project. For a general overview of the project, please see the [main README](../CHANGELOG.md).

## Development Environment

### Requirements

- Python 3.10+
- Git
- Poetry 1.5+
- A code editor (VS Code recommended)

### Initial Setup

1. Clone the repository and navigate to the project directory:
   ```bash
   git clone https://github.com/Hugues-DTANKOUO/data-eyes.git
   cd data-eyes
   ```

2. Install dependencies with Poetry:
   ```bash
   poetry install
   ```

3. Activate the virtual environment:
   ```bash
   poetry shell
   ```

## Project Structure

The structure presented below is preliminary and will evolve with the development of the project:

```
data-eyes/
├── src/                # Source code
│   └── data_eyes/      # Main module
│       ├── interface.py    # FastAPI entry point
│       ├── processors/     # Data format processors
│       ├── static/         # Static files (CSS, JS)
│       └── templates/      # Jinja2 templates
├── tests/              # Automated tests
├── docs/               # Documentation
│   └── architecture.md     # Architecture documentation
└── README.md
```

## VS Code Development Environment

If you use VS Code, here is the recommended configuration for this project. Create a `.vscode` folder and add a `settings.json` file with the following content:

```json
{
    "python.linting.enabled": true,
    "python.linting.ruffEnabled": true,
    "editor.formatOnSave": true,
    "python.formatting.provider": "ruff",
    "python.testing.pytestEnabled": true,
    "plantuml.server": "http://www.plantuml.com/plantuml",
    "[python]": {
        "editor.defaultFormatter": "charliermarsh.ruff",
        "editor.formatOnSave": true,
        "editor.codeActionsOnSave": {
            "source.organizeImports": true,
            "source.fixAll": true
        }
    }
}
```

## Development Scripts

This project will include several utility scripts to facilitate development:

```bash
# Start the development server
poetry run server

# Run tests
poetry run tests

# Run linting and type checking
poetry run lint

# Run all checks (lint + tests)
poetry run check
```

## Development Workflow

1. **Create a feature branch**:
   ```bash
   git checkout -b feature/feature-name
   ```

2. **Develop and test locally**:
   ```bash
   # Start the server to see changes
   poetry run server
   
   # Verify that tests pass
   poetry run tests
   ```

3. **Commit changes**:
   ```bash
   git add .
   git commit -m "Clear description of changes"
   ```

4. **Push the branch**:
   ```bash
   git push origin feature/feature-name
   ```

5. **Create a Pull Request** on GitHub.

## Planned API Endpoints

Here are the main endpoints planned for the API:

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/` | Home page |
| GET | `/upload` | Upload page |
| GET | `/schema` | Schema generation page |
| POST | `/api/data/upload` | File upload |
| GET | `/api/data/preview` | Data preview |
| POST | `/api/schema/generate` | SQL schema generation |
| GET | `/api/schema/export` | Schema export |

## Code Standards

### Code Style

- Follow PEP 8 for Python style
- Use type annotations for all functions
- Document all classes and methods with docstrings
- Name variables and functions in snake_case
- Name classes in PascalCase

### Docstrings

Use the following format for docstrings:

```python
def function_name(param1: str, param2: int) -> bool:
    """
    Clear description of what the function does.

    :param param1: Description of the first parameter
    :param param2: Description of the second parameter
    :return: Description of the return value
    """
```

### Tests

- All modules should have associated tests
- Use pytest for testing
- Name test files with the prefix `test_`

## Architectural Principles

- **Modularity**: Separate responsibilities into distinct modules
- **Extensibility**: Allow easy addition of new formats and features
- **Clear Interface**: Define precise interfaces between components
- **Unit Tests**: Cover code with automated tests
- **Documentation**: Document APIs and features

## Development Resources

- [FastAPI Documentation](https://fastapi.tiangolo.com/)
- [Jinja2 Documentation](https://jinja.palletsprojects.com/)
- [Poetry Documentation](https://python-poetry.org/docs/)
- [Python Type Guide](https://mypy.readthedocs.io/en/stable/cheat_sheet_py3.html)

---

For any additional questions, please feel free to open an issue on GitHub or contact @Hugues-DTANKOUO.