---

# ⚡ Salesforce Training: Day 4 - Flow Builder & Automation

## 🏗️ 1. What is Flow Builder?

Flow Builder is a visual tool within Salesforce that allows administrators to automate business processes without writing any code. It is used to design logic that performs actions—like sending emails or updating records—based on specific triggers.

## 🔄 2. Types of Flows

There are several types of flows, but these are the two most common:

* 
**Screen Flow:** A flow that requires user interaction. it provides a guided UI (like a form or wizard) to collect information from a user.


* 
**Record-Triggered Flow:** An automation that runs silently in the background whenever a record is created, updated, or deleted.



## 💡 3. My Automation Ideas (Wedding System)

Based on my **Wedding Management System**, here are 5 processes that can be automated to improve efficiency:

1. 
**Welcome Email to Couple:** Automatically send a brochure and price list when a new **Lead** (inquiry) is created.


2. 
**Payment Milestone Reminder:** Send an automated email to the couple 10 days before their next payment is due.


3. **Vendor Confirmation:** Automatically notify the **Photographer** or **Caterer** (Contacts) as soon as the Wedding date is marked as "Venue Secured."
4. **Budget Alert:** If the "Total Expense" field on a Wedding record exceeds the "Maximum Budget" field, send a notification to the Wedding Planner immediately.
5. **Task Creation for New Clients:** When a Lead is converted to a **Contact**, automatically create a "Wedding Checklist" task for the account manager to follow up.

## ✍️ 4. My Flow Diagram (Task 2)

This logic represents a **Record-Triggered Flow** for the "Welcome Email" process:

**[ TRIGGER ]**
*New Lead record is created*
⬇️
**[ DECISION ]**
*Does the Lead have an Email address?*
⬇️
**( If Yes )** ➡️ **[ ACTION ]** ➡️ *Send "Wedding Welcome Package" Email*
⬇️
**( If No )** ➡️ **[ ACTION ]** ➡️ *Create a "Call Lead" Task for the Planner*

## 🛠️ 5. Manual vs. Automated Process

For **Task 3**, I compared the process of tracking vendor payments:

* 
**Manual Process:** A wedding planner manually checks a spreadsheet every morning to see which payments are due, then types out individual emails to couples.


* 
**Problems:** This is time-consuming, prone to human error, and emails might be forgotten.


* 
**Salesforce Automation:** A **Scheduled Flow** checks all records daily and sends the emails automatically at 9:00 AM.


* 
**Improvement:** This ensures 100% consistency and allows the planner to focus on creative tasks instead of paperwork.



## 🤔 6. Reflection: Why Automation Matters

Automation is critical in enterprise systems because it ensures that repetitive business processes are handled accurately every time. It improves productivity by removing manual tasks and prevents data errors caused by human forgetfulness. Using **no-code** tools like Flow Builder allows businesses to adapt their logic quickly without needing a team of developers.

---
