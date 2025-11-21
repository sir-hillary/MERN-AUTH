MERN Authentication System

A complete and secure MERN authentication system featuring JWT authentication, email verification with OTP, password reset with OTP, protected routes, secure HTTP-only cookies, and a React + Tailwind CSS UI.

This project is built using the MERN stack (MongoDB, Express, React, Node.js) and includes full API functionality and frontend pages for all authentication actions.

📌Core Features
🔐 Authentication

📌User registration with hashed passwords (bcrypt)

📌Login with JWT stored in HTTP-only cookies

📌Logout (secure cookie removal)

📌Protected routes using middleware

📌📧 Email Verification

📌OTP-based verification system

📌OTP expires after 24 hours

📌Email sent through Nodemailer

📌Verification UI page in React

📌Password Reset

📌Password reset request with OTP

📌OTP expires after 15 minutes

📌Reset password page in React

📌👤 Full Frontend

Built with:

📌React.js

📌Tailwind CSS

📌Context API for global user state

📌Axios for API calls

📌Toast notifications (react-toastify)

🛡 Security

📌Secure cookies (httpOnly, sameSite, secure)

📌JWT-based session management

📌Backend validation for missing fields and invalid input

🏗 Tech Stack
Frontend

📌React.js

📌Tailwind CSS

📌Context API

📌Axios

📌React Router

📌React Toastify

Backend

📌Node.js

📌Express.js

📌MongoDB + Mongoose

📌BcryptJS

📌JSON Web Tokens (JWT)

📌Nodemailer

📌Email templates (HTML)

📁 Project Structure
MERN-AUTH/
|
├── client/           # React frontend
│
├── server/           # Backend API
│   
└── README.md

🔧 Environment Variables

Create a .env file in the server folder:

MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
SENDER_EMAIL=your_email@example.com
SENDER_EMAIL_PASS=your_email_app_password
CLIENT_URL=http://localhost:5173


Create a .env file in the client folder if needed:

VITE_BACKEND_URL=http://localhost:5000

🚀 Running the Project Locally
1️⃣ Clone the Repository
git clone https://github.com/yourusername/mern-auth-system.git
cd mern-auth-system

2️⃣ Install Dependencies
Frontend
cd client
npm install

Backend
cd server
npm install

3️⃣ Start Development Servers
Run backend (Express API)
cd server
npm start

Run frontend (React app)
cd client
npm run dev

🔥 API Endpoints
Auth Routes
Register
POST /api/auth/register


Body:

{
  "name": "",
  "email": "",
  "password": ""
}

Login
POST /api/auth/login

Logout
POST /api/auth/logout

Send Verification OTP
POST /api/auth/send-verify-otp

Verify Email
POST /api/auth/verify-email

Send Reset OTP
POST /api/auth/send-reset-otp

Reset Password
POST /api/auth/reset-password

Check Authentication
GET /api/auth/is-authenticated

🎨 Frontend Screens (React)

The frontend includes:

Login page

Register page

Email Verification page

Reset Password page

Forgot Password page

Protected dashboard layout

Navbar with user initials and logout

Toast notifications

Fully responsive using Tailwind CSS.

🔥 Notable Features in Code
✔ Secure cookie-based JWT

Frontend never sees the token → safer from XSS.

✔ OTP expiration logic

Email OTP: 24 hours

Password OTP: 15 minutes

✔ Nodemailer with reusable email templates
✔ Clean Controller separation

register

login

sendVerifyOtp

verifyEmail

sendResetOtp

resetPassword

📦 Build for Production
Frontend
cd client
npm run build

Backend

If using plain JS:
No build needed.

☁ Deployment Tips (Render / Netlify / Vercel)
Backend (Render)

Build Command: npm install

Start Command: npm start

Add environment variables

Enable CORS with credentials

Add allowed origins (CLIENT_URL)

Frontend (Netlify/Vercel)

Set VITE_BACKEND_URL in dashboard

Enable redirects for React Router

👤 Author

Sirhillarytech
Full Stack MERN Developer
Nairobi, Kenya

🔗 GitHub: https://github.com/sir-hillary

🌐 Portfolio: https://sirhillarytech.vercel.app

💼 LinkedIn: https://www.linkedin.com/in/sirhillary-tech-13827a21b

💬 Fluent in English & Swahili

📜 License

This project is licensed under the MIT License.

🎯 Final Note

This MERN Authentication System is production-ready and can be used as a starter for:

SaaS apps

Dashboards

E-commerce platforms

Admin panels

User portals

Any project requiring secure user accounts
