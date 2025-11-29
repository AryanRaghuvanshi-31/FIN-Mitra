# FIN-Mitra
This project combines FinTech, Hyperledger Fabric, AI/ML, SMS automation, and multilingual UX to deliver a complete digital-finance assistant.
<p align="center">
  <img src="https://img.shields.io/badge/Fin--Mitra%20%7C%20Micro%20Moves,%20Macro%20Impact-0A1A44?style=for-the-badge&logoColor=white" alt="Fin-Mitra Banner"/>
</p> 

---------------

📌 Table of Contents
-

• Introduction  
• Problem Statement  
• Key Features  
• Architecture Overview  
• Tech Stack  
• System Workflow  
• Setup Instructions  
• API Endpoints  
• Blockchain (Hyperledger) Integration  
• Screenshots  
• Future Enhancements

-----
🧭 Introduction
-
Fin-Mitra is a modern FinTech application that targets a major gap:
managing micro-expenses and debt for India’s youth.

People often lose track of small, daily payments (₹10–₹100) which add up to large monthly losses.
Traditional banking apps do not analyse micro-spending, debt optimization, or provide personalised budgeting insights.

Fin-Mitra solves this with:

✔ AI-based insights
✔ Multilingual support
✔ Debt optimization
✔ Micro-payment SMS analysis
✔ Blockchain-secured data storage

----
❗ Problem Statement
-

A large portion of India’s young population lacks access to automated financial tools that help with:

- Micro-payments and leakage spending
- Confusion about budgeting rules
- Difficulty deciding which loan to close first
- No privacy-friendly SMS-based trackers
- No personalised saving recommendations
- Limited financial literacy


Fin-Mitra addresses these issues using smart automation, machine learning, and Hyperledger Fabric for secure storage.

-----
⭐ Key Features
-

1️⃣ Micro-Payment Tracking

- Automatically fetches SMS alerts from UPI apps
- Categorises small spends (food, chai, autos, snacks)
- Highlights “invisible expenses” that drain your money
- Provides real-time dashboards

2️⃣ Smart Budgeting (AI-Driven)

- Supports budgeting rules like 50-30-20, 20-40-30, and custom AI-based rules
- Provides monthly saving insights
- Sends alerts for overspending
- Delivers simple, vlog-style money tips


3️⃣ Debt Management Engine

- EMI, interest, and tenure calculator
- Recommends the best loan to pay first
- Shows interest saved if user pays ₹500–₹1000 extra
- Step-by-step payoff strategies


4️⃣ Blockchain-Powered Privacy (Hyperledger Fabric)

Stores sensitive SMS logs and metadata securely

Tamper-proof audit trail

Off-chain encrypted storage + on-chain hash

Ensures user’s financial data is never leaked

5️⃣ Multilingual Support

Hindi

English

Marathi

Punjabi

6️⃣ AI Chatbot Assistant
- Explains your spending patterns
- Recommends which category to cut
- Helps reduce debt faster
- Provides financial education in simple language


--------
🏗️ Architecture Overview
--
User Phone (SMS)  
      ↓  
Android App (Reads SMS via consent API)  
      ↓  
Encrypt Payload → Upload to Off-Chain Storage (MongoDB / IPFS)  
      ↓  
SHA-256 Hash → Hyperledger Fabric Smart Contract  
      ↓  
Backend API (Flask / FastAPI)  
      ↓  
React Web Dashboard  


✔ Off-chain: encrypted transaction details
✔ On-chain: immutable hash + metadata


## 🎨 Frontend Tech Stack (React Web)

| Technology | Badge | Purpose |
|-----------|--------|---------|
| **React.js** | ![React](https://img.shields.io/badge/React-61DAFB.svg?style=for-the-badge&logo=react&logoColor=black) | UI rendering, component structure |
| **Tailwind CSS** | ![Tailwind](https://img.shields.io/badge/TailwindCSS-38BDF8.svg?style=for-the-badge&logo=tailwindcss&logoColor=white) | Modern utility-first styling |
| **Recharts** | ![Recharts](https://img.shields.io/badge/Recharts-FF6384.svg?style=for-the-badge&logo=chart.js&logoColor=white) | Visual charts for insights |
| **JavaScript (ES6+)** | ![JS](https://img.shields.io/badge/JavaScript-F7DF1E.svg?style=for-the-badge&logo=javascript&logoColor=black) | Dashboard logic |
| **npm** | ![npm](https://img.shields.io/badge/npm-CB3837.svg?style=for-the-badge&logo=npm&logoColor=white) | Package management |

## 🛠️ Backend Tech Stack (Flask API)

| Technology | Badge | Purpose |
|-----------|--------|---------|
| **Python** | ![Python](https://img.shields.io/badge/Python-3776AB.svg?style=for-the-badge&logo=python&logoColor=yellow) | Core backend logic |
| **Flask** | ![Flask](https://img.shields.io/badge/Flask-000000.svg?style=for-the-badge&logo=flask&logoColor=white) | API server for Fin-Mitra |
| **Flask-CORS** | ![CORS](https://img.shields.io/badge/CORS-4B5563.svg?style=for-the-badge&logo=fastapi&logoColor=white) | Cross-origin (React ↔ Flask) |
| **SQLite** | ![SQLite](https://img.shields.io/badge/SQLite-003B57.svg?style=for-the-badge&logo=sqlite&logoColor=white) | Local development DB |
| **MongoDB (Off-chain)** | ![MongoDB](https://img.shields.io/badge/MongoDB-47A248.svg?style=for-the-badge&logo=mongodb&logoColor=white) | Stores encrypted SMS blobs (off-chain) |
| **IPFS (Optional)** | ![IPFS](https://img.shields.io/badge/IPFS-65C2CB.svg?style=for-the-badge&logo=ipfs&logoColor=white) | Decentralized off-chain storage |
| **AWS S3 (Optional)** | ![S3](https://img.shields.io/badge/AWS%20S3-569A31.svg?style=for-the-badge&logo=amazonaws&logoColor=white) | Secure encrypted file storage |

## 🔐 Blockchain & Security Stack

| Technology | Badge | Purpose |
|-----------|--------|---------|
| **Hyperledger Fabric** | ![Fabric](https://img.shields.io/badge/Hyperledger%20Fabric-2F3134.svg?style=for-the-badge&logo=linux-foundation&logoColor=white) | Permissioned blockchain for integrity |
| **Private Data Collections (PDCs)** | ![Private](https://img.shields.io/badge/Private%20Data%20Collections-111827.svg?style=for-the-badge&logo=databricks&logoColor=white) | Store encrypted SMS privately |
| **Transient Fields** | ![Transient](https://img.shields.io/badge/Transient%20Map-6B7280.svg?style=for-the-badge&logo=apachekafka&logoColor=white) | Secure private values during tx |
| **SHA-256 Hashing** | ![SHA256](https://img.shields.io/badge/SHA--256-1E40AF.svg?style=for-the-badge&logo=apache&logoColor=white) | Tamper-proof record hashing |
| **AES-256 Encryption** | ![AES](https://img.shields.io/badge/AES--256-10B981.svg?style=for-the-badge&logo=verizon&logoColor=white) | Encrypt SMS payloads |
| **RSA Public/Private Keys** | ![RSA](https://img.shields.io/badge/RSA--2048-DC2626.svg?style=for-the-badge&logo=letsencrypt&logoColor=white) | Secure key-based encryption |

## 📱 Mobile (Android) Tech Stack

| Technology | Badge | Purpose |
|-----------|--------|---------|
| **Android (Java / Kotlin)** | ![Android](https://img.shields.io/badge/Android-3DDC84.svg?style=for-the-badge&logo=android&logoColor=white) | Mobile app for SMS reading |
| **SMS User Consent API** | ![SMS](https://img.shields.io/badge/SMS%20Consent%20API-34A853.svg?style=for-the-badge&logo=google&logoColor=white) | Read UPI SMS securely |
| **Retrofit** | ![Retrofit](https://img.shields.io/badge/Retrofit-20232A.svg?style=for-the-badge&logo=square&logoColor=white) | Upload parsed SMS to backend |
| **Room Database** | ![Room](https://img.shields.io/badge/Room%20DB-6D28D9.svg?style=for-the-badge&logo=sqlite&logoColor=white) | Local caching of SMS records |

## 🤖 AI/ML Tech Stack

| Technology | Badge | Purpose |
|-----------|--------|---------|
| **Python ML** | ![ML](https://img.shields.io/badge/Machine%20Learning-2563EB.svg?style=for-the-badge&logo=pytorch&logoColor=white) | Smart tagging & insights |
| **NLP** | ![NLP](https://img.shields.io/badge/NLP-9333EA.svg?style=for-the-badge&logo=google&logoColor=white) | Understand SMS text |
| **Scikit-learn** | ![sklearn](https://img.shields.io/badge/Scikit--Learn-F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white) | Train classifiers |
| **Custom Rule Engine** | ![Rules](https://img.shields.io/badge/Rule--Engine-4B5563.svg?style=for-the-badge&logo=apache&logoColor=white) | Budgeting & debt recommendations |

## ⚙️ Developer Tools

| Tool | Badge | Purpose |
|------|--------|---------|
| **Git / GitHub** | ![GitHub](https://img.shields.io/badge/GitHub-181717.svg?style=for-the-badge&logo=github&logoColor=white) | Version control |
| **VS Code** | ![VS Code](https://img.shields.io/badge/VS%20Code-007ACC.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white) | Development |
| **Postman** | ![Postman](https://img.shields.io/badge/Postman-FF6C37.svg?style=for-the-badge&logo=postman&logoColor=white) | API testing |
| **Node.js** | ![Node](https://img.shields.io/badge/Node.js-339933.svg?style=for-the-badge&logo=node.js&logoColor=white) | Frontend tooling |

## 🧩 Combined Tech Stack Summary

| Layer | Technologies |
|-------|--------------|
| **Frontend** | React, Tailwind, Recharts |
| **Backend** | Flask, SQLite, MongoDB |
| **Blockchain** | Hyperledger Fabric, PDCs, SHA-256 |
| **Mobile** | Android (SMS Consent API), Retrofit |
| **AI Engine** | Python, Scikit-learn, NLP |
| **Security** | AES-256, RSA, Encrypted Off-chain |
| **Tools** | GitHub, VS Code, Postman, Node.js |

----------------------
🔄 System Workflow – Fin-Mitra
-

1️⃣ User Authentication
-

User logs in via React.js Web App or Android App.

Login request → Flask Backend API.

JWT token is issued for secure session flow.

2️⃣ Micro-Payment Capture (Android App)
-

Android app reads UPI transactional SMS in real-time.

SMS content is AES-256 encrypted on-device.

Encrypted payload → sent to Flask backend via HTTPS.

3️⃣ Backend SMS Processing

Backend decrypts SMS.

NLP-based parser extracts:

Merchant

Amount

UPI ID

Category

Timestamp

Expense is classified as:

Essential

Non-Essential

Micro-Payment (< ₹200)

4️⃣ Smart Budget Engine

Aggregates monthly income & categorized expenses.

Applies budgeting rules:

20-40-30,

50-30-20,

OR personalized strategy.

Generates insights on:

Overspending

Ideal saving targets

Monthly limits

5️⃣ Smart Debt Engine

Takes loan amount, interest rate, tenure, monthly savings.

Suggests:
✔ Which loan to repay first (highest ROI)
✔ Strategies inspired by finance influencers
✔ Impact of prepayments (reduced interest + tenure)

6️⃣ Blockchain Hashing (Hyperledger Fabric)

Only hashed transaction records are stored on-chain.

Full expense data stays encrypted off-chain in Flask DB.

Ensures:
🔐 Data integrity
🔐 Privacy
🔐 Tamper-proof logs

7️⃣ Web Dashboard

React frontend fetches user financial summary:

Expenses

SMS insights

Debt reduction tips

Budget health

Charts & analytics are rendered in:

Recharts

Chart.js

8️⃣ User Views Insights

Monthly graphs

Category-wise spend

Micro-payment heatmap

Debt payoff forecast

Smart alerts & recommendations

⚙️ Setup Instructions
-
Backend (Flask)
-

🔗 1. Clone the Repository

gitclone <repository-url>
Cd Fin-Mitra

Backend (Flask)
<img width="325" height="72" alt="image" src="https://github.com/user-attachments/assets/2d288763-0f85-4c5c-8dec-0f8443ef0c78" />

Test API:
<img width="295" height="45" alt="image" src="https://github.com/user-attachments/assets/831c92d6-6422-48eb-a970-16fc64540054" />

Frontend (React)
<img width="351" height="98" alt="image" src="https://github.com/user-attachments/assets/cb4f57de-5cda-4937-9505-2c1ff50deed0" />

📡 API Endpoints
| Method | Endpoint      | Description            |
| ------ | ------------- | ---------------------- |
| GET    | `/ping`       | Health check           |
| POST   | `/auth/login` | Login                  |
| POST   | `/upload_sms` | Upload UPI SMS         |
| GET    | `/expenses`   | List user expenses     |
| GET    | `/verify/:id` | Verify blockchain hash |
| DELETE | `/delete/:id` | Delete expense         |

🔐 Blockchain (Hyperledger) Integration
-
✔ Off-Chain

Encrypted SMS data stored in:

MongoDB 
✔ On-Chain

Fabric stores:

hash

timestamp

pointer (CID/URL)

payer address

minimal metadata

✔ Smart Contract Functions

SubmitHash(key, payload)

ReadTxn(key)


✔ Security Model

Private Data Collections

Transient fields for sensitive data

No plaintext SMS is ever stored on-chain

 ----
🖼️ Screenshots
-
![11](https://github.com/user-attachments/assets/4f9f0255-2310-4139-bc08-a341578c77db)


![1222](https://github.com/user-attachments/assets/63e4f1a8-1770-422f-a0bd-ea590ec30c94)


![13](https://github.com/user-attachments/assets/b89b5bac-bf85-4418-8d9d-0d97b9e83f7e)


![WhatsApp Image 2025-11-29 at 10 06 41_127802a0](https://github.com/user-attachments/assets/940a43e7-c3db-4318-ab0f-f72fb37c8182)



![WhatsApp Image 2025-11-29 at 10 07 02_13a4804d](https://github.com/user-attachments/assets/924d2edb-6155-404d-8407-5ee8d5d92dd1)




MOBILE APP
-


![WhatsApp Image 2025-11-29 at 10 17 57_080d2389](https://github.com/user-attachments/assets/c802a95c-d6bd-498c-a291-dbb0b9d4cfaa)



![WhatsApp Image 2025-11-29 at 10 21 12_2c6f770b](https://github.com/user-attachments/assets/9c471051-3062-48ec-be10-b00a6d0e1483)




![WhatsApp Image 2025-11-29 at 10 21 13_1dcb2ca1](https://github.com/user-attachments/assets/55c36cfe-dfc9-4009-976b-5cf8c2ac1552)




![WhatsApp Image 2025-11-29 at 10 21 13_cb03cdc5](https://github.com/user-attachments/assets/a0aafe3e-99e5-4033-8c96-fe60a5473427)



![WhatsApp Image 2025-11-29 at 10 21 14_75ac0870](https://github.com/user-attachments/assets/c08688fe-19c5-43b6-b2f5-a213822ac657)




![WhatsApp Image 2025-11-29 at 10 21 14_29f4507b](https://github.com/user-attachments/assets/7d17579c-0b73-4735-aafb-b7a78e4d236c)




------------
🚀 Future Enhancements
-

OCR on bank PDFs

Account Aggregator integration (AA Framework)

Credit-score analysis

Auto-sync with UPI apps

Loan recommendation algorithm


---------

Project Demo
-
URL :- 


APPLICATION URL :- https://fin-mitra--raryann31.replit.app





