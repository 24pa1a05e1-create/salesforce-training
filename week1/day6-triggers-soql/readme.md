# SOQL and Apex Trigger Basics

## 1. What is SOQL?

SOQL (Salesforce Object Query Language) is a query language used in Salesforce to retrieve data from objects. It is similar to SQL but is specially designed for Salesforce records and relationships.

---

## 2. What is an Apex Trigger?

An Apex Trigger is a piece of Apex code that executes automatically when records are created, updated, deleted, or restored in Salesforce. Triggers are used to automate business logic and maintain data consistency.

---

## 3. Difference

### Flow vs Trigger

| Flow | Trigger |
|---|---|
| Created using drag-and-drop tools | Written using Apex code |
| No coding knowledge required | Requires programming knowledge |
| Best for simple automation | Best for complex logic |
| Easier to maintain | More flexible and powerful |

### Before vs After Trigger

| Before Trigger | After Trigger |
|---|---|
| Executes before data is saved to the database | Executes after data is saved to the database |
| Used to validate or modify data | Used for related record operations |
| Faster because changes happen before save | Used when record ID is needed |
| Example: Updating field values | Example: Sending notifications |

---

## 4. Your Trigger Use Cases

1. Automatically set admission status when a student record is created.  
2. Send an email notification when admission is approved.  
3. Prevent duplicate student records from being saved.  
4. Update total fee amount after course selection.  
5. Create a follow-up task when a new lead is added.

---

## 5. Query Examples (English Query Ideas)

- Get all students from a particular college.  
- Find students whose admission status is approved.  
- Display all leads created today.  
- Retrieve contacts with missing phone numbers.  
- Show opportunities related to a specific course.

---

## 6. Reflection

Enterprise systems react automatically to data changes to improve efficiency, accuracy, and productivity. Automation helps organizations reduce manual work, maintain consistent data, send instant notifications, and ensure business processes happen quickly without human intervention.
---
## Screenshots


![](https://github.com/24pa1a05e1-create/salesforce-training/blob/main/week1/day6-triggers-soql/day6-database%20%26%20net-basics.png)
![](https://github.com/24pa1a05e1-create/salesforce-training/blob/main/week1/day6-triggers-soql/day6-Apex%20Triggers.png)
