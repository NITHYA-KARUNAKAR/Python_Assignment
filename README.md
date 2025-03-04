# Python_Assignment
IU_Python_Assignment_Code

# Python Project

## Description
This project implements a Python-based solution to process training data, find the best ideal functions, map test data, and store the results in an SQLite database. The program follows a structured workflow to ensure accuracy and efficiency in function selection and test data mapping.

## How This Code Meets the Assignment Requirements
The implementation meets all the assignment requirements as follows:

1. **Object-Oriented Design**
   - The project is structured using **classes** for different functionalities:
     - `DatasetHandler` (Base class for data handling)
     - `TrainingData`, `IdealFunctions`, `TestData` (Derived from `DatasetHandler`)
     - `DataMapping` (Handles function selection and test data mapping)
     - `DatabaseHandler` (Manages database operations)
     - `Visualizer` (Handles visualization)
   - This ensures modularity and **object-oriented programming (OOP)** principles.

2. **Inheritance**
   - The `TrainingData`, `IdealFunctions`, and `TestData` classes **inherit** from `DatasetHandler`, demonstrating **class inheritance**.

3. **Exception Handling**
   - The code includes **both standard and user-defined exceptions**:
     - It handles **file loading errors** (e.g., `FileNotFoundError`, `pd.errors.EmptyDataError`, `pd.errors.ParserError`).
     - It includes exception handling in **data processing** (`KeyError`, `IndexError`).
     - Custom messages and structured logging are used.

4. **Use of Pandas, Bokeh, and SQLAlchemy**
   - `Pandas`: Used for **data processing** (loading CSV, manipulating DataFrames).  
   - `Bokeh`: Used for **data visualization** (plotting training, ideal, and test data).  
   - `SQLAlchemy`: Used to **store and manage** the dataset in an **SQLite database**.

5. **Unit Testing**
   - The project includes **unit tests** for:
     - **Loading data** (`test_load_data`)
     - **Selecting ideal functions** (`test_select_best_ideal_functions`)
     - **Mapping test data** (`test_map_test_data`)

6. **Documentation and Docstrings**
   - **Each class and method has a proper docstring**, explaining:
     - Purpose
     - Attributes
     - Input and output details
   - The README also clearly describes **what the code does** and how it meets the assignment requirements.

7. **How Data is Processed**
   - The program reads four training datasets (A) and one test dataset (B) from CSV files.
   - It also reads 50 ideal functions (C) from another dataset.
   - The **Least Squares Method** is applied to select the best four ideal functions.
   - The test dataset is evaluated against these functions based on a **threshold condition (√2 max deviation rule)**.
   - The results are stored in an SQLite database.
   - The processed data and mappings are visualized using **Bokeh**.

---

## Installation
### Prerequisites
Ensure you have the following installed on your system:
- Python 3.x
- Git
- Required dependencies (listed in `requirements.txt`)

### Clone the Repository
```bash
git clone https://github.com/NITHYA-KARUNAKAR/Python_Assignment.git
cd Python_Assignment
```

### Create a Virtual Environment (Optional but Recommended)
```bash
python -m venv venv
source venv/bin/activate  # macOS/Linux
venv\Scripts\activate  # Windows
```

### Install Dependencies
```bash
pip install -r requirements.txt
```

---

## Usage
To run the project:
```bash
python main.py
```

For specific functionalities, use:
```bash
python script.py --option
```

Example:
```bash
python script.py --help
```

---

## Git Workflow (as per Assignment Requirements)

### Clone the Repository and Work on the Develop Branch
```bash
git clone https://github.com/NITHYA-KARUNAKAR/Python_Assignment.git
cd Python_Assignment
git checkout develop
git pull origin develop
git checkout -b feature-new-function
```

### Making Changes and Committing
```bash
git add .
git commit -m "Added a new function to improve feature XYZ"
```

### Pushing and Creating a Pull Request
```bash
git push origin feature-new-function
```
1. Go to the repository on GitHub.
2. Create a Pull Request (PR) against the `develop` branch.
3. Request a review and wait for approval.

### Merging and Cleaning Up
```bash
git checkout develop
git pull origin develop
git branch -d feature-new-function
git push origin --delete feature-new-function
```

### Additional Git Commands as Required by the Assignment
#### Basic Git Configurations
```bash
git config --global user.email "your-email@example.com"
git config --global user.name "Your Name"
```

#### Creating and Managing Branches
```bash
git branch develop
git checkout -b develop
git push origin develop
git branch --set-upstream-to=origin/develop
```

#### Checking Branch Information
```bash
git branch -a  # List all branches
git branch -r  # Check remote branches only
git branch  # Check current branch
git status  # Show working directory status
```

#### Handling Outdated Branch During Push
```bash
git pull origin develop --rebase
```

The above **Git workflow**  ensures the correct **cloning, developing, committing, pushing, and merging process** 

---

## Contact
For questions or suggestions, reach out to me at:
- Email: nithyakarunakara@gmail.com
- GitHub: https://github.com/NITHYA-KARUNAKAR

