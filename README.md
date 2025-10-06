# 🗞️ News Aggregator Web Application

A full-stack **News Aggregator** that scrapes, stores, and displays news articles from *naftemporiki.gr*.  
The project includes a **React + Vite** front-end and a **Flask + MongoDB** back-end.

---

## 📖 Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Architecture](#architecture)
- [Installation](#installation)
- [Front-End Setup](#front-end-setup)
- [Back-End Setup](#back-end-setup)
- [API Endpoints](#api-endpoints)
- [Technologies Used](#technologies-used)
- [Future Improvements](#future-improvements)
- [License](#license)

---

## 🧠 Project Overview

This application automatically **scrapes news articles** from the *Naftemporiki* website,  
stores them in a **MongoDB database**, and presents them through a clean and responsive **React** interface.

Users can:
- View the latest scraped news
- Filter or browse articles
- Trigger data scraping through backend endpoints

---

## ✨ Features

### 🔍 Back-End
- Built with **Flask**
- Scrapes live data from [naftemporiki.gr](https://www.naftemporiki.gr/)
- Stores news in a **MongoDB Atlas** database
- Provides RESTful API endpoints
- CORS enabled for React frontend

### 🖥️ Front-End
- Built with **React + Vite**
- Organized in pages (`HomePage`, `Dashboard`, `Login`, `News`)
- Reusable components (`Navbar`, `Sidebar`, `CardList`)
- Fetches and displays articles from the backend API

---

## 🏗️ Architecture

