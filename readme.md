# 🧠 AI Ticket Assistant

A smart AI-powered ticket management system that automatically categorizes, prioritizes, and assigns support tickets to the right moderators based on skills.

---

## 🚀 Features

- 🤖 **AI-Generated Insights**
  - Ticket category & priority
  - Required skills & helpful notes
- 👥 **Role-Based Access**
  - User, Moderator, Admin
- 🎯 **Skill-Based Assignment**
  - Regex matching for moderator skills
  - Fallback to Admin
- 📧 **Email Notifications**
  - Nodemailer + Mailtrap
- ⚙️ **Background Processing**
  - Event-driven jobs with Inngest

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Backend** | Node.js + Express |
| **Database** | MongoDB + Mongoose |
| **Authentication** | JWT |
| **AI** | Google Gemini API |
| **Background Jobs** | Inngest |
| **Email** | Nodemailer + Mailtrap |

---

## 🔧 Configuration

Create a `.env` file in the project root with the following variables:

```env
# MongoDB
MONGO_URI=your_mongodb_uri

# JWT
JWT_SECRET=your_jwt_secret

# Mailtrap (Email)
MAILTRAP_SMTP_HOST=your_mailtrap_host
MAILTRAP_SMTP_PORT=your_mailtrap_port
MAILTRAP_SMTP_USER=your_mailtrap_user
MAILTRAP_SMTP_PASS=your_mailtrap_pass

# Google Gemini
GEMINI_API_KEY=your_gemini_api_key

# Application URL
APP_URL=http://localhost:3000
```

---

## ▶️ Running the Application

1. **Start Express server**
   ```bash
   npm run dev
   ```

2. **Start Inngest dev server**
   ```bash
   npm run inngest-dev
   ```

The API will be available at `http://localhost:3000` and Inngest at `http://localhost:8288`.

---

## 📮 API Endpoints

### Authentication

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/signup` | Register a new user |
| POST | `/api/auth/login` | Login and get a JWT |

### Tickets

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/tickets` | Create a new support ticket |
| GET | `/api/tickets` | List tickets for the logged-in user |
| GET | `/api/tickets/:id` | Get details of a specific ticket |

### Admin

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/auth/users` | List all users (Admin only) |
| POST | `/api/auth/update-user` | Update user role & skills |

---

### Common Issues
- **AI errors**: Verify `GEMINI_API_KEY` and check Google AI quotas
- **Email issues**: Confirm Mailtrap SMTP credentials
- **Database connection**: Ensure MongoDB is running and `MONGO_URI` is correct

---

## 🙌 Credits

- **Google Gemini API** – AI processing
- **Inngest** – Background job orchestration
- **Mailtrap** – Email testing
- **MongoDB** – Data storage

🚫 part of a structured learning project.

---

*Built with ❤️ for efficient ticket management*
