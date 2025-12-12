# StudyNotion :books::rocket:

**A Modern EdTech Platform for Creating, Discovering & Learning**

Live Website: [https://studynotion-frontend.vercel.app/](https://studynotion-frontend.vercel.app/)

![StudyNotion Hero](images/mainpage.png)

StudyNotion is a **fully functional EdTech platform** built with the **MERN stack** (MongoDB, Express.js, React.js, Node.js). It allows **students** to learn from high-quality courses and enables **instructors** to create, manage, and monetize their content seamlessly.

---

## Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [System Architecture](#system-architecture)
- [Frontend Overview](#frontend-overview)
- [Backend Features](#backend-features)
- [Database Schema](#database-schema)
- [API Design](#api-design)
- [Screenshots](#screenshots)
- [Installation & Setup](#installation--setup)
- [Environment Variables](#environment-variables)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)

---

## Features

### For Students
- Browse & filter courses
- Add courses to wishlist/cart
- Secure enrollment via Razorpay
- Watch video lectures & download resources
- Rate and review courses
- Track progress & view enrolled courses
- Responsive & intuitive UI

### For Instructors
- Create and publish courses
- Upload video lectures, PDFs, quizzes
- Rich text (Markdown) support for content
- Analytics dashboard (views, revenue, ratings)
- Manage course pricing & content
- Update profile and course details

### Platform-Wide
- Role-based authentication (Student / Instructor / Admin)
- OTP-based login & password reset
- Cloudinary for media storage (videos, thumbnails, documents)
- JWT-based secure sessions
- Responsive design (mobile + desktop)

---

## Tech Stack

| Layer         | Technology                                      |
|-------------|-------------------------------------------------|
| Frontend     | React.js, Redux Toolkit, Tailwind CSS, React Router |
| Backend      | Node.js, Express.js                             |
| Database     | MongoDB (with Mongoose ODM)                     |
| Authentication | JWT, Bcrypt, Nodemailer (OTP)                 |
| Payments     | Razorpay                                        |
| Media Storage| Cloudinary                                      |
| Deployment   | Vercel (Frontend), Render/Railway (Backend)     |

---

## System Architecture

```mermaid
graph TD
    A[Client (React + Tailwind)] -->|REST API| B(Express.js Server)
    B --> C(MongoDB)
    B --> D(Cloudinary - Media Storage)
    B --> E(Razorpay - Payments)
    B --> F(Nodemailer - Email/OTP)