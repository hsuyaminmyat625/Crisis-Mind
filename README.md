# CrisisMind

> A multilingual crisis alert and information system designed to detect, notify, and support users during natural disasters or emergencies.

## 🚀 Overview

**CrisisMind** is a Python-based application that combines real-time disaster data, geolocation, and multilingual AI to deliver crisis notifications and guidance in accessible formats. It is especially focused on regions with low alert infrastructure, such as Myanmar and Southeast Asia.

---

## Key Features

- Multilingual notifications using Hugging Face pretrained models
- Location-based alerts with Map APIs
- RESTful API for disaster info and user data
- SMS, LINE, or email push integration (Twilio, Firebase, etc.)
- Optional AI chatbot for crisis Q&A (offline/online modes)

---

## 🛠️ Tech Stack

| Layer        | Tech Used                |
|-------------|--------------------------|
| Backend API | Python + FastAPI / Flask |
| NLP         | Hugging Face Transformers |
| Data Source | Public Crisis APIs (JMA, USGS, GDACS) |
| Database    | SQLite / PostgreSQL      |
| Geolocation | OpenStreetMap / Leaflet  |
| Notification| Twilio, LINE API, Email  |
| Deployment  | Render / Railway / Docker |

---

## 🔗 API Endpoints

| Method | Endpoint               | Description                       |
|--------|------------------------|-----------------------------------|
| GET    | `/alerts/nearby`       | Get alerts by user geolocation    |
| POST   | `/user/register`       | Register a new user               |
| POST   | `/user/location`       | Update user’s location            |
| POST   | `/translate`           | Translate message for user locale |
| GET    | `/chatbot/ask`         | Crisis Q&A bot (optional)         |

---

## 📦 Installation

```bash
git clone https://github.com/yourname/crisismind.git
cd crisismind
pip install -r requirements.txt
uvicorn main:app --reload  # (if using FastAPI)
```

---

## Project Structure

```
crisismind/
│
├── app/
│   ├── main.py           # Entry point
│   ├── models.py         # DB models
│   ├── routers/
│   │   ├── alerts.py     # Alert endpoints
│   │   ├── users.py      # User endpoints
│   │   └── translate.py  # Translation endpoints
│   ├── services/
│   │   ├── geo.py        # Geolocation logic
│   │   ├── notify.py     # Notification logic
│   │   └── nlp.py        # NLP/AI logic
│   └── utils/
│       └── logger.py     # Logging
├── data/
│   └── sample_alerts.json
├── requirements.txt
├── .env
└── README.md
```

---

## ⚙️ Configuration

1. Copy `.env.example` to `.env`
2. Fill in your API keys, secrets, and config variables.

---

## Contributing

Contributions, issues and feature requests are
