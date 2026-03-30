# Swasth Khet 2.0 

**Swasth Khet 2.0** is an AI-powered comprehensive farm management platform designed to empower farmers with modern technology. The platform leverages artificial intelligence to provide actionable insights, disease detection, and continuous support to optimize agricultural practices and yields.

## 💡 The Idea Behind It
The core vision of Swasth Khet is to bridge the gap between traditional farming and modern technology. By integrating AI and data-driven insights, it solves key challenges faced by farmers:
- Difficulty in accurately identifying and treating crop diseases early.
- Lack of access to instant, reliable expert agricultural advice.
- Challenges in farm management, crop tracking, and understanding carbon footprints.
- A need for a centralized platform to connect with marketplaces and weather updates.

Swasth Khet acts as a digital companion for farmers, aiming to improve crop health, increase productivity, and promote sustainable farming practices.

## 🏗️ Working Architecture
The project follows a decoupled **MERN (MongoDB, Express, React, Node.js) Stack** architecture, ensuring high performance, scalability, and ease of maintenance.

### 1. Frontend (Client-Side)
- **Framework**: Built with **React** and **TypeScript** using **Vite**.
- **UI/UX**: Uses **Tailwind CSS** and **Shadcn UI** (Radix UI primitives) for a fully responsive, modern, and accessible user interface. Data visualization is handled by **Recharts**.
- **Role**: It acts as the interactive interface for the end-users. It connects to the backend REST API to fetch data, authenticate users, upload images for disease detection, and interact with the AI chatbot.

### 2. Backend (Server-Side)
- **Framework**: Built with **Node.js** and **Express.js**.
- **Security & Optimization**: Secured with `helmet` for HTTP headers, `cors` for cross-origin resource sharing, and `express-rate-limit` to prevent abuse. User authentication is safely managed using `bcryptjs` and `jsonwebtoken`.
- **RESTful API**: Exposes a variety of modular controller endpoints:
  - `/api/auth`: User authentication and authorization.
  - `/api/farms` & `/api/crops`: Datastore for managing farm and crop portfolios.
  - `/api/disease`: Endpoint for crop disease diagnosis using AI and image uploads (Multer).
  - `/api/weather`: Real-time weather forecasting integration.
  - `/api/marketplace`: Peer-to-peer marketplace listings.
  - `/api/carbon`: Tools for tracking sustainable farming and carbon footprint.
  - `/api/chatbot`: Conversational AI interface for instant agricultural assistance.

### 3. Artificial Intelligence (AI) Layer
- **Integration**: Powered by **Google Generative AI (Gemini)**.
- **Capabilities**: It works as the brain behind the project, powering the intelligent conversational Chatbot for specialized agricultural advice and processing visual data for plant disease detection.

### 4. Database
- **NoSQL System**: **MongoDB**, interacted with via **Mongoose** ORM models.
- **Role**: Flexibly stores user profiles, farm records, crop cycles, marketplace listings, and disease history securely in documents.

### 5. Hosting & Deployment
- The platform follows an Infrastructure-as-Code (IaC) method for deployment using a unified `render.yaml` specification. It supports decoupled environments where the frontend acts as a Static Site and the backend runs as a continuous Web Service.
