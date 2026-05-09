# Salesforce Platform Basics

## 1. What is Salesforce Platform?

Salesforce Platform is a cloud-based platform used to build and manage business applications. It helps organizations store data, automate workflows, manage customers, and create applications in a secure environment.

---

## 2. Explain

### App
An App in Salesforce is a collection of tabs, objects, and features designed for a particular business process.

### Object
An Object is a database table used to store information such as student details, admissions, or customer records.

### Tab
A Tab provides access to Salesforce objects and features through the user interface.

---

## 3. Difference: Configuration vs Coding

| Configuration | Coding |
|---|---|
| Uses built-in Salesforce tools | Uses programming languages like Apex |
| No coding knowledge required | Requires coding knowledge |
| Faster and easier to implement | Used for advanced customization |
| Example: Creating fields and workflows | Example: Writing Apex classes and triggers |

---

# System Design

## App

The Salesforce App used in this system is the **College Admission Management App**. It helps manage student enquiries, admissions, and communication in a single platform.

## Objects

The system uses standard Salesforce objects:

- **Account** → College/University  
- **Contact** → Student/Parent  
- **Lead** → Interested Student  
- **Opportunity** → Admission/Application Process  

These objects store and organize all admission-related data.

## User Interaction

1. A student submits an enquiry form.  
2. Salesforce creates a Lead record for the student.  
3. After verification, the Lead is converted into a Contact linked with the College Account.  
4. An Opportunity is created to track the admission or enrollment process.  
5. Staff members can update student details, admission status, and communication records through the Salesforce App.
