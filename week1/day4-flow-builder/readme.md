# Day 4 - Flow Builder and Automation

## Topics Covered

- Flow Builder in Salesforce
- Business Process Automation
- Types of Flows
- Record Automation
- Manual vs Automated Processes
- No-Code Workflow Automation

---

# What is Flow Builder?

Flow Builder is a Salesforce automation tool used to automate business processes without writing code.  
It allows users to create workflows using a visual interface with logic, decisions, and actions.  
Flow Builder helps organizations reduce manual work, improve accuracy, and save time.

---

# Why Automation is Important

Automation helps businesses perform repetitive tasks automatically with less human effort.  
It improves consistency, reduces errors, increases productivity, and speeds up business operations.  
Salesforce automation helps organizations manage workflows efficiently using no-code tools.

---

# Types of Flows

## Screen Flow

A Screen Flow is an interactive flow that collects user input through screens.  
It is used when users need to enter or update information manually.  
Screen Flows guide users step-by-step through a process.

### Example
Student Registration Form

---

## Record Triggered Flow

A Record Triggered Flow runs automatically when a record is created, updated, or deleted.  
It is commonly used for background automation and business process management.  
These flows reduce manual tasks and automate system actions instantly.

### Example
Automatically sending a confirmation email after student registration.

---

# Automation Ideas for College Management System

## 1. Auto Email After Student Registration

When a student successfully registers, Salesforce automatically sends a confirmation email.

### Why Automation Helps?
Reduces manual communication effort and improves student experience.

---

## 2. Auto Generate Student ID

When a new student record is created, the system automatically generates a unique student ID.

### Why Automation Helps?
Avoids duplicate IDs and reduces manual data entry errors.

---

## 3. Auto Update Available Course Seats

Whenever a student enrolls in a course, remaining seats are updated automatically.

### Why Automation Helps?
Helps maintain accurate seat availability information in real time.

---

## 4. Fee Payment Reminder Notifications

The system automatically sends reminders before fee due dates.

### Why Automation Helps?
Improves fee collection efficiency and reduces missed payments.

---

## 5. Notify Faculty When Attendance is Low

Faculty members receive automatic alerts when student attendance falls below the required percentage.

### Why Automation Helps?
Helps identify student issues early and improves academic monitoring.

---

# Flow Design Thinking

## Automation Selected
Auto Email After Student Registration

---

# Flow Steps

```text
Trigger:
Student Record Created

        │
        ▼

Check Student Email Exists?

        │
   ┌────┴────┐
   │         │
 Yes         No
   │         │
   ▼         ▼

Send Email   Stop Flow

   │
   ▼

Update Registration Status

   │
   ▼

End
```

---

# Manual vs Automated Process

## Process Chosen
Fee Payment Reminder System

---

## Manual Process

In a manual system, staff members check fee records regularly and send reminders individually through calls or emails.  
This process takes more time and may lead to missed reminders or delayed communication.

---

## Problems in Manual Process

- Time consuming
- Human errors
- Missed reminders
- Inconsistent communication
- Increased workload

---

## Automated Process Using Salesforce

Salesforce automatically checks fee due dates and sends reminder notifications to students before deadlines.  
This improves efficiency, consistency, and reduces manual effort.

---

# Reflection - Why Automation Matters

Companies automate repetitive business processes to improve productivity and reduce operational effort.  
Automation increases consistency, minimizes human errors, and speeds up workflow execution.  
Enterprise systems use automation to manage large-scale business operations efficiently.

Salesforce Flow Builder allows organizations to automate processes visually without coding.

---

# Learning Outcomes

Through this task, I learned:
- What Flow Builder is
- Types of Salesforce Flows
- Difference between manual and automated workflows
- Importance of automation in enterprise systems
- How no-code automation works in Salesforce
- How business workflows can be improved using Flow Builder

---

# Screenshots
