# Medical Appointment No-Shows Analysis

This project analyzes a dataset of medical appointments to uncover why approximately 30% of patients miss their scheduled appointments. The analysis includes exploratory data analysis (EDA), model development, error analysis, and insights for improving predictions.

## Overview

A person schedules a doctor’s appointment, receives all the instructions, and still fails to attend. This project seeks to answer key questions:
- What factors influence whether a patient shows up for their appointment?
- Can we predict no-shows using patient demographics, appointment details, and reminders?

## Project Highlights

- **Data Analysis**:
  - Explored relationships between features like `Age`, `DayOfWeek`, `SMS_received`, and `No-show`.
  - Visualized patterns in attendance based on demographics and appointment details.

- **Modeling**:
  - Built a basic predictive pipeline using XGBoost.
  - Preprocessed data by handling categorical variables with one-hot encoding and extracting features from dates (e.g., `DayOfWeek`).

- **Error Analysis**:
  - Identified patterns in misclassified samples (false positives and false negatives).
  - Analyzed the impact of age groups and days of the week on errors.

- **Insights**:
  - Highlighted the influence of neighborhoods, age, and appointment reminders on attendance.
  - Addressed issues with high-cardinality features (`Neighbourhood`) and irrelevant identifiers (`AppointmentID`, `PatientID`).

## Key Files

- **Medical_Appointment_No_Shows.ipynb**:
  - Contains the full implementation, including data preprocessing, model training, and evaluation.

## Steps to Run

1. **Install Dependencies**:
   - Ensure the following Python libraries are installed:
     ```
     pip install pandas numpy matplotlib seaborn xgboost scikit-learn
     ```

2. **Run the Notebook**:
   - Open and execute the `Medical_Appointment_No_Shows.ipynb` file in Jupyter Notebook or JupyterLab.

## Key Visualizations

- **Feature Importance**:
  - Identified top features influencing predictions, highlighting the dominance of age and neighborhoods.
- **Error Analysis**:
  - Visualized the distribution of age and other features in misclassified samples to uncover patterns.

## Next Steps

- Simplify the `Neighbourhood` feature by clustering or grouping to improve generalization.
- Remove irrelevant identifiers (`AppointmentID`, `PatientID`) to reduce noise and overfitting.
- Address class imbalance with techniques like SMOTE to improve recall for no-shows.

## Acknowledgments

This analysis is based on a dataset from medical appointments, exploring insights to optimize scheduling and reduce missed appointments.
