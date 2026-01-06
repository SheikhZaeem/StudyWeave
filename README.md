# 🕸️ StudyWeave

### Research Analytics & Artifact Evaluation Platform
> **A scalable, human-in-the-loop (HITL) platform for evaluating AI-generated vs. human-written software artifacts.**



## 🚀 Overview
**StudyWeave** is a full-stack research management system designed to solve the "Black Box" problem of AI code generation. It allows researchers to conduct blinded, side-by-side comparisons of software artifacts (code, UML, test cases) to measure readability, maintainability, and correctness.

Unlike simple survey tools, StudyWeave features a **custom competency engine**, **real-time analytics dashboards**, and **automated AI summarization**, making it a complete lifecycle management tool for software engineering research.

---

## ⚡ Key Features

### 🤖 AI & Intelligence
* **Automated Summarization:** Integrated LLM services to generate textual summaries of study results, allowing researchers to digest complex datasets instantly.
* **Smart Reporting:** Automated generation of professional PDF and CSV reports for offline analysis.

### 📊 Analytics & Visualization
* **Custom SVG Dashboards:** Built a high-performance analytics engine (without external heavy libraries) to render participant competency matrices and study progress in real-time.
* **Anomaly Detection:** Algorithms to flag "speed-running" participants or inconsistent data patterns automatically.

### 🛡️ Security & Architecture
* **Role-Based Access Control (RBAC):** Secure, distinct workflows for **Researchers** (creation), **Participants** (evaluation), and **Reviewers** (adjudication).
* **Study "Time-Travel":** Implemented a snapshot system to track changes in study configurations over time, preventing data corruption during active research.

### 🎨 Advanced UX
* **Customizable Dashboards:** Researchers can rearrange widgets, toggle dark mode, and persist UI preferences (stored via PostgreSQL/LocalStorage).
* **Blinded Evaluation Mode:** A specialized UI that strips author metadata from artifacts to ensure unbiased A/B testing.

---

## 🛠️ Tech Stack

| Domain | Technologies |
| :--- | :--- |
| **Frontend** | React.js, Shadcn UI, Tailwind CSS, Vite |
| **Backend** | Node.js, Express.js, Multer (File Uploads) |
| **Database** | PostgreSQL, Sequelize ORM |
| **Auth & Security** | JWT (JSON Web Tokens), SMTP Email Verification |
| **DevOps** | Docker, GitHub Actions (CI/CD) |

---

## 📸 Screenshots


| **Researcher Dashboard** | **Comparison Interface** |
|:---:|:---:|


---
## 👥 Contributors
- Zaeem Masood Sheikh - Full Stack Architect & Analytics Engine
- Ali Demir
- İsmail Yağız Güven
- Shahin Ibrahimli
- Farrukh Mammadov

