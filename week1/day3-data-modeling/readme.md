# **Data Modeling**

## **Topics Covered**

1. Difference Between: App, Object, Record, and Field  
2. Standard vs. Custom Objects  
3. College Data Model (Objects, Relationships, Diagram)  
4. Formula Fields  
5. Validation Rules  
6. Reflection: Why Structured Enterprise Data Matters

## **1\. Difference Between: App, Object, Record, and Field**

Understanding the hierarchy of data in a CRM/Database environment is crucial:

* **App:** A collection of items (such as objects, tabs, and processes) that work together to serve a specific business function or workflow (e.g., a "University Administration" app).  
* **Object:** A database table that stores a specific kind of information. It acts as a container for your data (e.g., a "Student" object or a "Course" object).  
* **Record:** A single instance of data within an object. It represents one specific entity, akin to a row in a spreadsheet (e.g., a specific student named "Jane Doe").  
* **Field:** A specific data point or attribute tracked on a record, akin to a column in a spreadsheet (e.g., "First Name", "Email Address", or "Date of Birth").

## **2\. Standard vs Custom Objects**

* **Standard Objects:** These are built-in, out-of-the-box objects provided by the platform (like Salesforce) to handle common business scenarios. Examples include *Accounts*, *Contacts*, *Leads*, and *Opportunities*.  
* **Custom Objects:** These are objects created by the user or administrator to store information that is unique and specific to their organization's needs. If a university is using the system, they would create Custom Objects like *Students*, *Courses*, and *Enrollments* since those aren't standard B2B sales concepts.

## **3\. College Management System Data Model**

### **Objects**

* **Department:** Stores information about different academic faculties (e.g., Computer Science, Arts).  
* **Professor:** Stores details about the teaching staff.  
* **Course:** Stores information about the classes offered.  
* **Student:** Stores personal and academic details of enrolled students.  
* **Enrollment (Junction Object):** Connects Students to Courses to track who is taking what class.

### **Relationships between obejects**

| Source Object | Relationship Type | Target Object | Description |
| :---- | :---- | :---- | :---- |
| **Department** | One-to-Many | **Course** | One department offers many courses. |
| **Department** | One-to-Many | **Professor** | One department employs many professors. |
| **Professor** | One-to-Many | **Course** | One professor teaches many courses. |
| **Student** | One-to-Many | **Enrollment** | One student has many enrollments. |
| **Course** | One-to-Many | **Enrollment** | One course has many enrollments. |


### **College Mangement System Diagram**


Department  
    |  
    |-- Professor  
    |  
    L-- Course  
          |  
          L-- Enrollment  
                |  
                L-- Student

## **4\. Formula Fields**

**Explanation:** Formula fields are read-only fields that automatically calculate a value based on other fields, expressions, or values in the system. When the underlying data changes, the formula field updates automatically.

**Your Examples:**

1. **Full Name (Text Formula):** Combines First Name and Last Name fields on the Student object so users don't have to type it twice.  
   * *Formula:* First\_Name\_\_c & " " & Last\_Name\_\_c  
2. **Pass/Fail Status (Checkbox Formula):** Evaluates if a student's GPA is above a certain threshold (e.g., 2.0).  
   * *Formula:* GPA\_\_c \>= 2.0  
3. **Total Tuition Fee (Currency Formula):** Calculates the cost of a course by multiplying its credits by a fixed dollar amount per credit (e.g., $500).  
   * *Formula:* Credits\_\_c \* 500

## **5\. Validation Rules**

**Explanation:** Validation rules verify that the data entered by a user meets specific standards before the record can be saved. If the data violates the rule, the system prevents the save and displays a custom error message.

**Your Examples:**

1. **Valid GPA Range:** Ensures a user cannot enter a GPA less than 0.0 or greater than 4.0.  
   * *Condition:* OR(GPA\_\_c \< 0.0, GPA\_\_c \> 4.0)  
   * *Error Message:* "GPA must be between 0.0 and 4.0."  
2. **Phone Number Required:** Ensures a contact phone number is entered when creating a new student record.  
   * *Condition:* ISBLANK(Phone)  
   * *Error Message:* "A contact phone number is required for all enrolled students."  
3. **Future Graduation Year:** Prevents a user from accidentally setting an expected graduation year that has already passed.  
   * *Condition:* Expected\_Graduation\_Year\_\_c \< YEAR(TODAY())  
   * *Error Message:* "Expected graduation year cannot be in the past."

## **6\. Reflection**

**Why structured enterprise data matters:**

Structured enterprise data is the backbone of any successful organization. Without a clear data model (like defining specific objects, relationships, and validations), data becomes messy, duplicated, and unreliable. Proper structuring ensures data integrity, meaning reports and dashboards reflect reality, enabling leadership to make accurate, data-driven decisions. Furthermore, structured data is a prerequisite for automation; you cannot automate workflows or triggers if the system doesn't understand how a "Student" record relates to an "Enrollment" record.

## **Learning Outcomes**

By completing this assignment, the following learning outcomes were achieved:

* Mastered the foundational vocabulary of relational databases and CRM platforms (App, Object, Record, Field).  
* Gained the ability to conceptualize and map out real-world entities into a functional data model (ERD).  
* Learned how to establish appropriate data relationships (One-to-Many, Many-to-Many).  
* Acquired practical skills in automating data entry using Formula Fields.  
* Understood how to enforce data hygiene and integrity using Validation Rules.  
* Recognized the broader business value of maintaining structured, well-architected enterprise data.
