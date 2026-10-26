# Notes CRUD API

A simple REST API built with FastAPI and SQLite to handle basic note management (Create, Read, Update, Delete).

## 1. Environment Setup

Create and activate a virtual environment in terminal:

**macOS / Linux:**
```bash
python3 -m venv .venv
source .venv/bin/activate
```
## 2. Installing Packages

python -m pip install -r requirements.txt

## 3. Running API

uvicorn main:app --reload

## API Endpoints & Expected Output
| Action | Method | Endpoint | Description | Expected Status |
|---|---|---|---|---|
| Read home | `GET` | `/` | Returns API status message | `200 OK` |
| Read all notes | `GET` | `/notes` | Retrieves all notes | `200 OK` |
| Read a note | `GET` | `/notes/{note_id}` | Retrieves note by ID | `200 OK` |
| Create a note | `POST` | `/notes` | Creates a new note with title and text | `201 Created` |
| Update a note | `PATCH` | `/notes/{note_id}` | Updates selected fields of a note | `200 OK` |
| Delete a note | `DELETE` | `/notes/{note_id}` | Deletes note by ID | `200 OK` |
| Missing note test | `GET / PATCH / DELETE` | `/notes/9999` | Returns error for non-existent note | `404 Not Found` |
| Validation test | `POST` | `/notes` | Missing required fields | `422 Unprocessable Entity` |
