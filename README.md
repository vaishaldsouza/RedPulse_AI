# 🩸 RedPulse AI

**AI-powered blood donation coordination platform connecting donors, recipients, hospitals, and blood banks.**

> "Every Second Matters. AI BloodBridge finds the right donor before time runs out."

---

## 📌 Overview

RedPulse AI is a centralized platform that solves a real, life-critical problem: during medical emergencies, finding compatible blood quickly is difficult because donor information is fragmented across phone calls, social media, and manual hospital records.

The platform connects **donors, recipients, hospitals, and blood banks** in real time, using an intelligent recommendation engine to match donors based on blood group compatibility, eligibility, location, availability, and response history — cutting emergency coordination time from hours to minutes.

---

## 🚨 The Problem

- **118.5M+** blood donations are collected globally every year , yet patients still face delays during emergencies.
- Hospitals rely on manual donor search — phone calls, WhatsApp groups, personal networks.
- No unified system connects donors, hospitals, and blood banks in real time.
- Rare blood groups are especially hard to locate quickly.
- Blood banks have limited real-time visibility into inventory across locations.

---

## 💡 The Solution

RedPulse AI provides:

- **Emergency request posting** — hospitals and blood banks post urgent blood requirements
- **Intelligent donor recommendation** — ranks eligible donors by blood group compatibility, distance, eligibility, and response reliability
- **Real-time notifications** — donors receive instant alerts and can accept/decline
- **Role-based dashboards** — for donors, recipients, hospitals, and blood banks
- **Live geographic heatmap** — visualizes blood demand and donor availability
- **Demand forecasting (prototype)** — flags potential shortages using historical trends
- **Donation history & eligibility tracking** — for safe, reliable donations

---

## 🧠 Why AI Instead of Manual Search?

**Traditional approach:**
Emergency Request → Hospital searches donor list manually → Calls one donor at a time → Slow, unreliable response

**RedPulse AI approach:**
Emergency Request → System scores every eligible donor → Ranks by compatibility, distance & reliability → Instant notification → Fast response

Manual filtering doesn't scale under time pressure — ranking and prioritization matter more than simply having a list of donors.

---

## ⚙️ How It Works

1. Hospital/recipient creates a blood request
2. System interprets urgency level
3. Checks nearby hospitals and inventory
4. Predicts availability *(prototype model)*
5. Ranks best-fit donors
6. Sends emergency notifications
7. Donor accepts/declines in real time
8. Hospital confirms and blood is delivered
9. Donation history and inventory updated

---

## 🌟 Key Features

| Feature | Description |
|---|---|
| Multi-role registration | Donor, Recipient, Hospital, Blood Bank |
| Intelligent donor recommendation | Weighted scoring on compatibility, distance, eligibility, response history |
| Emergency priority classification | Requests tagged Critical / High / Medium / Low |
| Real-time notifications | Instant alerts with accept/decline |
| Role-based dashboards | Manage requests, inventory, and history per role |
| Live heatmap | Geographic view of demand vs. donor availability |
| Demand forecasting (prototype) | Historical trend-based shortage prediction |
| Explainable recommendations | Every donor match comes with a clear reason |
| Rare blood registry | Tracks and protects rare blood-type donor pools |

---

## 🏗️ System Architecture

```
Users
  │
  ▼
React Frontend
  │
  ▼
FastAPI Backend
  ├── Authentication
  ├── Blood Request Service
  ├── Recommendation Engine
  ├── Notification Service
  ├── Heatmap Module
  └── Analytics
  │
  ▼
MongoDB
```

Serves: Hospitals · Blood Banks · Donors · Admin Dashboard

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React.js, Tailwind CSS |
| Backend | FastAPI (Python) |
| Database | MongoDB |
| Intelligence Layer | Python, scikit-learn |
| Maps & Geolocation | Google Maps API |
| Notifications | Firebase Cloud Messaging |
| Authentication | JWT |
| Deployment | Docker |

---

## 📂 Project Structure

```
ai-bloodbridge/
├── backend/
│   ├── app/
│   │   ├── routes/
│   │   ├── models/
│   │   ├── services/
│   │   └── ai_engine/
│   ├── requirements.txt
│   └── main.py
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   └── dashboards/
│   └── package.json
├── docs/
│   └── architecture.md
└── README.md
```


---

## 🚀 Getting Started

### Prerequisites
- Node.js (v18+)
- Python (v3.10+)
- MongoDB (local or Atlas)

### Backend Setup
```bash
cd backend
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate
pip install -r requirements.txt
uvicorn main:app --reload
```

### Frontend Setup
```bash
cd frontend
npm install
npm run dev
```

### Environment Variables
Create a `.env` file in `backend/`:
```
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
MAPS_API_KEY=your_google_maps_api_key
```

---

## 🔒 Security

- JWT-based authentication
- Role-based access control (RBAC)
- Encrypted communication over HTTPS
- Audit logs for request/response tracking

---

## 🗺️ Roadmap

- [x] Core donor-hospital matching engine
- [x] Real-time notifications
- [x] Role-based dashboards
- [ ] Live heatmap integration
- [ ] Demand forecasting with real historical data
- [ ] Multilingual support
- [ ] Wearable device integration
- [ ] Government healthcare system integration (e-RaktKosh, ABHA)

---

## 👥 Team

| Name | Role |
|---|---|
| Senona Jenisha Pereira | Frontend Development |
| Vaishal Dsouza | Backend & Database |
| Jessel Ruby Crasta | Intelligence Layer / Matching Logic |
| Melriya Smitha Gonsalves | UI/UX & Presentation |

---

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

*"One donation can save three lives. One smart platform can save thousands."*
```
