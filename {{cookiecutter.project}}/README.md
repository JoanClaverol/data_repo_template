# readme of {{cookiecutter.project}}

This package was made by {{cookiecutter.author}}.

Sure, let's break it down step by step and include it in a detailed section for your `README.md`.

## Setting Up Python Version in `pyproject.toml`

To ensure consistency in the Python environment for our project, follow these steps:

#### Step 1: Check the Python Version

Open your terminal and run the following command to check the Python version:

```bash
python --version
```

or

```bash
python3 --version
```

Example output:

```
Python 3.8.10
```

#### Step 2: Initialize Poetry in Your Project

If you haven't already set up Poetry for your project, you'll need to do so. Poetry is a dependency management tool for Python that helps you manage your project dependencies in a reproducible manner.

First, ensure Poetry is installed:

```bash
curl -sSL https://install.python-poetry.org | python3 -
```

or

```bash
pip install poetry
```

Navigate to your project directory:

```bash
cd /path/to/your/project
```

Initialize a new Poetry project:

```bash
poetry init
```

Follow the prompts to set up your project. This command will create a `pyproject.toml` file in your project directory.

#### Step 3: Specify the Python Version in `pyproject.toml`

Open the `pyproject.toml` file created by Poetry in a text editor. Add the Python version under the `[tool.poetry.dependencies]` section. For example, if you're using Python 3.8:

```toml
[tool.poetry.dependencies]
python = "^3.8"
# other dependencies
```

Alternatively, you can set the Python version using a Poetry command:

```bash
poetry env use python3.8
```

This command updates the `pyproject.toml` file to specify Python 3.8 as the required version.

#### Step 4: Add Dependencies Using Poetry

To add dependencies to your project, use the `poetry add` command followed by the package name. For example, to add the `requests` package:

```bash
poetry add requests
```

This command updates the `pyproject.toml` file and installs the `requests` package in your project's environment.

To add a development dependency, use the `--dev` flag:

```bash
poetry add --dev pytest
```

#### Step 5: Verify Your Setup

To check the installed packages and their versions, use the following command:

```bash
poetry show
```

This command lists all the dependencies and their respective versions installed in your project.

### Conclusion

By following these steps, you can ensure that your project uses a consistent Python version and manage your dependencies effectively with Poetry. This setup helps maintain compatibility and reproducibility across different environments.
