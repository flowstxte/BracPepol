
# BracPepol - BRAC University Student Management System

## Overview
BracPepol is a **Python-based OOP project** that manages and analyzes BRAC University student data.  
It reads from a CSV file and provides functionalities for **student information retrieval, academic analysis, blood donor search, and telecommunication insights**.

---

## Features

### Student Data Management
- Reads & processes student data from a CSV file  
- Generates unique IDs (based on year, department, serial)  
- Stores personal details, academics, and contact info  

### Statistical Analysis
- Male-to-female ratio calculation  
- Find students sharing the same birth year or month  

### Blood Donation Management
- Search donors by blood group + location  
- Search donors by blood group + department  

### Academic Performance
- Identify students on probation (CGPA < 2.00)  
- Top 5 **Valedictorian candidates** (CGPA + ≥130 credits)  
- **Gold Medalists** → top CGPA in each department (≥130 credits)  
- **Female Coder Championship** → Female CSE students with CGPA > 3.5 and ≥30 credits  

### Telecommunication Analysis
- Identify SIM card users by operator from phone numbers  

---

## Tech Stack
<p>
  <img src="https://skillicons.dev/icons?i=python" />
</p>

- **Language**: Python 3.6+  
- **Data Source**: CSV file  
- **Libraries**: Python standard `csv` module  

---

## Usage Examples
```python
# Gender ratio
BracPepol.male_femaleRatio()

# Students born in June 2000
BracPepol.siblingFromAnotherMother(2000, 'Jun')

# O+ donors in Uttara (limit 20)
BracPepol.availableBloodDonorByLocation('O+', 'Uttara', 20)

# B+ donors in CSE (limit 100)
BracPepol.availableBloodDonorByDept('B+', 'CSE', 100)

# Probation list
BracPepol.generateProbationStudentInfo()

# Top 5 valedictorian candidates
BracPepol.findValedictorianCandidates()

# Gold medalists by department
BracPepol.findGoldMedalistCandidates()

# Female coder championship candidates
BracPepol.findFemaleCoderChampionshipCandidates()

# Students using TeleTalk SIM
BracPepol.findSIM_users('TeleTalk')
````

---

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/flowstxte/Project-BracPepol.git
cd Project-BracPepol
```

### 2. Prepare the data file

Ensure `data.csv` exists in the correct location or update the path in code:

```python
with open('path/to/data.csv', 'r') as file:
```

### 3. Run the program

```bash
python main.py
```

---

## Data Structure

The CSV file should include:

* Name
* Gender
* Location
* Birthdate
* Blood Group
* Phone
* Department
* Enrolled Year
* Completed Credits
* Current CGPA

---

## License

Licensed under the **MIT License** – see [LICENSE](LICENSE).
