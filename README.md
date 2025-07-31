#  Agent Task Distributor App

This full-stack web application allows an admin to manage agents and upload tasks in bulk using CSV files. Tasks are automatically distributed equally and sequentially among all agents.

---

##  Features

-  Admin Authentication (JWT-based)
-  Add Agents with international phone numbers
-  Upload CSV of tasks (with first name, phone, notes)
-  Tasks distributed evenly across agents
-  View agent-wise assigned tasks
-  Modern UI with background image, animations & hover effects

---

##  Tech Stack

**Frontend:**
- React.js
- Tailwind CSS
- Axios
- `react-select` + `country-telephone-data`

**Backend:**
- Node.js
- Express.js
- MongoDB (Mongoose)
- Multer (for CSV file uploads)
- csv-parser (for reading CSV)

---

##  Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/agent-task-distributor.git
cd agent-task-distributor
```

### 2. Backend Setup (`/backend`)

```bash
cd backend
npm install
```

- Create a `.env` file:
```env
PORT=5000
MONGO_URI=mongodb://localhost:27017/agent-tasks
JWT_SECRET=your_secret_key
```

- Start backend:
```bash
npm start
```

### 3. Frontend Setup (`/frontend`)

```bash
cd frontend
npm install
```

- Start frontend:
```bash
npm run dev  # or npm start
```

---

##  Folder Structure

```
/backend
  ├── routes/
  ├── models/
  ├── config/
  ├── controllers/
  └── server.js

/frontend
  ├── components/
  ├── pages/
  ├── App.jsx
  └── index.js
```

---

##  Sample CSV Format

Ensure your CSV has these exact headers:
```
FirstName,Phone,Notes
John,+912345678901,Important client
Jane,+447911123456,Follow up tomorrow
```

> ⚠️ The distribution logic will assign tasks round-robin to all registered agents.

---

## 🔐 Authentication

- Admin login generates a JWT token stored in localStorage.
- All protected routes require the `Authorization: Bearer <token>` header.

---

## 🌐 UI Preview

- Home: Background image, animated elements
- Login: Styled form with smooth transitions
- Admin Dashboard: Card-based links to key features
- Upload Page: CSV upload with success/failure feedback
- Task Viewer: Agent-wise grouped task cards

---

## 🤝 Contributing

Feel free to fork and enhance! Suggestions, improvements, and PRs are welcome.

---

## 📧 Contact

Created by [Your Name]  
Email: youremail@example.com  
LinkedIn: [your-link]

---