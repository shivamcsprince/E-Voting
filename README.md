# 🗳️ E-Voting — Online Election System


A full-stack MERN web application that enables secure, anonymous online voting. Built as a portfolio/learning project to demonstrate end-to-end development skills including REST APIs, authentication, and real-time data.

---

## 📋 Table of Contents

- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Environment Variables](#-environment-variables)
- [API Endpoints](#-api-endpoints)
- [Screenshots](#-screenshots)
- [License](#-license)

---

## ✨ Features

- 🔐 **User Authentication** — Secure registration & login with JWT tokens
- 🗳️ **Create Elections** — Admins can create and manage elections/polls
- 🕵️ **Anonymous Voting** — Cast votes without revealing your identity
- 📊 **Real-Time Results** — View live vote counts and results
- 🛡️ **Admin Dashboard** — Manage users, elections, and monitor activity
- 🚫 **One Vote Per User** — Prevents duplicate voting per election

---

## 🛠 Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React.js, React Router, Axios |
| Backend | Node.js, Express.js |
| Database | MongoDB, Mongoose |
| Auth | JSON Web Tokens (JWT), bcrypt |
| Styling | CSS / Tailwind CSS |

---

## 📁 Project Structure

```
E-Voting/
├── backend/
│   ├── controllers/       # Route handlers
│   ├── middleware/        # Auth middleware (JWT verification)
│   ├── models/            # Mongoose schemas (User, Election, Vote)
│   ├── routes/            # API route definitions
│   └── server.js          # Entry point
├── frontend/
│   ├── public/
│   └── src/
│       ├── components/    # Reusable UI components
│       ├── pages/         # Page-level components
│       ├── context/       # Auth context / state management
│       └── App.js
├── .gitignore
├── package.json
└── README.md
```

---



The application will run at `http://localhost:3000` and the API at `http://localhost:5000`.

---


 📡 API Endpoints

 Auth Routes — `/api/auth`

| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| POST | `/register` | Register a new user | ❌ |
| POST | `/login` | Login and get JWT token | ❌ |

 Election Routes — `/api/elections`

| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| GET | `/` | Get all elections | ✅ |
| POST | `/` | Create a new election | ✅ Admin |
| GET | `/:id` | Get election by ID | ✅ |
| DELETE | `/:id` | Delete an election | ✅ Admin |

### Vote Routes — `/api/votes`

| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| POST | `/` | Cast a vote | ✅ |
| GET | `/:electionId` | Get results for an election | ✅ |

---


 Contributing

This is a personal learning project, but feedback and suggestions are welcome!

1. Fork the repo
2. Create a new branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author 
Shivam — @shivamcsprince


**Shivam** — [@shivamcsprince](https://github.com/shivamcsprince)

⭐ If you found this project helpful, please consider giving it a star!
