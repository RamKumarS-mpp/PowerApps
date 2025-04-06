# 📌 Cap UK - Performance Tracking System

## 🔧 Overview
This Power Platform-based solution was designed for **Cap UK analysts** to track their daily activities, monitor performance through key metrics, and support **1-2-1 performance evaluations** using Complexity Per Hour scores. It integrates **Power Apps**, **Power Automate**, and **SharePoint Online** to enable seamless data entry, filtering, and automated reminders.

## 🛠️ Components

### 🔹 Power Apps
- **SearchEntries Screen**: Allows users to filter submissions by `WorkflowID` and `Date`.
- **Dashboard Display**: Aggregates and displays total `ComplexityScore`, `TotalHours`, and `ComplexityPerHour` based on the selected date.
- **Role-Based View**: Filters checklist data to show only records submitted by the logged-in analyst.
- **Edit Functionality**: Users can update existing checklist records.

### 🔹 SharePoint Lists
1. **Cap UK - Checklist**
   - Tracks analyst entries including WorkflowID, ComplexityScore, TimeTaken, and Date.
   - Used as the main data source for Power Apps and Power Automate.
2. **AnalystMaster**
   - Stores EmployeeID and Email to validate entries and send reminders.

### 🔹 Power Automate Flows
- **Reminder Flow**: Sends automatic daily email reminders to analysts who haven’t submitted an entry.
- **Edit Tracker Flow**: Updates the ComplexityPerHour when a record is modified without causing infinite trigger loops.
- **Audit Flow** *(optional)*: Logs changes for tracking and compliance purposes.

## 📊 Key Metrics
- **ComplexityPerHour = Total Complexity Score / Total Hours Taken**
- Used to monitor workload and performance efficiency per analyst.

## 💡 Features
- ✅ Analyst-specific filtering
- ✅ Date-based dashboard for performance review
- ✅ Auto email reminders for missing submissions
- ✅ Error-handled flows to prevent loop triggers
- ✅ GitHub version control to preserve stable versions

## 📂 How to Deploy
1. Import `.msapp` into Power Apps.
2. Import `.zip` flows into Power Automate.
3. Connect to your SharePoint lists.
4. Update environment variables and test flows before production.
