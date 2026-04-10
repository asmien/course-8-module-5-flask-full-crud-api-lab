# Flask Full CRUD API - Event Management

## 📌 Overview

This project is a simple RESTful API built using Flask. It simulates an event management system where users can create, read, update, and delete events.

The application uses in-memory data (a Python list) instead of a database.

---

## ⚙️ Technologies Used

* Python 3
* Flask

---

## 🚀 Setup Instructions

### 1. Clone the repository

```bash
git clone <your-repo-url>
cd <your-repo-name>
```

### 2. Install dependencies

```bash
pip install flask
```

### 3. Run the application

```bash
python app.py
```

The server will start at:

```
http://127.0.0.1:5000/
```

---

## 📡 API Endpoints

### 🔹 GET /

Returns a welcome message.

**Response:**

```json
{
  "message": "Welcome to the Event API"
}
```

---

### 🔹 GET /events

Returns all events.

**Response:**

```json
[
  { "id": 1, "title": "Tech Meetup" },
  { "id": 2, "title": "Python Workshop" }
]
```

---

### 🔹 POST /events

Creates a new event.

**Request Body:**

```json
{
  "title": "Hackathon"
}
```

**Response (201 Created):**

```json
{
  "id": 3,
  "title": "Hackathon"
}
```

---

### 🔹 PATCH /events/<id>

Updates an event’s title.

**Request Body:**

```json
{
  "title": "Updated Event"
}
```

**Response (200 OK):**

```json
{
  "id": 1,
  "title": "Updated Event"
}
```

---

### 🔹 DELETE /events/<id>

Deletes an event.

**Response (200 OK):**

```json
{
  "message": "Event deleted"
}
```

---

## ❗ Error Handling

### Missing Title

```json
{
  "error": "Title is required"
}
```

Status Code: 400

### Event Not Found

```json
{
  "error": "Event not found"
}
```

Status Code: 404

---

## 🧪 Testing

You can test the API using:

* Postman
* curl
* Browser (for GET requests)

---

## 📝 Notes

* Data is stored in memory and resets when the server restarts.
* The API follows RESTful conventions.
* Status codes are used correctly (200, 201, 400, 404).

---

## ✅ Features Implemented

* Create event (POST)
* Read events (GET)
* Update event (PATCH)
* Delete event (DELETE)
* Input validation
* Error handling

---

## 📚 Future Improvements

* Add a real database (e.g., SQLite, PostgreSQL)
* Add authentication
* Improve structure using Flask Blueprints
* Add more fields (date, location, description)

---
