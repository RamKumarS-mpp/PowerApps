**Performance Tracking System**
🔧 Overview
This Power Platform-based solution was designed for Cap UK analysts to track their daily activities, monitor performance through key metrics, and support 1-2-1 performance evaluations using Complexity Per Hour scores. It integrates Power Apps, Power Automate, and SharePoint Online to enable seamless data entry, filtering, and automated reminders.

**🛠️ Components**
🔹 Power Apps
SearchEntries Screen: Allows users to filter submissions by WorkflowID and Date.
Dashboard Display: Aggregates and displays total ComplexityScore, TotalHours, and ComplexityPerHour based on the selected date.
Role-Based View: Filters checklist data to show only records submitted by the logged-in analyst.
Edit Functionality: Users can update existing checklist records.

🔹 **SharePoint Lists**
Checklist File:
Tracks analyst entries including WorkflowID, ComplexityScore, TimeTaken, and Date.
Used as the main data source for Power Apps and Power Automate.

AnalystMaster:
Stores EmployeeID and Email to validate entries and send reminders.

🔹 Power Automate Flows
Reminder Flow: Sends automatic daily email reminders to analysts who haven’t submitted an entry.
Edit Tracker Flow: Updates the ComplexityPerHour when a record is modified without causing infinite trigger loops.

Audit Flow (optional): Logs changes for tracking and compliance purposes.

📊 Key Metrics
ComplexityPerHour = Total Complexity Score / Total Hours Taken

Used to monitor workload and performance efficiency per analyst.
