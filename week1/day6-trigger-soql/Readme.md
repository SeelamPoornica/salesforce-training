---

# 🔍 Salesforce Training: Day 6 - SOQL & Apex Triggers

## 🎯 Goal for Today

Today’s focus was on learning how to interact with the Salesforce database using **SOQL** and how to automate complex operations using **Apex Triggers**. These tools allow for high-performance automation that reacts instantly to data changes. 

---

## 🏗️ 1. What is SOQL?

**SOQL (Salesforce Object Query Language)** is a powerful tool used to read data from the Salesforce database.  While it looks similar to SQL, it is specifically designed for the Salesforce platform. It allows me to retrieve specific records and fields, such as finding all "High-Budget Weddings" or "Available Venues" without searching through lists manually. 

---

## ⚡ 2. What is an Apex Trigger?

An **Apex Trigger** is a script that executes before or after specific events happen to a record, such as when it is created, updated, or deleted. It acts as an automated "listener" that waits for a change to occur and then executes custom code to maintain data accuracy or perform complex calculations. 

---

## 🔄 3. Key Differences

### **Flow vs. Trigger**

* 
**Flow:** A visual, no-code tool best for standard business processes and simple logic. 


* 
**Trigger:** A code-based tool used for high-performance logic, handling thousands of records at once (bulkification), or performing complex operations that Flows cannot handle. 



### **Before vs. After Trigger**

* **Before Trigger:** Used to update or validate record values **before** they are saved to the database. For example, checking if a wedding date is already taken. 


* **After Trigger:** Used to access field values set by the system (like Record IDs) and to affect **other** related records after the change is saved. For example, automatically creating a "Thank You" task for a vendor once a wedding is completed. 



---

## 💡 4. My Trigger Use Cases (Wedding System)

Following the "Automation Thinking" task, here are 5 ways I would use Triggers in my system: 

1. 
**Duplicate Date Blocker:** A "Before Trigger" that prevents a new Wedding from being saved if the chosen Venue is already booked for that specific date. 


2. 
**Auto-Budget Update:** An "After Trigger" that automatically updates the "Total Expenses" on a Wedding record whenever a new Vendor Payment is added. 


3. 
**Vendor Availability Sync:** When a Wedding is canceled, a trigger automatically updates the "Availability" status of all linked Vendors (Caterers, Photographers). 


4. 
**Premium Client Flag:** A trigger that automatically marks a couple as a "VIP Client" if their total wedding budget exceeds ₹10,00,000. 


5. 
**Task Cleanup:** A trigger that deletes all pending "Follow-up" tasks if a Lead is disqualified or the wedding contract is canceled. 



---

## 📝 5. Query Examples (SOQL in English)

For **Task 5**, here are three queries I would use to manage my system:

* **Query 1:** "Select the Name and Wedding Date of all Couples where the Wedding Stage is 'Planning'."
* **Query 2:** "Find all Vendors who are located in 'New York' and have a rating of 5 stars."
* **Query 3:** "Get a list of all Weddings where the Total Budget is greater than ₹50,000 and the Ceremony is happening this month."

---

## 🤔 6. Reflection: Automatic Data Reactions

Enterprise systems react automatically to data changes to ensure **consistency** and **speed**. In a large-scale business, manual updates lead to "bad data" or forgotten tasks. Triggers ensure that every time a single piece of information changes, the entire system updates instantly. This prevents errors, keeps the team synchronized, and allows the business to scale without needing a human to double-check every record. 

--- 
> **Key Learning:** I realized today that while Flows are the "user-friendly" way to automate, Triggers and SOQL are the "professional-grade" tools that give developers total control over how data behaves in an enterprise environment. 
> 
>
