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


| **Researcher Dashboard** |
|:---:|
<img width="1652" height="814" alt="Screenshot 2026-01-06 at 4 08 58 PM" src="https://github.com/user-attachments/assets/3570181c-96c9-4dfa-a96e-1255f19453dc" />
<img width="1659" height="783" alt="Screenshot 2026-01-06 at 4 09 12 PM" src="https://github.com/user-attachments/assets/7e22e292-065f-4911-ae3f-bcc18a479ab6" />
<img width="1071" height="759" alt="Screenshot 2026-01-06 at 4 18 50 PM" src="https://github.com/user-attachments/assets/665b55aa-84c5-4c3d-89a8-8d88d77001ce" />

---

## ⚙️ Installation & Configuration
Clone the repo and run *npm install* in both server and client.

##### Backend Setup
1. Navigate to the server directory and install dependencies:

```bash 
cd server
npm install
```

2. Create a .env file in the root directory and configure the following variables:

```bash 
NODE_ENV=development   # Sets the environment (development/production)
PORT=5200              # The port the Express API will listen on

# --- Database Configuration ---
# The application uses individual variables to construct the connection.
DB_HOST=127.0.0.1          # Database server address (localhost)
DB_PORT=5432               # Default PostgreSQL port
DB_NAME=study_weave_db     # The name of your specific database
DB_USER=postgres           # Database username
DB_PASSWORD=postgres       # Database password

# --- Auth / Security ---
JWT_SECRET=change_this_to_a_long_random_string # Used to sign login tokens
# --- Email Services (SMTP) ---
# Required for "Authentication", "Forgot Password" and email notifications.
# Example below uses Mailtrap for testing.
SMTP_HOST=sandbox.smtp.mailtrap.io
SMTP_PORT=2525
SMTP_USER=your_mailtrap_user
SMTP_PASS=your_mailtrap_password
SMTP_SECURE=false
SMTP_FROM=noreply@study_weave.com

# --- CORS & URLs ---
# Defines where the frontend and backend are running to prevent CORS errors.
FRONTEND_URL=http://localhost:5173
BACKEND_URL=http://localhost:5200

# --- AI Integration (Google Gemini) ---
GEMINI_API_KEY=AIzaSy... # Your Google GenAI API Key
GEMINI_LLM_NAME=gemini-2.5-flash # Specific model version (e.g., gemini-1.5-pro or
gemini-2.5-flash)
```
3. Database Initialization

You must build the schema and seed initial data (admin accounts, templates) or you will be unable to log in.

Run the following commands inside the */server* directory:

```bash
# 1. Create tables based on Models
npx sequelize-cli db:migrate

# 2. Populate tables with initial data
npx sequelize-cli db:seed:all
```

4. Frontend Setup

Navigate to the client directory and install dependencies:
```bash 
cd client
npm install
```

## 🚀 Usage
You must run two terminal processes simultaneously

Terminal 1: Start the Backend

```bash 
cd server
npm run dev
```

Terminal 2: Start the Frontend

```bash 
cd client
npm run dev
```

---
## 👥 Contributors
- Zaeem Masood Sheikh - Full Stack Architect & Analytics Engine
- Ali Demir
- İsmail Yağız Güven
- Shahin Ibrahimli
- Farrukh Mammadov

