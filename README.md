**Citizen Issue Reporting Backend**

A production-ready Flask backend for citizens to report civic issues like potholes, water leaks, and street lights in Hyderabad.

## **Live Demo**
```
https://hyderabad-issues.onrender.com           ← Homepage
https://hyderabad-issues.onrender.com/api/issues ← All complaints
https://hyderabad-issues.onrender.com/api/issues?status=open ← Urgent issues
```
## **Demonstration Video**
https://drive.google.com/file/d/1u6Jd4Dex37_JUEZH7EKGvzi5fBp6otsF/view?usp=drive_link

## **Features**
- Citizen reporting via mobile apps, WhatsApp, SMS
- Categories: Pothole, Water Leak, Street Light, Garbage
- Status tracking: Open → Resolved with timestamps
- Filter: `?status=open` or `?category=1`
- Production deployed on render.com (free 24/7)

## **Problem Solved**
Citizens report potholes/water leaks → City workers see organized lists → Issues get fixed faster.

## **How Citizens Use It**

```bash
# Mobile app sends:
curl -X POST -H "Content-Type: application/json" \
-d '{"user_id":1,"category_id":1,"title":"Pothole Charminar","description":"Big hole"}' \
https://yourapp.onrender.com/api/issues
```

```bash
# City worker views open issues:
curl "https://yourapp.onrender.com/api/issues?status=open"
```

## **Quick Start (Local)**

```bash
# 1. Clone & Install
git clone <your-repo>
cd citizen-reporting-system
pip install -r requirements.txt

# 2. Run
python app.py

# 3. Test
curl http://127.0.0.1:5000/api/issues
```

**Homepage:** `http://127.0.0.1:5000`

## **File Structure**
```
├── app.py              # Flask backend + API endpoints
├── requirements.txt    # Python packages
├── Procfile           # Render deployment
├── issues.db          # SQLite database (3 test issues)
└── README.md          # This file
```

## **API Endpoints**

| Method | URL | Description |
|--------|-----|-------------|
| `GET` | `/api/issues` | List all issues |
| `GET` | `/api/issues?status=open` | Open issues only |
| `POST` | `/api/issues` | Report new issue |
| `PATCH` | `/api/issues/1` | Update status |

## **Categories**
```
1 = Pothole 
2 = Water Leak 
3 = Street Light 
4 = Garbage 
```

## **Deploy to Render (Free)**

1. Fork this repo
2. [render.com](https://render.com) → New Web Service
3. Connect GitHub repo
4. Deploy → **Live in 2 minutes!**

## **Tech Stack**
```
Backend: Python + Flask
Database: SQLite
ORM: Flask-SQLAlchemy
Hosting: Render.com (free)
API: RESTful JSON
```

## **Demo Video Structure**
```
1. CMD: python app.py
2. Browser: localhost:5000 → Homepage
3. Click "View All Issues" → 3 potholes shown
4. Deploy render.com → Live URL demo
```

## **Real-World Usage**
- **Citizens:** Mobile apps/WhatsApp/SMS report issues
- **Workers:** Browser dashboard filters urgent complaints  
- **Analytics:** Track resolution times by category/ward

## **License**
MIT License - Free for commercial use.

***

**Report potholes → Fix streets → Cleaner city!**
