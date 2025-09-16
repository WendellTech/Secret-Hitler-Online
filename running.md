# Running Secret-Hitler-Online (Frontend + Backend)

This guide explains how to run both the **frontend (React/TypeScript)** and **backend (Java/Gradle)** locally.

---

## 1. Prerequisites

Make sure you have these installed:

- **Node.js** (v18 or later recommended)
- **npm** (comes with Node.js)
- **Java JDK** (17 or later)
- **Gradle** (or use the included `gradlew` script)
- **Git** (if pulling code from repository)

---

## 2. Running the Frontend

The frontend is a React app located in `frontend/`.

```bash
cd frontend
npm install   # install dependencies
npm start     # start the development server
```

- Default URL: [http://localhost:3000](http://localhost:3000)

---

## 3. Running the Backend

The backend is a Java/Gradle project located in `backend/`.

### Option A: Using Gradle Wrapper (recommended)

```bash
cd backend
./gradlew bootRun
```

### Option B: Build and Run JAR

```bash
cd backend
./gradlew build
java -jar build/libs/*.jar
```

- Default URL: [http://localhost:8080](http://localhost:8080)

---

## 4. Connecting Frontend to Backend

By default, the frontend may need the backend API URL.  
Check `frontend/src/config` (or similar) and ensure it points to:

```
http://localhost:8080
```

---

## 5. Stopping the Servers

- Press **CTRL + C** in each terminal window.

---

## 6. (Optional) Run with Docker

Backend includes a `Dockerfile`. To build and run:

```bash
cd backend
docker build -t secret-hitler-backend .
docker run -p 8080:8080 secret-hitler-backend
```

---
