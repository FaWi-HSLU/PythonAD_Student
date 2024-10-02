# PythonAD_Student
Python Advanced Repo for Students


# Python Environments

This repository provides an overview of three popular methods for managing Python environments. They are:

**Anaconda ``conda``**
    A comprehensive distribution of Python that includes **package and environment management tools.** Anaconda simplifies the installation of libraries and dependencies, particularly for data science and machine learning projects. **Anaconda environments are global, allowing you to create environments that can be accessed system-wide.**

**Virtual Environment``venv``**
    A built-in Python module that allows you to create lightweight, isolated Python environments. **Each environment is created in a local folder**, keeping project-specific dependencies separate from the global Python installation.

**Pip Virtual Environment ``pipenv``**
    A packaging tool that combines ``pip`` and ``venv`` into one cohesive workflow. ``Pipenv`` automatically creates and manages a **local virtual environment** for your projects, using a ``Pipfile`` to track dependencies and their versions. **Like ``venv``, Pipenv environments are also stored in local folders.**




## Explanation of Differences

| **Feature**                                | **Conda (Anaconda)**                                               | **venv**                                                   | **Pipenv**                                                |
|--------------------------------------------|--------------------------------------------------------------------|------------------------------------------------------------|------------------------------------------------------------|
| **Requirements**                           | Install **Anaconda** or **Miniconda**                              | **Python 3.x** (``venv`` is native to Python) <br>  `pyenv` recommended for managing different Python versions                   | **Python 3.6+** <br> ``pipenv`` is installed <br> `pyenv` recommended for managing different Python versions |
| **Requires Python version pre-installed**  | **No**                                                             | **Yes** (install **manually** using `pyenv`)                                                     | **YES** (but can install **automatically** if using `pyenv`)   |
| **How to install a module**                | `conda install <module_name>`                                       | `pip install <module_name>`                                 | `pipenv install <module_name>`                             |
| **How to uninstall a module**              | `conda remove <module_name>`                                        | `pip uninstall <module_name>`                               | `pipenv uninstall <module_name>`                           |
| **Creating an environment**                | `conda create -n <env_name>`                                        | `python -m venv <env_name>`                                 | `pipenv --python <python_version>` (auto creates env)      |
| **Creating an env with a specific Python version** | `conda create -n <env_name> python=<version>`                      | `python<version> -m venv <env_name>` (requires `pyenv` if specific version is not installed) | `pipenv --python <version>` (requires `pyenv` if version is not installed) |
| **Activate an environment**                | `conda activate <env_name>`                                         | `source <env_name>/bin/activate` (Linux/Mac) <br> `<env_name>\Scripts\activate` (Windows) | `pipenv shell`                                             |
| **Deactivate an environment**              | `conda deactivate`                                                  | `deactivate`                                                | `exit`                                                     |

### Summary:
- **Conda**: Automatically manages Python versions and does not require pre-installation of Python.
- **venv**: Requires Python to be pre-installed, but you can use **`pyenv`** to manage multiple Python versions.
- **Pipenv**: Uses the existing Python installation, but can work with **`pyenv`** to manage and install different Python versions automatically.
