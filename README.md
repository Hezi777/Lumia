<h1 align="center"><b>Lumia</b></h1>

<p align="center">
  A full-stack Instagram-style photo sharing platform built with React, NestJS, and PostgreSQL.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=black&style=for-the-badge" />
  <img src="https://img.shields.io/badge/NestJS-9-E0234E?logo=nestjs&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Prisma-ORM-2D3748?logo=prisma&style=for-the-badge" />
  <img src="https://img.shields.io/badge/PostgreSQL-14-336791?logo=postgresql&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Material--UI-007FFF?logo=mui&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/github/license/Hezi777/lumia-image-sharing-app?style=for-the-badge" />
</p>

<p align="center">
  <a href="#about">About</a> |
  <a href="#features">Features</a> |
  <a href="#screenshots">Screenshots</a> |
  <a href="#tech-stack">Tech Stack</a> |
  <a href="#getting-started">Getting Started</a> |
  <a href="#contributing">Contributing</a>
</p>

---

## About

Lumia is a full-stack photo sharing web application inspired by Instagram, built to explore modern full-stack architecture with a React frontend and a NestJS REST API backend. It allows users to upload images via drag-and-drop, browse a responsive infinite-scroll gallery, and engage with posts through likes and comments. The project demonstrates end-to-end integration of a typed ORM (Prisma), relational database (PostgreSQL), and a component-driven React UI.

---

## Features

| Area | Description |
|------|-------------|
| Image Upload | Drag-and-drop interface with live preview and file type/size validation |
| Gallery | Responsive grid layout with infinite scroll and image metadata display |
| Likes and Comments | Optimistic UI updates for likes and per-image comment threads |
| User Profiles | Personal gallery grid with post stats and inline username editing |
| Dark Mode | Toggleable dark theme with persistent user preference |
| Mobile-First Design | Fully responsive layout across all screen sizes |
| REST API | Structured backend endpoints for images, likes, and comments |

---

## Screenshots

*(Demo content generated with sample travel and lifestyle images for presentation purposes.)*

| Home Gallery (Infinite Scroll) | Image Upload Interface |
|--------------------------------|------------------------|
| ![Home Gallery](frontend/public/Screenshots/Gallery.gif) | ![Upload Page](frontend/public/Screenshots/UploadPage.png) |

| User Authentication | User Profile |
|--------------------|--------------|
| ![Login](frontend/public/Screenshots/LoginPage.png) | ![Profile](frontend/public/Screenshots/ProfilePage.png) |

| Registration | Dark Mode Theme |
|--------------|----------------|
| ![Register](frontend/public/Screenshots/RegisterPage.png) | ![Dark Mode](frontend/public/Screenshots/DarkMode.png) |

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | React 19, TypeScript, Material-UI, React Router, Axios |
| Backend | NestJS 9, TypeScript, Prisma ORM, Multer |
| Database | PostgreSQL 14 |
| Storage | Local filesystem (`uploads/`) |

---

## Getting Started

### Prerequisites

- Node.js 18+
- PostgreSQL 14+
- npm

### 1. Clone the repository

```bash
git clone https://github.com/Hezi777/lumia-image-sharing-app.git
cd lumia-image-sharing-app
```

### 2. Install dependencies

```bash
npm install --prefix backend
npm install --prefix frontend
```

### 3. Configure environment

```bash
cp backend/.env.example backend/.env
cp frontend/.env.example frontend/.env
```

**`backend/.env`**
```env
DATABASE_URL="postgresql://USER:PASSWORD@HOST:PORT/DATABASE?schema=public"
PORT=3001
UPLOAD_DIR="./uploads"
CORS_ORIGIN="http://localhost:5173"
```

**`frontend/.env`**
```env
VITE_API_URL="http://localhost:3001"
```

### 4. Run the app

```bash
# Apply database migrations
npm run prisma:migrate:dev --prefix backend

# Start backend (http://localhost:3001)
npm run start:dev --prefix backend

# Start frontend (http://localhost:5173)
npm start --prefix frontend
```

---

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m "Add your feature"`
4. Push to the branch: `git push origin feature/your-feature`
5. Open a Pull Request

---

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
