# Python Lab Project — Assignment Worksheet


## Part A — Project Setup Using the CLI

### Command Explanation

I created the `python_lab` project directory and moved into it using `mkdir` and `cd`. I then created the `src`, `tests`, and `docs` subdirectories using `mkdir`. Inside `src`, I created the Python files `main.py`, `utils.py`, and `config.py`. Inside `docs`, I created `README.md` and used output redirection to write `My Python Lab Project` into it. Finally, I displayed the full directory tree recursively to verify that the folders and files were correctly created and nested.

### Project Structure

Separating code into `src`, `tests`, and `docs` is good practice because each directory has a clear purpose. The `src` directory contains the application's source code, `tests` provides a dedicated location for testing code, and `docs` contains project documentation. This separation keeps the project organized, makes files easier to locate and maintain, and provides a structure that can scale as the project becomes larger.

### Evidence

The recursive directory listing screenshot is included in the `docs/screenshots/` directory.

---

## Part B — Git Initialization and First Commit

### `.gitignore`

The `.gitignore` file tells Git which files and directories should not be tracked in the repository. The project uses entries to ignore Python compiled cache folders, compiled `.pyc` files, and `.env` files. Ignoring `__pycache__` directories and `.pyc` files prevents generated Python bytecode from being committed because these files are automatically generated and are not part of the source code. Ignoring `.env` files is important because they can contain environment-specific configuration and sensitive information such as credentials or API keys.

### Commit History

The Git commit history records the sequence of changes made to the project over time. It shows information such as commit identifiers, commit messages, authorship, and the order in which changes were recorded. This provides a history of the project's development and makes it possible to understand when and how changes were introduced.

### Evidence

The screenshot showing the first commit and commit message is included in the `docs/screenshots/` directory.

---

## Part C — Writing and Committing Python Code

### `utils.py`

```python
def square(n):
    return n * n


def is_even(n):
    return n % 2 == 0


def celsius_to_fahrenheit(c):
    return (c * 9 / 5) + 32


def greet(name):
    return f"Hello, {name}! Welcome to my Python Lab Project."
```

### `main.py`

```python
from utils import square, is_even, celsius_to_fahrenheit, greet


number = float(input("Enter a number: "))

print("Square:", square(number))

if is_even(number):
    print("The number is even")
else:
    print("The number is odd")

print("Fahrenheit equivalent:", celsius_to_fahrenheit(number))

name = input("Enter your name: ")
print(greet(name))
```

### Python Import Explanation

Python's import system allows code in one module to be reused by another module. In this project, `utils.py` contains the reusable functions while `main.py` imports those functions using `from utils import square, is_even, celsius_to_fahrenheit, greet`. This allows `main.py` to call the functions without defining their implementations again, keeping the program organized and reducing duplicated code.

### Testing

The program was tested with three different input values.

#### Test 1 — Input: 5

```text
Enter a number: 5
Square: 25.0
The number is odd
Fahrenheit equivalent: 41.0
Enter your name: Morgan
Hello, Morgan! Welcome to my Python Lab Project.
```

#### Test 2 — Input: 8

```text
Enter a number: 8
Square: 64.0
The number is even
Fahrenheit equivalent: 46.4
Enter your name: Alex
Hello, Alex! Welcome to my Python Lab Project.
```

#### Test 3 — Input: -3

```text
Enter a number: -3
Square: 9.0
The number is odd
Fahrenheit equivalent: 26.6
Enter your name: Jane
Hello, Jane! Welcome to my Python Lab Project.
```

The three tests confirm that the program correctly calculates the square, identifies whether the number is even or odd, converts the number from Celsius to Fahrenheit, and produces the personalized greeting.

---

## Part D — Publishing to GitHub and Branch Workflow

### Branches and Pull Requests

Developers use branches to isolate new work from the stable `main` branch. This allows changes to be developed and tested without directly affecting the main codebase. Pull requests provide a controlled process for proposing changes before they are merged into `main`. During a code review, reviewers examine the proposed changes, check whether the implementation meets the project requirements, identify bugs or potential problems, suggest improvements, and verify that the changes are appropriate before approving the pull request for merging.

### Feature Branch

The greeting functionality was developed on the `feature/add-greeting` branch. The `greet(name)` function was added to `utils.py` and then imported and called from `main.py`.

### Evidence

The screenshot showing the GitHub repository, files and commit history is included in the `docs/screenshots/` directory.

The screenshot showing the open pull request from `feature/add-greeting` into `main` is included in the `docs/screenshots/` directory.

