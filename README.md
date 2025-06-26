🧠 Sign Language Learning App
An educational web app that enables users to sign up, log in, and explore sign language-based rhymes and safety lessons. It includes authentication, interactive UI, and multimedia resources.

🚀 Features
✅ User Signup & Login

✅ Passwords hashed using bcrypt

✅ Secure MySQL Database Integration

✅ Responsive and animated frontend

✅ Rhymes grid UI with modern styling

✅ Cross-origin support with CORS

📁 Tech Stack
Backend: Flask (Python)

Database: MySQL

Frontend: HTML, CSS, JavaScript, Bootstrap

Security: bcrypt for password hashing

API Testing: Postman / cURL

CORS: Enabled for frontend-backend communication

🛠️ Installation & Setup
📌 Prerequisites
Python 3.8+

MySQL Server

pip (Python package installer)

🔧 Backend Setup
Clone the repository:

bash
Copy
Edit
git clone https://github.com/yourusername/sign-language-app.git
cd sign-language-app
Create and activate a virtual environment (optional but recommended):

bash
Copy
Edit
python -m venv venv
venv\Scripts\activate   # On Windows
Install dependencies:

bash
Copy
Edit
pip install flask flask-cors flask-mysqldb bcrypt
Configure MySQL database:

sql
Copy
Edit
CREATE DATABASE sign_language_app;

USE sign_language_app;

CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    fullname VARCHAR(100) NOT NULL,
    username VARCHAR(50) NOT NULL UNIQUE,
    email VARCHAR(100) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
Update MySQL credentials in app.py:

python
Copy
Edit
app.config['MYSQL_HOST'] = 'localhost'
app.config['MYSQL_USER'] = 'root'
app.config['MYSQL_PASSWORD'] = 'your_password'
app.config['MYSQL_DB'] = 'sign_language_app'
Run the backend server:

bash
Copy
Edit
python app.py
The server will start at http://localhost:5000.

🌐 Frontend Setup
Open login.html or signup.html in your browser.

Make sure your backend (app.py) is running on port 5000.

Use developer tools or browser console to debug if needed.

📬 API Endpoints
🔸 POST /signup
json
Copy
Edit
{
  "fullname": "Jane Doe",
  "username": "janedoe",
  "email": "jane@example.com",
  "password": "securepassword"
}
🔸 POST /login
json
Copy
Edit
{
  "username": "janedoe",
  "password": "securepassword"
}
🛡️ Security Notes
Passwords are securely hashed with bcrypt.

CORS is enabled for frontend-backend interaction.

Inputs should be validated in production.

📸 Screenshots


![Screenshot (49)](https://github.com/user-attachments/assets/979fbb7c-8477-4feb-89d9-308e658f8b93)
![Screenshot (50)](https://github.com/user-attachments/assets/7890e43b-d2a5-46f7-9d62-8b7c06b62a55)
![Screenshot (50)](https://github.com/user-attachments/assets/7890e43b-d2a5-46f7-9d62-8b7c06b62a55)
s://github.com/user-attachments/assets/ad00ece7-44ad-42f9-b571-8f5426d061ba)

🧑‍💻 Author
Developed by [K U Thanisha]
GitHub: @[Thanishaudayakumar](https://github.com/Thanishaudayakuma)

📄 License
This project is open-source and available under the MIT License.
