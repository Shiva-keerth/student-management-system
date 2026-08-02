# 🎓 Student Performance Management System

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-UI-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![Session State](https://img.shields.io/badge/Persistence-Session_State-4CAF50?style=for-the-badge)
![No Database](https://img.shields.io/badge/Database-None_Required-blue?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

A fully functional, real-time **Student Academic Records & Performance Analytics Platform** built with Python and Streamlit. Demonstrates advanced use of **Streamlit Session State** as an in-memory data persistence layer — no external database, no backend server required.

---

## 🚀 Core Features

### 📝 Student Records Management
*   **Add Records:** Capture student name, roll number, subject, and marks through a clean 4-column form layout.
*   **Duplicate Detection:** Automatically prevents the same roll number from having multiple mark entries for the same subject, ensuring data integrity.
*   **Subject Filtering:** Filter the records table by subject (Math, Science, English, Computer) or view all records at once.
*   **Record Deletion:** Delete the last inserted record or perform a full data reset with a single click.
*   **Timestamped Entries:** Every record is automatically stamped with the exact date and time it was added.

### 📊 Real-Time Performance Analytics Engine
Analytics are computed dynamically from session state on every render — no pre-computation or caching needed:

| Metric | Description |
| :--- | :--- |
| **Total Records** | Count of all student-subject entries in the current session |
| **Average Marks** | Mean across all subjects and all students |
| **Highest Marks** | Maximum mark across the entire session |
| **Lowest Marks** | Minimum mark across the entire session |

### 🏫 Subject-wise Average Breakdown
Computes and displays the average marks **per subject** across all students for the 4 core subjects: Math, Science, English, and Computer.

### 🏆 Dynamic Top Performer Tracker
Scans the entire session dataset in real-time to identify and highlight the student with the highest marks in the entire system.

### 🎯 Automated Grading Engine
Every record is auto-graded using this rule-based schema:

| Grade | Marks Range |
| :--- | :--- |
| **A** | 90 – 100 |
| **B** | 75 – 89 |
| **C** | 60 – 74 |
| **Fail** | Below 60 |

---

## 🏗️ Application Architecture

```
Input Layer (4-Column Streamlit Form)
    │
    ├── Duplicate Check (Roll No + Subject match)
    │
    └── Session State Store (st.session_state["student"])
              │
              ├── Filter Engine ──────────────────► Filtered Records View
              │
              ├── Performance Analytics Engine ───► Total / Avg / High / Low
              │
              ├── Subject-wise Average Aggregator ► Per-Subject Mean Stats
              │
              └── Top Performer Scanner ──────────► Dynamic Champion Display
```

---

## 🛠️ Tech Stack

| Technology | Purpose |
| :--- | :--- |
| **Python 3.10+** | Core programming language |
| **Streamlit** | Interactive web UI framework |
| **st.session_state** | In-memory data persistence (zero DB overhead) |
| **datetime** | Automatic record timestamping |

---

## 💻 Quick Start & Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Shiva-keerth/student-management-system.git
   cd student-management-system
   ```

2. **Install dependencies:**
   ```bash
   pip install streamlit
   ```

3. **Launch the application:**
   ```bash
   streamlit run student_management_system.py
   ```

---

## 📁 Project Structure

```
student-management-system/
├── student_management_system.py    # Main Streamlit app (all logic)
└── README.md                       # Project documentation
```

---

## 💡 Key Technical Concepts Demonstrated

*   **Stateful Web Apps Without a Backend:** Uses `st.session_state` as a Python list-based in-memory database, demonstrating that fully functional data management UIs can be built without SQL or NoSQL databases.
*   **Real-Time Computation:** All analytics (averages, top performer, subject-wise stats) are computed live from the session store on each render cycle — no cached state needed.
*   **Duplicate-Safe Ingestion:** The duplicate check (`roll_no + subject`) pattern mirrors real-world data validation logic used in production data pipelines.

---

## 🤝 Connect With Me
*   **GitHub:** [Shiva-keerth](https://github.com/Shiva-keerth)
*   **LinkedIn:** [Shiva Keerth G](https://www.linkedin.com/in/shiva-keerth-9574b92a6/)
*   **Focus:** Generative AI, RAG Systems, Agentic AI, and Machine Learning.
