# 🎬 QuickShow – Movie Ticket Booking App

QuickShow is a full-stack movie ticket booking web application. Users can browse movies, view details and showtimes, pick seats, and book tickets online.

## ✨ Features

- Browse current and upcoming movies
- Movie details with genre, release year and runtime
- Theatre and showtime listings
- Seat selection and ticket booking
- User login / authentication
- Favourite movies list
- Background jobs and event handling with Inngest
- Responsive, modern UI

## 🛠️ Tech Stack

**Client**
- React (Vite)
- Tailwind CSS
- ESLint

**Server**
- Node.js
- Express.js
- MongoDB (Mongoose models)
- Inngest (background jobs / events)

**Deployment**
- Vercel (both `client` and `server` include a `vercel.json`)

## 📁 Project Structure

```
movie-ticket-booking/
├── client/                 # Frontend (React + Vite)
│   ├── index.html
│   ├── package.json
│   ├── vite.config.js
│   ├── eslint.config.js
│   └── vercel.json
│
└── server/                 # Backend (Node + Express)
    ├── config/             # Database & app configuration
    ├── controllers/        # Route handlers / business logic
    ├── inngest/            # Inngest functions and client
    ├── lib/                # Helper utilities
    ├── middlewares/        # Auth and other middlewares
    ├── models/             # Mongoose schemas
    ├── routes/             # API routes
    ├── server.js           # Entry point
    ├── package.json
    └── vercel.json
```

## 🚀 Getting Started

### Prerequisites

- Node.js (v18 or later)
- npm
- A MongoDB database (local or Atlas)

### 1. Clone the repository

```bash
git clone <your-repo-url>
cd movie-ticket-booking
```

### 2. Setup the server

```bash
cd server
npm install
```

Create a `.env` file in the `server` folder:

```env
PORT=3000
MONGODB_URI=your_mongodb_connection_string

# Add any other keys your app uses (auth, Inngest, payments, etc.)
```

Start the server:

```bash
npm run server
# or
node server.js
```

### 3. Setup the client

```bash
cd client
npm install
```

Create a `.env` file in the `client` folder:

```env
VITE_BASE_URL=http://localhost:3000
```

Start the development server:

```bash
npm run dev
```

The app will be available at **http://localhost:5173**.

## 📜 Available Scripts

**Client**

| Command           | Description                  |
| ----------------- | ---------------------------- |
| `npm run dev`     | Start the Vite dev server    |
| `npm run build`   | Build for production         |
| `npm run preview` | Preview the production build |
| `npm run lint`    | Run ESLint                   |

**Server**

| Command          | Description                      |
| ---------------- | -------------------------------- |
| `npm start`      | Start the server                 |
| `npm run server` | Start the server in watch mode   |

> Adjust script names to match your `package.json`.

## 🌐 Deployment

Both the client and the server can be deployed to [Vercel](https://vercel.com). Each folder contains its own `vercel.json`, so deploy them as two separate projects and set the environment variables in the Vercel dashboard.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m "Add your feature"`
4. Push the branch: `git push origin feature/your-feature`
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License.
