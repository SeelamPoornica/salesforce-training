# 🚀 Salesforce Training: Day 3 - Data Modeling & Business Logic

## 🎯 Goal for Today

Today was all about understanding how Salesforce actually stores business data. I learned how to build a structured system using **Objects, Fields, and Records**, and how to use **Relationships** and **Automated Logic** to keep data clean.

---

## 🏛️ 1. The Building Blocks of Salesforce

I learned that the platform follows a specific hierarchy to keep data organized:

* **App:** The top-level container (like my "Wedding Wonders" App) that holds all related tools together.


* **Object:** These are like database tables or digital folders for different categories (e.g., Lead, Account, Contact).


* **Record:** A single entry inside an object (e.g., "The Sharma Wedding" is a record inside the Wedding object).


* **Field:** The specific details inside a record, like "Wedding Date" or "Guest Count".



**Standard vs. Custom Objects:**

* **Standard Objects:** Built-in by Salesforce, like **Accounts** and **Contacts**.


* **Custom Objects:** Ones I create for specific business needs, like **Venues** or **Caterers**.



---

## 💍 2. My Data Model: Wedding Management System

For today’s task, I mapped out the relationships for a Wedding System:

* **Objects Created:** Bride/Groom (Contact), Vendor (Account), Wedding Project (Opportunity), and Venue (Custom Object).


* **Relationships:** I used **Lookup Relationships** because they allow objects to stay independent but still talk to each other.


* **One-to-Many:** One **Venue** can host many different **Weddings** over time.


* **Why it matters:** Without relationships, data is just a list. Relationships allow me to see which Caterer is linked to which Wedding instantly.





---

## 🧪 3. Formula Thinking (Task 2)

Formula fields are great because they do the math for me automatically.

1. **Total Budget Remaining:** `Total_Budget__c - Amount_Spent__c`. This shows the couple their balance instantly.


2. **Full Client Name:** `FirstName & " " & LastName`. This makes sure names look professional on invitations.


3. **Days Until Wedding:** `Wedding_Date__c - TODAY()`. This acts as a countdown for the organizers.

* **Why automate?** It prevents human calculation errors and keeps the dashboard updated in real-time.



---

## 🛑 4. Validation Rule Thinking (Task 3)

Validation rules act as "gatekeepers" to block bad or "dirty" data.

1. **Age Verification:** Ensuring the Bride and Groom are at least 18 years old.


2. **Email Required:** Blocking a record if the email field is empty, so we don't lose contact.


3. **Capacity Check:** Preventing a booking if the "Guest Count" is higher than the "Venue Capacity".



* **What this prevents:** This prevents "garbage data" from entering the system, ensuring our reports are always accurate.



---

## 🤔 5. Reflection: Why Structured Data?

I used to think Excel was enough, but now I see why big companies need Salesforce:

* **Excel vs. Salesforce:** Excel is a "flat" sheet. If you change a vendor's phone number in Excel, you have to find every row where they appear and change it manually. In Salesforce, you change it once on the **Account**, and it updates everywhere.


* **Inconsistent Data:** If data is messy, a business cannot trust its reports. Salesforce uses **Metadata** to ensure the structure stays the same even as the business grows.



---
> **Pro Tip:** I realized today that Salesforce is called a **Metadata-driven platform** because the "data about the data" (the fields and rules I created) tells the system how to behave without me having to write a single line of code!.
> 
>
