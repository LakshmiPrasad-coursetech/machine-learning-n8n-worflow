# 🎯 Lead Scoring System — Data Science Intern Test (Project Origins)

This repository contains the end-to-end solution I developed for the **Project Origins Data Science Intern Test**, simulating a real-world B2B SaaS GTM (Go-to-Market) workflow using data science, automation, and cloud tools.

## 🚀 Project Overview

The goal was to build a lead scoring system for a B2B SaaS company targeting mid-market manufacturers. The system identifies high-potential leads based on their firmographics and marketing engagement behavior, then routes them automatically using an automation tool.

---

## 🛠️ Tools & Technologies

| Component             | Tool/Tech               | Purpose                                     |
|----------------------|------------------------|---------------------------------------------|
| Data Processing       | Python (Google Colab)   | Feature engineering, lead scoring model     |
| Data Warehouse        | Snowflake               | Data storage, SQL joins, centralized access |
| Workflow Automation   | n8n                     | Triggered automation, lead routing          |
| Data Export/Transfer  | CSV                     | Intermediate data transfer between tools    |

---

🔹 Step 1: Load Data into Snowflake
Created tables in Snowflake for leads, companies, and engagements using SQL DDL.

Uploaded CSV files (provided for the test) into these tables using the Snowflake UI.

Used SQL to join all three tables and prepare a final dataset with useful columns like total_engagements.

🔹 Step 2: Export Data to Colab
Ran a SQL query in Snowflake to extract the joined dataset.

Exported the query result as a CSV file from the Snowflake UI.

Uploaded the CSV to Google Colab for data analysis and modeling.

🔹 Step 3: Lead Scoring in Python (Colab)
Loaded the CSV in Colab using Pandas.

Cleaned and prepared the data.

Created new features from columns (e.g., engagements, industry, revenue).

Built a simple ML model to assign a lead score.

Exported the scored data as a new CSV file from Colab.

🔹 Step 4: Upload Scored Data Back to Snowflake
Uploaded the scored CSV back into a new table in Snowflake.

Now the warehouse has all leads with their scores, ready for automation.

🔹 Step 5: Automate with n8n
Connected Snowflake to n8n using credentials.

Built a workflow that fetches high-scoring leads from Snowflake.

Created a basic action (like sending a notification or flagging a lead).

Ran the workflow successfully and captured the screenshot.
