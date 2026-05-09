
# Day 2 - Salesforce Platform Basics

## 1. What is Salesforce Platform?
The Salesforce Platform is a cloud-based environment that allows businesses and developers to build, customize, and deploy applications. It provides tools for managing data, automating processes, and extending CRM functionality without needing to build everything from scratch. It’s the foundation that supports Salesforce CRM and enables developers to create apps tailored to specific business needs.

## 2. Key Concepts
- **App** → A collection of tabs, objects, and functionality grouped together to serve a business purpose. Example: A Sales app that includes Accounts, Contacts, and Opportunities.
- **Object** → A database table in Salesforce that stores records. Example: Account, Contact, Opportunity, or a custom object like “Patient.”
- **Tab** → The user interface element that lets you access an object or app feature. Example: Clicking the “Accounts” tab shows all Account records.

## 3. Difference: Configuration vs Coding
- **Configuration (Declarative Development):** Point-and-click customization using Salesforce’s built-in tools (e.g., creating fields, workflows, reports). No programming required.
- **Coding (Programmatic Development):** Writing custom code (Apex, Visualforce, Lightning Web Components) to extend functionality beyond what configuration allows.

**In short:** Configuration = “no-code/low-code” setup, Coding = “custom development.”

## 4. My System Design (Hospital Example)
- **App:** Hospital Management App  
- **Objects:**  
  - Account = Hospital  
  - Contact = Patient  
  - Lead = New Inquiry  
  - Opportunity = Treatment Plan/Admission  
- **User Interaction:**  
  Staff log into the Hospital Management App → use the **Leads tab** to track new inquiries → convert leads into **Contacts** tied to **Accounts** (hospitals) → create **Opportunities** for admissions or treatments → manage ongoing patient relationships through the app.

---

## ✅ End of Day Outcome
By completing this, I can clearly explain:
- How the Salesforce platform is structured (Apps, Objects, Tabs).  
- How CRM fits into the platform (Accounts, Contacts, Opportunities).  
- How developers build on Salesforce using both configuration and coding.  
