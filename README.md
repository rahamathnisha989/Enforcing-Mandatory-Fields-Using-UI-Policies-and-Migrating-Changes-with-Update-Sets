📌 Project Overview

This project demonstrates how to enforce mandatory fields dynamically in the ServiceNow platform using UI Policies without writing complex scripts. It also shows how configuration changes can be migrated between different ServiceNow instances using Update Sets.

The implementation ensures better data accuracy, reduces manual errors, and improves maintainability of the ServiceNow system.


---

🎯 Project Objectives

Implement mandatory field validation using UI Policies.

Avoid complex scripting for form validation.

Capture configuration changes using Update Sets.

Migrate configurations between ServiceNow instances such as Development, Testing, and Production.



---

🛠 Tools & Technologies Used

ServiceNow Platform

UI Policies

Update Set Management

Incident Management Module

Admin / Developer Access



---

⚙️ Implementation Steps

1. Create an Update Set

Navigate to System Update Sets → Local Update Sets

Click New

Enter an Update Set name (e.g., Mandatory Field Policy)

Click Submit and select Make Current


2. Create UI Policy

Navigate to System UI → UI Policies

Click New

Select table: Incident

Define condition: State = Resolved

Save the policy


3. Configure UI Policy Action

Open UI Policy Actions

Select field: Resolution Code

Set Mandatory = True

Submit


4. Testing

Open an Incident Record

Change the State to Resolved

Try to save without entering the Resolution Code

The system will prevent saving until the field is filled



---

🔄 Update Set Migration Process

1. Open the created Update Set


2. Verify captured configuration changes


3. Export the Update Set as XML


4. Import the XML file into the target instance


5. Preview the Update Set


6. Commit the Update Set


7. Verify that the UI Policy works in the new instance




---

🎬 Demo Scenario

1. User opens an Incident form


2. User changes the Incident State to Resolved


3. UI Policy triggers automatically


4. Resolution Code field becomes mandatory


5. System prevents saving until the field is completed
