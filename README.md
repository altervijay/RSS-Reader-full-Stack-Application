# 📰 Node-RED RSS Reader with Keyword Monitor

This project is a complete RSS Feed monitoring system built using [Node-RED](https://nodered.org/). It can fetch RSS feeds, match them against dynamic keywords from a database, and notify you based on matches. It also includes a REST API interface and a simple admin panel for managing feeds and keywords.

---

## 📌 Features

✅ Scheduled RSS Feed fetching  
✅ Keyword filtering using DB expressions  
✅ Dynamic database-driven matching  
✅ Admin interface for creating/dropping feeds, keywords, and matches  
✅ REST API for monitoring and debugging  
✅ Easy to import and customize Node-RED flows

---

## 🧠 Project Architecture

The project is divided into **3 main flows**:

### 🔹 `rss reader`
Handles:
- Fetching RSS feed URLs from DB
- Reading feeds using HTTP requests
- Parsing and filtering articles via keywords
- Storing matched articles into the database
- Notifications (customizable)

### 🔹 `db-admin`
Admin panel flow to:
- Create or drop tables: `feed`, `keyword`, `match`
- Manage database schema for monitoring feeds and keywords

### 🔹 `renata`
REST-based API interface to:
- Insert/delete feeds or keywords
- Monitor feeds and keywords via HTTP GET/POST
- Connect external apps via endpoints like:
  - `/monitor/feed`
  - `/monitor/keyword`
  - `/monitor`

---

## 📂 Folder Structure


---

## 🖼️ Screenshots

### 🧩 RSS Reader Flow
![RSS Reader Flow](assets/screenshots/rss-reader.png)

### 🧩 DB Admin Flow
![DB Admin](assets/screenshots/db-admin.png)

### 🧩 API Monitor Flow (`renata`)
![Renata](assets/screenshots/renata.png)

---

## 📽️ Demo

Watch the video demo of the full system:  
**[▶️ Demo Video](assets/demo.mp4)**

---

## 🚀 Getting Started

### 🔧 Prerequisites
- Node-RED installed locally (`npm install -g node-red`)
- A SQLite (or compatible) DB with tables: `feed`, `keyword`, `match`
- Basic understanding of flows and JSON import/export in Node-RED

### ⬇️ Import Flows
1. Open your Node-RED editor
2. Go to Menu → Import → Clipboard
3. Copy contents of JSON files in `flows/` folder
4. Deploy the flows

---

## 📡 REST API Examples

- **Get Feeds**: `GET /monitor/feed`
- **Add Feed**: `POST /monitor/feed`
- **Delete Feed**: `GET /monitor/feed/delete/:rowid`

- **Get Keywords**: `GET /monitor/keyword`
- **Add Keyword**: `POST /monitor/keyword`
- **Delete Keyword**: `GET /monitor/keyword/delete/:rowid`

- **Monitor View**: `GET /monitor`

---

## 📃 License

This project is open-sourced for educational and automation purposes. Add your preferred license here (MIT, Apache 2.0, etc).

---

## 🙌 Author

Built with ❤️ using Node-RED by VIJAY BHARDWAJ  
[GitHub Profile](https://github.com/altervijay)

---

