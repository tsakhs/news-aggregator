# 🗞️ News Aggregator Web Application

A full-stack **News Aggregator** that automatically scrapes and displays news articles from multiple Greek sources such as **Naftemporiki** and **Kathimerini**.  
The project combines a **React + Vite** front-end and a **Flask + MongoDB** back-end to deliver real-time, structured, and easily accessible news content.

---

## 📖 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Installation](#installation)
- [Front-End Setup](#front-end-setup)
- [Back-End Setup](#back-end-setup)
- [API Endpoints](#api-endpoints)
- [Database Structure](#database-structure)
- [Technologies Used](#technologies-used)
- [Future Improvements](#future-improvements)
- [License](#license)
- [Summary](#summary)

---

## 🧠 Overview

The **News Aggregator** collects, organizes, and stores news articles from Greek online media outlets,  
allowing users to view, analyze, and manage them via a clean web interface.

The system:
- Scrapes live data from *Naftemporiki* and *Kathimerini*
- Saves articles to a **MongoDB Atlas** database
- Exposes a RESTful API with CRUD functionality
- Displays news dynamically in a **React** front-end

---

## ✨ Features

### 🔍 Back-End
- Built with **Flask**
- Scrapes data using **BeautifulSoup** and **Requests**
- Integrates with **MongoDB Atlas**
- RESTful endpoints for CRUD operations
- CORS-enabled for frontend interaction

### 🖥️ Front-End
- Developed using **React + Vite**
- Pages: `HomePage`, `Dashboard`, `Login`, `News`
- Components: `Navbar`, `Sidebar`, `CardList`
- Fetches and displays news from the backend API
- Responsive design with clean UI

---

## 🏗️ Architecture

```
Frontend (React + Vite)
       ↓
Backend (Flask REST API)
       ↓
Database (MongoDB Atlas)
```

- **Front-End:** Handles the user interface and data visualization.  
- **Back-End:** Manages scraping, data persistence, and API routing.  
- **Database:** Stores scraped articles with metadata (title, date, source, etc.).

---

## ⚙️ Installation

### 1️⃣ Clone the repository
```bash
git clone https://github.com/your-username/news-aggregator.git
cd news-aggregator
```

### 2️⃣ Extract project files
```bash
unzip FE.zip
unzip BE.zip
```

---

## 💻 Front-End Setup

```bash
cd FE
npm install
npm run dev
```

By default, the app will run at **http://localhost:5173**

---

## 🧠 Back-End Setup

```bash
cd BE
python -m venv venv
source venv/bin/activate   # macOS/Linux
venv\Scripts\activate      # Windows

pip install Flask Flask-PyMongo requests beautifulsoup4 pandas lxml flask-cors
python app.py
```

The Flask API will run at **http://localhost:5000**

---

## 🔌 API Endpoints

### 📰 Naftemporiki News

| Endpoint | Method | Description |
|-----------|--------|-------------|
| `/scrape?start=1&end=3` | GET | Scrapes news articles from Naftemporiki pages (1–3) |
| `/news` | GET | Retrieves all stored Naftemporiki news |
| `/news` | POST | Adds a new Naftemporiki news article |
| `/news/<news_id>` | PUT | Updates an existing article |
| `/news/<news_id>` | DELETE | Deletes a specific article |

### 🗞️ Kathimerini News

| Endpoint | Method | Description |
|-----------|--------|-------------|
| `/scrape_kathimerini` | GET | Scrapes news articles from Kathimerini |
| `/news_kathimerini` | GET | Retrieves all stored Kathimerini news |
| `/news_kathimerini` | POST | Adds a new Kathimerini article |
| `/news_kathimerini/<news_id>` | PUT | Updates an existing article |
| `/news_kathimerini/<news_id>` | DELETE | Deletes a specific article |

---

## 🗂️ Database Structure

Each article is stored as a document in MongoDB:

```json
{
  "_id": ObjectId,
  "title": "Article title",
  "date": "YYYY-MM-DD",
  "url": "https://example.com/article",
  "source": "Naftemporiki" | "Kathimerini"
}
```

Collections:
- `news` — for Naftemporiki articles  
- `news_kathimerini` — for Kathimerini articles

---

## 🧩 Technologies Used

**Front-End**
- React
- Vite
- JavaScript (ES6+)
- CSS Modules

**Back-End**
- Flask
- Flask-PyMongo
- Requests
- BeautifulSoup4
- Pandas
- lxml
- Flask-CORS

**Database**
- MongoDB Atlas

---

## 🚀 Future Improvements

- Add scheduled scraping using **Celery** or **Cron jobs**
- User authentication (JWT)
- Advanced search and filtering
- Sentiment analysis of news content
- Dockerize front-end and back-end
- Deployment via GitHub Actions or CI/CD
- Real-time updates with WebSockets

---

## 💡 Summary

This **News Aggregator** serves as a full-stack demonstration of web scraping, REST API development,  
database integration, and modern front-end design — providing a strong base for data-driven media projects.
