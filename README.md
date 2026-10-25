# Grass Assignment

A repository containing two Python data science and software engineering projects:
1. **Analysis on Titanic Dataset**: Exploratory Data Analysis (EDA), feature engineering, and predictive modeling using NumPy, Pandas, Matplotlib, and Scikit-Learn.
2. **Library Management System Using Python**: An Object-Oriented Library Management System with borrowing rules, fine calculations, JSON persistence, analytics reporting, and an interactive CLI menu.

---

## Repository Structure

```text
Grass-Assignment/
├── Analysis on titanic dataset/
│   ├── Titanic_Analysis.ipynb         # EDA, feature engineering, and ML modeling
│   └── Titanic-Dataset.csv            # Titanic dataset
├── Library management using python/
│   └── Library_Management_System.ipynb # OOP Library Management System notebook
├── .gitignore                         # Standard Python & Jupyter ignore rules
├── requirements.txt                   # Python package dependencies
└── README.md                          # Project documentation
```

---

## Project 1: Analysis on Titanic Dataset

### Overview
This project performs an end-to-end data science workflow on the classic Titanic passenger dataset to explore survival factors and build predictive machine learning models.

### Workflow & Key Highlights
- **Data Inspection & Cleaning**:
  - Identified and handled missing values: imputed missing `Age` with the median, filled missing `Embarked` entries with mode, and dropped the sparse `Cabin` feature.
  - Checked for duplicates and verified data integrity.
- **Feature Engineering**:
  - Extracted passenger titles (`Mr`, `Mrs`, `Miss`, `Master`, `Other`) from names.
  - Created composite features: `FamilySize` (`SibSp + Parch + 1`) and `IsAlone`.
  - Discretized ages into bins (`AgeGroup`) and flagged minors (`IsChild`).
  - Addressed right-skewed `Fare` distribution using logarithmic transformations (`np.log1p`).
  - Standardized continuous features using Z-score scaling.
- **Exploratory Data Analysis & Visualizations**:
  - Survival rate comparisons across gender, passenger class (`Pclass`), and embarkation points.
  - Cross-tabulations and pivot tables examining multi-variable interactions.
  - Data visualizations using Matplotlib: survival distribution bars, age histograms, fare scatter plots, and correlation matrices.
- **Machine Learning Modeling**:
  - Supervised binary classification using:
    - **Logistic Regression** (with 5-fold cross-validation)
    - **Decision Tree Classifier**
    - **Random Forest Classifier**
  - Evaluated performance with accuracy, precision, recall, and confusion matrices.
  - Extracted feature importances to assess key predictors of survival.

---

## Project 2: Library Management System Using Python

### Overview
An Object-Oriented Programming (OOP) implementation of a comprehensive Library Management System designed in Python.

### Core Architecture
- **`Book` Class**:
  - Attributes: `book_id`, `title`, `author`, `total_copies`, `available_copies`.
  - Methods for adjusting stock and tracking availability.
- **`Member` Class**:
  - Attributes: `member_id`, `name`, `borrowed_books` (mapping book IDs to issue dates).
  - Borrowing limits (up to 3 books per member).
- **`Library` Class**:
  - **Catalog Management**: Add new books, increase stock of existing titles, and remove books safely.
  - **Member Registration**: Register new members and view active members.
  - **Search Capabilities**: Case-insensitive search across book titles and authors.
  - **Lending & Returns**:
    - Validates borrowing limits and copy availability.
    - 14-day standard lending period.
    - Calculates overdue fines for late returns (e.g., ₹5/day after due date).
  - **Data Persistence**:
    - Serializes library state into `library_data.json` (`save()`).
    - Deserializes and restores state on startup (`load()`).
  - **Analytics & Reporting**:
    - Integrates with `pandas` to generate transaction history logs.
    - Generates visual distribution charts of borrowed books using `matplotlib`.
  - **Interactive CLI Menu**:
    - Console-based interactive menu (`menu(lib)`) for adding books, registering members, searching, issuing/returning books, viewing reports, and saving data.

---

## Installation & Setup

### 1. Prerequisites
Ensure you have Python 3.8+ installed.

### 2. Clone the Repository
```bash
git clone https://github.com/divyajeetswami5-tech/Grass-Assignment.git
cd Grass-Assignment
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Running the Notebooks
Launch Jupyter Notebook or JupyterLab:
```bash
jupyter notebook
```
Navigate to:
- `Analysis on titanic dataset/Titanic_Analysis.ipynb`
- `Library management using python/Library_Management_System.ipynb`

---

## Technologies Used
- **Language**: Python 3.x
- **Libraries**:
  - `NumPy` - Numerical operations & array transformations
  - `Pandas` - Data manipulation, pivot tables, and tabular analysis
  - `Matplotlib` - Data visualization & plotting
  - `Scikit-Learn` - Predictive classification models & evaluation metrics
  - `JSON` & `DateTime` - File persistence and date/fine calculations

---

## Author
- **Divyajeet Swami**
- GitHub: [@divyajeetswami5-tech](https://github.com/divyajeetswami5-tech)
