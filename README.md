# 🔒 Flask User Authentication System
This project is a secure Flask-based user authentication system. It allows users to register, log in, and access protected content. Additional features include password hashing for security and session management via Flask-Login.
## 📋 Features
- Home Page (/): Displays a landing page with options to register or log in.
- Registration (/register): Allows new users to create an account with a hashed password for security.
- Login (/login): Authenticates users and grants access to protected pages.
- Protected Page (/secrets): Accessible only to logged-in users.
- File Download (/download): Lets logged-in users download files securely.
- Logout (/logout): Logs out the user and redirects them to the homepage.
## 🛠️ Prerequisites
Make sure you have the following installed:
- Python 3.x
- Flask
- Flask-Login
- Flask-SQLAlchemy
- Werkzeug
## 📦 Installation
1. Clone the repository:
```bash
git clone <repository-url>
cd <project-directory>
```
2. Install the required dependencies: On Windows:
```bash
python -m pip install -r requirements.txt
```
On MacOS/Linux:
```bash
pip3 install -r requirements.txt
```
3. Initialize the database:
```bash
python main.py
```
## 🚀 How to Run
1. Start the Flask server:
```bash
python main.py
```
2. Open your browser and navigate to:
```arduino
http://127.0.0.1:5000
```
## 🖊️ Usage
- Register: Visit /register to create a new account.
- Login: Use /login to access your account.
- Secrets Page: Navigate to /secrets after logging in to view protected content.
- File Download: Go to /download to securely download the file (e.g., cheat_sheet.pdf).
- Logout: Use /logout to log out of the current session.
## 🗄️ Database Details
- Database: SQLite (users.db)
- Table: User
- Columns:
  - id (Primary Key)
  - email (Unique)
  - password (Hashed)
  - name
## 🛡️ Security Features
- Password Hashing: Uses werkzeug.security.generate_password_hash for hashing passwords with PBKDF2-SHA256 and a salt length of 8.
- Session Management: Flask-Login ensures secure session handling and access restriction for protected routes.
## 🎨 Customization
- Update HTML templates (index.html, register.html, login.html, etc.) to change the design or content.
- Add new routes for additional functionality as needed.
- Replace the file in static/files/cheat_sheet.pdf with your own downloadable content.
## 📜 License
This project is licensed under the MIT License. Feel free to use, modify, and distribute it as per the license.
