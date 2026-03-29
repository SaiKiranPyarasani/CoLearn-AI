# 🚀 CoLearn AI - Collaborative Learning Platform

CoLearn AI is an AI-powered collaborative study platform where students can create notebooks, chat with AI about their notes, and study together in real-time.

---

## 🛠️ Local Development Setup

Follow these steps to get the project running on your local machine.

### 1. Prerequisites
- **Node.js** (v18 or higher recommended)
- **PostgreSQL** (Installed locally or using a cloud provider like Neon.tech)

### 2. Installation
Clone the repository and install the dependencies:
```bash
npm install
```

### 3. Environment Variables (`.env`)
Create a `.env` file in the root directory and add the following:
```env
# Database connection string (PostgreSQL)
# Format: postgresql://[user]:[password]@[host]:[port]/[database]
DATABASE_URL=your_postgresql_connection_string

# Gemini AI API Key (from Google AI Studio)
GEMINI_API_KEY=your_gemini_api_key

# Secret for JWT Token generation (any random string)
JWT_SECRET=colearn_secret_12345

# Optional: Server Port (default is 3000)
PORT=3000
```

### 4. Database Initialization
The app automatically initializes the necessary tables on startup. Ensure your `DATABASE_URL` is correct before running.

### 5. Running the App
Start the server:
```bash
npm start
```

Once started, you can access the platform at:
- **Frontend:** [http://localhost:3000/index.html](http://localhost:3000/index.html)
- **API Health:** [http://localhost:3000/api/health](http://localhost:3000/api/health)

---

## 🌐 Production Deployment (Zero Cost)

The project is optimized for a single-server deployment on **Render.com** and **Neon.tech**.

### 1. Database (Neon.tech)
1. Create a free account on [Neon.tech](https://neon.tech/).
2. Create a project and copy the **Connection String**.

### 2. Backend + Frontend (Render.com)
1. Push your code to a GitHub repository.
2. In [Render](https://render.com/), create a new **Web Service**.
3. **Build Command:** `npm install`
4. **Start Command:** `npm start`
5. **Environment Variables:** Add `DATABASE_URL`, `GEMINI_API_KEY`, and `JWT_SECRET` in the Render dashboard.

### 3. Access your Live App
Once deployed, your app will be available at:
`https://your-service-name.onrender.com/index.html`

---

## 📂 Project Structure
- `server/` - Express.js backend (API routes and database logic)
- `index.html` - Landing page
- `login.html` - Authentication (Register/Login)
- `home.html` - Dashboard (Notebook list, Notifications)
- `notebook.html` - The workspace (AI Chat, Notes, File context)
- `config.js` - Global configuration for API URLs
- `styles.css` - Custom styling
- `tailwind.config.js` - UI Theme configuration