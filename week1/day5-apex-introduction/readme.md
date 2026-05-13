# Day 5 - Apex Introduction

## Topics Covered

- What is Apex?
- Declarative vs Programmatic Development
- Flow vs Apex
- Business Logic in Salesforce
- Apex Use Cases
- Pseudocode and Logic Building
- Integrated Enterprise System Design

---

# What is Apex?

Apex is a programming language developed by Salesforce for implementing custom business logic on the Salesforce platform.  
It is object-oriented and similar to Java in syntax and structure.  
Apex allows developers to create complex logic, automate processes, integrate external systems, and manipulate Salesforce data programmatically.

Apex is mainly used when Salesforce declarative tools like Flows and Validation Rules are not enough to handle advanced business requirements.

---

# Why Salesforce Needs Apex

Salesforce provides many no-code tools such as Flows, Validation Rules, and Process Automation.  
However, enterprise applications often require advanced calculations, integrations, and complex decision-making logic that cannot be fully implemented using clicks alone.

Apex provides flexibility and control to handle these advanced business requirements efficiently.

---

# Difference Between Flow and Apex

| Flow | Apex |
|------|------|
| No-code automation tool | Programming language |
| Easy to build using UI | Requires coding knowledge |
| Best for simple automation | Best for complex logic |
| Faster development | More flexible and powerful |
| Used for standard workflows | Used for advanced business logic |

---

# Difference Between Configuration and Coding

## Configuration (No Code)

Configuration uses Salesforce built-in tools to customize applications without programming.  
It is easier to maintain and faster to implement for simple business requirements.

### Examples
- Validation Rules
- Flows
- Page Layouts
- Formula Fields

---

## Coding (Apex)

Coding is used when business requirements are too complex for declarative tools.  
Apex allows developers to create advanced logic, integrations, and customized automation.

### Examples
- External payment gateway integration
- Complex scholarship eligibility calculation
- Advanced approval systems

---

# Real Examples Where Apex Is Needed

## 1. Complex Scholarship Eligibility Calculation

The system calculates scholarship eligibility based on attendance, marks, family income, category, and extracurricular activities.

### Why Flow Is Not Enough?
The logic involves multiple conditions, calculations, and advanced decision-making that becomes difficult to manage using only Flows.

---

## 2. Integration with External Payment System

The College Management System connects with an online payment gateway to verify fee transactions automatically.

### Why Flow Is Not Enough?
External API integration and secure transaction handling require Apex programming.

---

## 3. Automatic Timetable Conflict Detection

The system checks whether faculty or students already have another class scheduled at the same time.

### Why Flow Is Not Enough?
The process requires complex comparisons across multiple records and advanced validation logic.

---

# Integrated College Management System Design

## CRM Integration

The system manages the complete student admission and academic process using Salesforce CRM concepts.

### CRM Workflow
Lead → Student Admission → Course Enrollment → Fee Management → Academic Tracking

---

# Objects Used

- Student
- Faculty
- Course
- Department
- Fee Details

---

# Relationships

| Object | Relationship | Related Object |
|--------|--------------|----------------|
| Student | Lookup | Course |
| Faculty | Lookup | Department |
| Course | Lookup | Department |
| Student | Lookup | Faculty |

---

# Validation Rules Used

## 1. Student Email Cannot Be Empty
Ensures every student record contains valid contact information.

---

## 2. Course Start Date Cannot Be After End Date
Prevents invalid course schedules.

---

## 3. Student Phone Number Must Contain 10 Digits
Maintains clean and accurate contact data.

---

# Formula Fields Used

## 1. Attendance Percentage
Automatically calculates student attendance percentage.

---

## 2. Total Fee Balance
Calculates remaining fee amount after payment.

---

## 3. Course Duration
Calculates total duration between course start and end dates.

---

# Flow Automation Used

## 1. Auto Email After Registration
Automatically sends confirmation emails after student registration.

---

## 2. Fee Payment Reminder
Automatically reminds students before fee due dates.

---

## 3. Low Attendance Notification
Automatically alerts students and faculty when attendance falls below the required percentage.

---

# Apex Business Logic Used

## 1. Scholarship Eligibility Processing
Calculates eligibility using advanced conditions and multiple data factors.

---

## 2. External Payment Verification
Validates payment transactions from external systems.

---

## 3. Timetable Conflict Detection
Checks for overlapping schedules before assigning classes.

---

# Pseudocode Examples

## Example 1 - Course Seat Validation

```text
IF available seats = 0
THEN block student registration
ELSE allow admission
```

---

## Example 2 - Attendance Alert

```text
IF attendance percentage < 75
THEN send warning notification to student
```

---

## Example 3 - Fee Due Reminder

```text
IF fee due date is within 5 days
THEN send reminder email
```

---

# Reflection - Why Enterprise Systems Need Programming

Enterprise systems handle very large and complex business operations.  
No-code tools are useful for simple workflows, but they cannot handle every business requirement.  
Complex calculations, integrations, dynamic processing, and advanced automation often require programming.

Apex provides the flexibility needed to build scalable and customized enterprise applications in Salesforce.

---

# Learning Outcomes

Through this task, I learned:
- What Apex is
- Why programming is needed in Salesforce
- Difference between Flow and Apex
- Difference between configuration and coding
- How business logic works in enterprise systems
- How Salesforce concepts connect together
- Importance of balancing no-code and code solutions

---

# Screenshots
