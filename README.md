🎓 Educational Organisation Using ServiceNow
A ServiceNow-based Educational Management System that streamlines admissions, student and teacher data management, and academic progress tracking with automated workflows and clean form designs 📚⚙️.

👥 Team Members
Team ID: NM2025TMID20274 🏷️.

Team Leader: SARIGASREE SANDHIYAPPAN S 👩‍💼.

Team Member 1: MONISHA S 👤.

Team Member 2: DIVYA BHARATHI S 👤.

Category: ServiceNow System Administrator 🧑‍🔧.

📌 Project Overview
The Educational Management System centralizes student and teacher records, automates admission procedures, and tracks academic progress within a single ServiceNow application for real-time operational visibility 🧭. It reduces manual errors and enhances decision-making with standardized tables, process flows, number maintenance, and client-side scripts 🧩.

⚡ Key Features
Central repository for student and teacher profiles with controlled form behaviors and display fields 🗂️.

Admissions workflow states: New, InProgress, Joined, Rejected, Rejoined, Closed, Cancelled 🔁.

Student Progress tracking with computed Total, Percentage, and Result for consistent evaluation 🧮.

Client-side automation: pincode-based auto-fill for location fields and pass/fail logic with validation 🧑‍💻.

Number Maintenance for standard Admin Number sequencing with Dynamic Default “Get Next Padded Number” 🔢.

🛠 Skills Required
TensorFlow for future predictive analytics and intelligent insights into academic outcomes 🔮.

🎯 Project Goal
Streamline admissions and academic tracking through a centralized, automated ServiceNow solution 🎯.

Improve data integrity and visibility to support timely, data-driven decisions across departments 📈.

💻 Technologies Used
Platform: ServiceNow (Tables, Form Design, Local Update Sets, Process Flow, Number Maintenance, Client Scripts) 🧱.

🚀 How to Use
Access a Personal Developer Instance from the ServiceNow Developer Site and verify navigation readiness 🧑‍💻.

Create Local Update Sets (e.g., “Educational Organisation”, “Family Expenses”) and set them as Current for controlled deployment 🧪.

Create the “Salesforce” table, enable Extensible, set Admin Number as Display, configure Grade choices, and set Dynamic Default to “Get Next Padded Number” 🧰.

Create the “Student Progress” table, add module under the Salesforce menu, and define Subjects, Marks, Grade, Remarks, Total, Percentage, Result 🧭.

Configure Form Design for Salesforce, Admission, and Student Progress; add Admission Number to Student Progress and arrange fields clearly 🧩.

Create Number Maintenance for Admin Number sequencing to ensure consistent identifiers 🔢.

Build a Process Flow for Admissions with the defined state sequence and verify transitions 🔄.

Add Client Scripts: disable calculated fields onLoad, compute percentage onChange, set result with validation, and auto-populate location from pincode where applicable 🛡️.

🧑‍💻 Client Script Examples
Disable Calculated Fields (onLoad) 🧯

javascript
function onLoad() {
  g_form.setDisabled('u_total', true);
  g_form.setDisabled('u_percentage', true);
  g_form.setDisabled('u_result', true);
}
Percentage Calculation (onChange) 📊

javascript
function onChange(control, oldValue, newValue, isLoading, isTemplate) {
  if (isLoading || newValue === '') { return; }
  var Percentage = (Total / 600) * 100;
  g_form.setValue('u_percentage', Percentage + '%');
}
Result Logic & Validation (onChange) ✅
Compute pass/fail from u_percentage, handle invalid ranges by clearing u_result, and document logic for maintainability 📋.

Pincode Auto-Populate (Admission) 📮
Auto-fill u_mandal, u_city, and u_district for specific pincodes like 509358, 500081, 500079 🗺️.

🔮 Future Enhancements
Integrate TensorFlow for predictive analytics on admissions and student performance forecasting 📈.

Extend workflows for teacher lifecycle events, auditing, and richer executive dashboards 🧭.

📄 License
Add an open-source license compatible with institutional collaboration requirements
