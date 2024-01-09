# Environment & Package Info


## Virtualenv
- [Documentation](https://virtualenv.pypa.io/en/latest/index.html)

|Command|Description  |
|--|--|
| `python -m pip install --user virtualenv` | Install virtualenv via pip |
| `python -m virtualenv venv` | Create a new env called *venv* in the current direectory  |
| `.\venv\Scripts\activate` | Activate the virtual environment (**venv* here)|


## Pip Commands

| Command|Description  |
|--|--|
| `pip freeze` | Outputs all the packages used in requirements.txt |
| `pip freeze > requirements.txt` | Generates a requirements file containing all the package info |
| `pip install -r requirements.txt` | Installs all the packages in requirements.txt file |
| `pip list --outdated` | Lists all the outdated packages in the environment |
| `pip freeze \| %{$_.split('==')[0]} \| %{pip install --upgrade $_}` | Updates **ALL** the outdated packages in the system to the latest version in PyPI |
