# Python Assignment - Branch Version

## Brief Overview

This project implements a Python-based approach to analyze training data, identify the best ideal functions using the Least Squares Method, and map test data to these functions based on a predefined threshold. The processed data is stored in an SQLite database, and the results are visualized for better understanding.

### Key Functionalities:

1. **Loading Data**: The program reads training, ideal, and test datasets from CSV files.
2. **Function Selection**: It selects the best four ideal functions that minimize the sum of squared y-deviations.
3. **Test Data Mapping**: Maps test data to selected ideal functions if the deviation does not exceed a threshold.
4. **Data Storage**: All processed data is stored in an SQLite database.
5. **Visualization**: The results, including mappings and deviations, are displayed using Bokeh.
6. **Automated Report Generation**: Outputs results to an Excel file and opens it automatically.

---

## Dataset Information

The project utilizes three main datasets:

- **Training Dataset** (`train.csv`): Contains x-y pairs for four training functions used to select the best-fitting ideal functions.
- **Ideal Functions Dataset** (`ideal.csv`): Contains x-y pairs for 50 ideal functions. The program determines the four best matches for the training functions.
- **Test Dataset** (`test.csv`): Contains x-y pairs of test points. These are mapped to one of the four selected ideal functions based on a threshold criterion.

---

## Code Structure

The repository consists of the following key files:

- ``: The main execution file that runs the entire pipeline.
- ``: Handles loading and saving data from CSV and databases.
- ``: Implements function selection and test data mapping logic.
- ``: Manages SQLite database operations using SQLAlchemy.
- ``: Uses Bokeh to generate interactive graphs.
- ``: Contains unit tests to validate functionality.

---

## Expected Output

1. **Excel File Output**:

   - The program generates an Excel file containing:
     - Full logs of the function selection and mapping process.
     - Mapped test data with assigned ideal functions and deviation values.

2. **Graph Generation**:

   - The Bokeh visualization displays:
     - Training data as blue scatter points.
     - Selected ideal functions as green lines.
     - Mapped test data as red points, indicating whether they met the threshold.

---

## Identified Ideal Functions

After processing the data, the following four ideal functions were selected:

- **y1 → y41**
- **y2 → y11**
- **y3 → y42**
- **y4 → y48**

These functions were chosen based on the Least Squares Method, ensuring the best fit for the given training data. The Bokeh visualization confirms the correct mapping and thresholding of test data.

   ```

This branch focuses on a simplified overview, making it easier to understand the core functionalities and how results are processed and presented.

