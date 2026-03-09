# Citizen Issue Reporting Backend

A production-ready **Flask backend** that allows citizens to report civic issues such as potholes, water leaks, garbage problems, and street light failures in Hyderabad. The system helps city workers track and resolve issues quickly through organized complaint management.

---

## Live Demo

Homepage  
```
https://hyderabad-issues.onrender.com
```

View All Issues  
```
https://hyderabad-issues.onrender.com/api/issues
```

View Open Issues  
```
https://hyderabad-issues.onrender.com/api/issues?status=open
```

---

## Demonstration Video

https://drive.google.com/file/d/1u6Jd4Dex37_JUEZH7EKGvzi5fBp6otsF/view?usp=drive_link

---

## Features

- Citizens can report civic problems through mobile apps, WhatsApp, or SMS
- Categories supported:
  - Pothole
  - Water Leak
  - Street Light
  - Garbage
- Issue status tracking from **Open → Resolved**
- Filter issues by:
  - Status
  - Category
- RESTful API for easy integration with mobile applications
- Deployed on **Render.com** for public access

---

## Problem Solved

Many civic issues like potholes or water leaks remain unresolved because there is no simple system to track complaints.

This system allows:
- **Citizens** to report problems easily
- **City workers** to view organized issue lists
- **Authorities** to track and resolve complaints faster

---

## How Citizens Use the System

### Report an Issue

```bash
curl -X POST -H "Content-Type: application/json" \
-d '{"user_id":1,"category_id":1,"title":"Pothole near Charminar","description":"Large pothole causing traffic issues"}' \
https://yourapp.onrender.com/api/issues
```

### View Open Issues

```bash
curl "https://yourapp.onrender.com/api/issues?status=open"
```

---

## Quick Start (Local Setup)

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/citizen-reporting-system.git
cd citizen-reporting-system
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the Application

```bash
python app.py
```

### 4. Test the API

```bash
curl http://127.0.0.1:5000/api/issues
```

Open in browser:

```
http://127.0.0.1:5000
```

---

## Project Structure

```
citizen-reporting-system
│
├── app.py              # Flask backend with API endpoints
├── requirements.txt    # Python dependencies
├── Procfile            # Render deployment configuration
├── issues.db           # SQLite database
└── README.md
```

---

## API Endpoints

| Method | Endpoint | Description |
|------|------|------|
| GET | /api/issues | Get all reported issues |
| GET | /api/issues?status=open | Get only open issues |
| POST | /api/issues | Create a new issue |
| PATCH | /api/issues/<id> | Update issue status |

---

## Issue Categories

```
1 - Pothole
2 - Water Leak
3 - Street Light
4 - Garbage
```

---

## Deployment (Render)

1. Fork or upload this repository to GitHub
2. Go to **https://render.com**
3. Click **New Web Service**
4. Connect your GitHub repository
5. Deploy the application

Your API will be live in a few minutes.

---

## Technology Stack

- **Backend:** Python, Flask
- **Database:** SQLite
- **ORM:** Flask-SQLAlchemy
- **API:** RESTful JSON
- **Deployment:** Render.com

---

## Real World Usage

- Citizens report civic problems using mobile apps or messaging platforms
- Municipal workers monitor issues through API dashboards
- Authorities track resolution time and improve city infrastructure

---

## Author

**Swathi Royal**
