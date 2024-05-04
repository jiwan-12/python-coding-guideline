## Project and Python environment setup guidelines
   # Most use python3.7 or lastest stable version (python3.12)

## Please follow the following project structure for the new project
    project_name/
    │
    ├── docs/                   # Documentation files (optional)
    │
    ├── src/                    # Source code
    │   ├── package1/           # Package 1
    │   │   ├── __init__.py
    │   │   ├── module1.py
    │   │   └── module2.py
    │   │
    │   ├── package2/           # Package 2
    │   │   ├── __init__.py
    │   │   ├── module3.py
    │   │   └── module4.py
    │   │
    │   └── __init__.py         # Initialization file for the src directory
    |   |__ constant.py         # List of the constants needed for the application
    |   |__ main.py             # Entry point of the application
    │
    ├── tests/                  # Test cases
    |   |
    |   |__ test_data           # Folder that consist the data for test
    |   |
    │   ├── test_package1/
    │   │   ├── __init__.py
    │   │   └── test_module1.py
    │   │
    │   ├── test_package2/
    │   │   ├── __init__.py
    │   │   └── test_module3.py
    │   │
    │   └── __init__.py         # Initialization file for the tests directory
    │
    ├── config.json             # Configuration file
    ├── requirements.txt        # Dependencies file
    ├── README.md               # Project readme file
    ├── LICENSE                 # Project license file
    └── .gitignore              # Git ignore file

## Strictly follow the python pep8 styling
   # Recommanded: Use line lenght of 100 chars instead of 79
   # VS code setup for the autopep8
     # Install the VS code extension autopep8 and configure as the default formater
     # Go to the extension settings(autopep8 extension) and add argument
      `--max-line-length=100`

## Recommanded packages list
   # pylint # for liniting
   # isort # to sort header
   # autopep8 # for commandline fromating (optional)
   # coverage # to see the test coverage

   # Add following list on the requirements.txt and run
    `pip install -r requirements.txt`
    

## pylint Setup
   # If you are using pylint python virtual environment then please create pylint config file and add the following line
        # To generate pylint config
         `pylint --generate-rcfile > .pylintrc`
        # Update following line in .pylintrc
         `init-hook='import sys; sys.path.append(".")'`

## Run the application
    `python3 src/main.py`

## Run all unit tests (unittests from tests folder)
    `python -m unittest discover -s tests -p "test_*.py"`

## Use isort package to sort the imports
    `isort` <file_name>

## Use pylint package for the linting
    `pylint <file_name>` or
    `pylint <dir_name>`

## Test Coverage
    # Use `coverage` package to generate the test coverage report
        `coverage run -m unittest discover -s tests -p "test_*.py"`
    # Get the coverage result
        `coverage report`

## Optional settings

