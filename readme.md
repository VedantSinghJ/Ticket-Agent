# 🧠 AI Ticket Assistant - by Vedant Singh Jadon

A smart AI-powered ticket management system that automatically categorizes, prioritizes, and assigns support tickets to the right moderators based on skills.

## 🚀 Features

- 🤖 AI-generated:
  - Ticket category & priority
  - Required skills & helpful notes
- 👥 Role-based access (User, Moderator, Admin)
- 🎯 Skill-based moderator assignment
- 📧 Email notifications using Mailtrap
- ⚙️ Background tasks powered by Inngest

## 🛠️ Tech Stack

- **Backend**: Node.js + Express
- **DB**: MongoDB + Mongoose
- **Auth**: JWT
- **AI**: Google Gemini API
- **Jobs**: Inngest
- **Email**: Nodemailer + Mailtrap

## ⚙️ Setup

1. **Clone & Install**
   ```bash
   git clone <your-repo-url>
   cd ai-ticket-assistant
   npm install


## .env Setup

MONGO_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
MAILTRAP_SMTP_HOST=your_mailtrap_host
MAILTRAP_SMTP_PORT=your_mailtrap_port
MAILTRAP_SMTP_USER=your_mailtrap_user
MAILTRAP_SMTP_PASS=your_mailtrap_pass
GEMINI_API_KEY=your_gemini_api_key
APP_URL=http://localhost:3000


## Run App
   ```bash
   npm run dev         # Start Express server
   npm run inngest-dev # Start Inngest dev server


## API Endpoints

POST /api/auth/signup – Register a new user

POST /api/auth/login – Login and receive JWT

POST /api/tickets – Create a ticket

GET /api/tickets – List tickets for logged-in user

GET /api/tickets/:id – Get ticket details

GET /api/auth/users – Admin: List all users

POST /api/auth/update-user – Admin: Update user role & skills


## 🙌 Credits

Google Gemini API – AI processing

Inngest – Background event handling

Mailtrap – Email testing

MongoDB – Data storage
