# Day 3 - Data Modeling in Salesforce

## 1. Difference Between App, Object, Record, Field
- **App** → A collection of tabs and objects grouped for a business purpose (e.g., Sales App).
- **Object** → A database table in Salesforce that stores records (e.g., Account, Contact).
- **Record** → A single row of data in an object (e.g., one Account = Microsoft).
- **Field** → A column in the object that stores specific data (e.g., Account Name, Phone Number).

## 2. Standard vs Custom Objects
- **Standard Objects:** Predefined by Salesforce (Account, Contact, Opportunity, Lead).
- **Custom Objects:** Created by users to fit unique business needs (e.g., Student, Course, Hostel).

## 3. My College Data Model
- **Objects:**
  - Student
  - Course
  - Professor
  - Department
- **Relationships:**
  - A Student enrolls in many Courses (Many-to-Many).
  - A Professor teaches many Courses (One-to-Many).
  - Each Course belongs to one Department (Many-to-One).
- **Diagram/Image:**
 

## 4. Formula Fields
Formula fields automatically calculate values based on other fields.
- **Example 1:** GPA Calculation → `Total Points / Total Credits`
- **Example 2:** Student Full Name → `FirstName + " " + LastName`
- **Explanation:** Formula fields save time by automating repetitive calculations and ensuring consistency.

## 5. Validation Rules
Validation rules prevent invalid data entry by enforcing conditions.
- **Example 1:** Student Age must be greater than 16 → `Age < 16` → Error: "Student must be at least 16 years old."
- **Example 2:** Email must contain “@” → `NOT(CONTAINS(Email,"@"))` → Error: "Enter a valid email."
- **Explanation:** Validation rules improve data quality by blocking incorrect or incomplete entries early.

## 6. Reflection: Why Structured Enterprise Data Matters
Structured data ensures consistency, accuracy, and scalability in enterprise systems. It allows businesses to manage complex relationships, automate processes, and make reliable decisions.

---

## ✅ End of Day Outcome
By completing this, I can clearly explain:
- How Salesforce stores business data (Apps, Objects, Records, Fields).  
- How enterprise systems are structured with relationships.  
- Why relationships are critical for meaningful insights.  
- The difference between Formula Fields and Validation Rules.  
- How no-code business logic works in Salesforce.  

