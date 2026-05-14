# Day 5 - Apex Introduction

## 1. What is Apex?
Apex is Salesforce’s proprietary programming language, similar to Java, designed specifically for building custom logic on the Salesforce platform. It allows developers to write code that runs on Salesforce servers, enabling complex business processes, integrations, and customizations beyond what declarative tools (like Flows) can achieve.

## 2. Differences
- **Flow vs Apex:**  
  - Flow is a no-code automation tool for admins.  
  - Apex is a programmatic solution for developers, used when logic is too complex for Flows.
- **Configuration vs Coding:**  
  - Configuration uses point-and-click tools (fields, workflows, validation rules).  
  - Coding uses Apex, Visualforce, or Lightning Web Components for advanced customization.

## 3. Real Examples Where Apex Is Needed
1. Complex calculations across multiple objects (e.g., calculating weighted GPA across courses).  
2. Integrating Salesforce with external systems via APIs.  
3. Custom triggers that enforce advanced business rules (e.g., automatically assigning professors based on course load).

## 4. Integrated System Design (College Management System)
- **CRM:** Used to manage students, professors, courses, and departments.  
- **Objects:** Student, Course, Professor, Department.  
- **Relationships:**  
  - Students ↔ Courses (Many-to-Many).  
  - Professors ↔ Courses (One-to-Many).  
  - Courses ↔ Departments (Many-to-One).  
- **Validation:** Prevent invalid student ages or missing emails.  
- **Flow:** Automate enrollment notifications and course assignments.  
- **Apex:** Handle complex GPA calculations, integrate with external grading systems, and enforce advanced scheduling rules.

## 5. Pseudocode Examples
// Example 1: GPA Calculation
trigger CalculateGPA on Student (before insert, before update) {
for each student in Trigger.new {
student.GPA = student.TotalPoints / student.TotalCredits;
}
}

// Example 2: Auto-assign Professor
trigger AssignProfessor on Course (after insert) {
for each course in Trigger.new {
if (course.Department == 'Computer Science') {
course.Professor = 'Dr. Sharma';
}
}
}

// Example 3: External API Callout
class StudentAPI {
public static void syncStudentData(Student s) {
HttpRequest req = new HttpRequest();
req.setEndpoint('https://external-system.com/api/students');
req.setMethod('POST');
req.setBody(JSON.serialize(s));
Http http = new Http();
HttpResponse res = http.send(req);
}
}


## 6. Reflection: Why Enterprise Systems Eventually Need Programming
Programming is essential when business requirements go beyond simple automation. Apex provides flexibility, scalability, and integration capabilities that declarative tools cannot fully achieve.

---

## ✅ End of Day Outcome
By completing this, I can clearly explain:
- Why Apex exists and how it fits into Salesforce.  
- The difference between declarative (Flows) and programmatic (Apex) logic.  
- How CRM, Objects, Relationships, Validation, Flow, and Apex connect together in a complete system.
