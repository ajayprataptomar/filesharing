# File Sharing API

A sfile-sharing backend built with **FastAPI**, supporting two user roles:

- **Ops User**: Can upload `.docx`, `.pptx`, `.xlsx` files
- **Client User**: Can sign up, verify via email, and securely download files using encrypted URLs
- **Demo of Working Backend (Interactive Swagger UI)** :- 

## 🚀 Features

- Role-based access (Ops / Client)
- File upload validation (only Office docs)
- Encrypted download URLs (client-only access)
- JWT-based authentication
- Email verification system
- MySQL database support
- Dockerized for production deployment

---

## ⚙️ Technologies Used

- **FastAPI** (Python web framework)
- **MySQL** (Relational DB)
- **SQLAlchemy** (ORM)
- **JWT** (Auth tokens)
- **Cryptography / Fernet** (Link encryption)
- **Docker** (Production deployment)
- **Postman** (API testing)

---

## 📦 Setup Instructions
**1. Clone the Repository**
git clone https://github.com/your-username/secure-file-sharing.git
cd secure-file-sharing

**2. Create and Activate Virtual Environment**
# For Linux/macOS
python -m venv venv
source venv/bin/activate

# For Windows
python -m venv venv
venv\Scripts\activate

**3. Install Dependencies**
  pip install -r requirements.txt

**4. Configure Environment Variables**
  Create a .env file in the root directory:

  DATABASE_URL=mysql+mysqlconnector://<username>:<password>@<host>:<port>/<database>
  SECRET_KEY=your-secret-key
  ALGORITHM=HS256
  ACCESS_TOKEN_EXPIRE_MINUTES=30
  BASE_URL=http://localhost:8000

**5. Run the Application Locally**
  uvicorn app.main:app --reload
  Then open your browser or Postman at:

  **http://localhost:8000/docs – (Interactive Swagger UI)**

