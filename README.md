# Doctor Search & Appointment Booking System

## Overview
This project is a **Doctor Search & Appointment Booking System** built using the **MERN stack** (MongoDB, Express.js, React.js, Node.js). The system allows:
- **Patients** to search for doctors, book/cancel appointments.
- **Doctors** to manage their availability and appointments.

## Tech Stack
- **Frontend:** React.js, Tailwind CSS, Zustand (for state management)
- **Backend:** Node.js, Express.js, MongoDB, Mongoose
- **Authentication:** JWT, bcrypt.js
- **Database:** MongoDB
- **Email Notifications:** Nodemailer
- **Deployment:**
  - **Frontend:** Vercel/Netlify
  - **Backend:** Render/AWS Lambda

---

## Features
### 1. User Authentication & Role Management
- JWT-based authentication for **Doctors and Patients**.
- Secure password hashing with bcrypt.js.

### 2. Doctor Search & Profile Management
- Patients can search for doctors using:
  - **Specialty** (e.g., Cardiologist, Dermatologist)
  - **Location** (City, State)
  - **Doctor's Name** (Partial Match Search)
- Doctor profile displays:
  - Name, Specialty, Experience, Location, Availability Slots.

### 3. Appointment Booking System
- **Doctors** set their working hours and consultation locations.
- **Patients** can book available slots.
- **Concurrency handling** to prevent double booking.
- **Patients** can cancel appointments.
- Email notifications sent for bookings and cancellations.

### 4. Web Interface (Frontend)
#### **Patient Portal**
- Search for doctors.
- Book or cancel appointments.

#### **Doctor Dashboard**
- Set up consultation locations.
- Define and update availability.
- View upcoming appointments.

---

## Installation & Setup
### Backend Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo-url.git
   cd backend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Set up environment variables in a `.env` file:
   ```env
   PORT=5000
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   EMAIL_USER=your_email@example.com
   EMAIL_PASS=your_email_password
   ```
4. Start the backend server:
   ```bash
   npm start
   ```

### Frontend Setup
1. Navigate to the frontend folder:
   ```bash
   cd frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the development server:
   ```bash
   npm start
   ```

---

## API Endpoints
### Authentication
| Method | Endpoint        | Description          |
|--------|----------------|----------------------|
| POST   | /api/auth/register | Register a user (Patient/Doctor) |
| POST   | /api/auth/login | Login and get a JWT token |

### Doctor Management
| Method | Endpoint        | Description          |
|--------|----------------|----------------------|
| GET    | /api/doctors | Get list of doctors |
| GET    | /api/doctors/:id | Get doctor details |
| PUT    | /api/doctors/:id/availability | Set availability |

### Appointment Management
| Method | Endpoint        | Description          |
|--------|----------------|----------------------|
| POST   | /api/appointments/book | Book an appointment |
| DELETE | /api/appointments/:id/cancel | Cancel an appointment |

---

## Deployment
### Backend Deployment
- Hosted on **Render/AWS Lambda**.
- Ensure MongoDB is properly configured.

### Frontend Deployment
- Hosted on **Vercel/Netlify**.

---

## Live Demo
- **Frontend:** [Live Link](https://your-frontend-url.vercel.app)
- **Backend:** [Live API](https://your-backend-url.render.com)

---

## Future Enhancements
- Implement **real-time notifications** for appointment updates.
- Add **payment gateway** for online consultations.
- Improve **UI/UX** with animations and accessibility enhancements.

---

## Author
Developed by **[Your Name]** as part of the **Arogo AI - MERN Developer Intern Assignment**.

