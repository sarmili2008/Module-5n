# Hierarchical Inheritance in Python

This Python project demonstrates **Hierarchical Inheritance** using a base class `Details` and two derived classes `Employee` and `Patient`. The program collects and displays details for both employees and patients.

## 🎯 Aim

To write a Python program that uses **Hierarchical Inheritance** to input and display **Employee** and **Patient** details.

## 📘 Description

- **Base Class:** `Details`
  - Stores common attributes: `name`, `age`
  - Provides methods: `getName()`, `getAge()`

- **Derived Class 1:** `Employee`
  - Inherits from `Details`
  - Adds: `employee_id`, `department`
  - Method: `getEmployeeDetails()`

- **Derived Class 2:** `Patient`
  - Inherits from `Details`
  - Adds: `patient_id`, `disease`
  - Method: `getPatientDetails()`

## 🧠 Algorithm

1. Create base class `Details` with common attributes.
2. Create `Employee` class extending `Details`, adding employee-specific data.
3. Create `Patient` class extending `Details`, adding patient-specific data.
4. Get user input for employee and patient data.
5. Display collected information using class methods.

## Program
class Details:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    def getName(self):
        return self.name
    def getAge(self):
        return self.age

class Employee(Details):
    def __init__(self, name, age, employee_id, department):
        super().__init__(name, age)  # call base class constructor
        self.employee_id = employee_id
        self.department = department
    def getEmployeeDetails(self):
        return {
            "Name": self.getName(),
            "Age": self.getAge(),
            "Employee ID": self.employee_id,
            "Department": self.department
        }

class Patient(Details):
    def __init__(self, name, age, patient_id, disease):
        super().__init__(name, age)  # call base class constructor
        self.patient_id = patient_id
        self.disease = disease
    def getPatientDetails(self):
        return {
            "Name": self.getName(),
            "Age": self.getAge(),
            "Patient ID": self.patient_id,
            "Disease": self.disease
        }

# Example usage
emp = Employee("Alice", 30, "E1024", "Engineering")
pat = Patient("Bob", 45, "P5678", "Hypertension")

print("Employee Details:", emp.getEmployeeDetails())
print("Patient Details:", pat.getPatientDetails())
## Sample Output
Employee Details:
Name: Alice
Age: 30
Employee ID: E1024
Department: Engineering
Patient Details:
Name: Bob
Age: 45
Patient ID: P5678
Disease: Hypertension

##RESULT:
Thus,the python program was run successfully for the given question
