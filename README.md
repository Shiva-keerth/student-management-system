🎓 Student Performance Management System
A full-featured student records management system built with Python and Streamlit, using session state for in-memory data persistence — no database required.

🎯 Objective
Manage student academic records with real-time performance analytics, automated grading, subject-wise breakdowns, and dynamic top performer tracking.

🚀 Key Features

📝 Add student records — name, roll number, subject & marks
🚫 Duplicate detection — prevents same roll number having multiple entries for the same subject
🏅 Automated grading engine:

A → 90 and above
B → 75 to 89
C → 60 to 74
Fail → below 60


🔍 Filter records by subject
📊 Performance Analytics:

Total records
Average marks
Highest marks
Lowest marks


📚 Subject-wise average breakdown across 4 subjects
🏆 Dynamic Top Performer tracker
🗑️ Delete last record & Reset All options
📋 Last action tracker using session state


🛠️ Tech Stack
ToolPurposePythonCore programming languageStreamlitInteractive web app UISession StateIn-memory data persistenceDatetimeRecord timestamping

📁 Project Structure
student-management-system/
│
├── student_management.py    # Main Streamlit app
├── requirements.txt         # Dependencies
└── README.md                # Project documentation

▶️ How to Run

Clone the repository

bashgit clone https://github.com/Shiva-keerth/student-management-system.git
cd student-management-system

Install dependencies

bashpip install -r requirements.txt

Run the Streamlit app

bashstreamlit run student_management.py

📊 Outcome

Built a fully functional student management system without any database
Demonstrated real-world use of Streamlit session state for data persistence
Automated grading and analytics computed in real time from session data


👤 Author
Shiva Keerth G
📧 gantishivakeerth@gmail.com
🔗 GitHub | LinkedIn
