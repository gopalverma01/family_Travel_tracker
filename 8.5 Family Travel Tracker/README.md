# 🌍 Travel Tracker – A Multi-User Country Visiting App

Welcome to **Travel Tracker**, a full-stack web app that allows users to track the countries they've visited and manage their travel records in real time! Built with Node.js, Express, PostgreSQL, and EJS — this project showcases dynamic routing, relational databases, and clean UI handling.


---

## 🚀 Features

✅ Multi-user support  
✅ Add new countries you've visited  
✅ Search countries by name (partial match supported)  
✅ Color-coded UI per user  
✅ PostgreSQL-powered relational data management  
✅ EJS templates for server-side rendering  
✅ Deployed on [Render](https://render.com) ✨

---

## 🛠️ Tech Stack

| Layer      | Technology            |
|------------|------------------------|
| Backend    | Node.js, Express.js   |
| Database   | PostgreSQL            |
| Frontend   | HTML, CSS, EJS        |
| Hosting    | Render (Web + DB)     |

---

## 🧩 Database Schema

```sql
-- Users Table
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  name VARCHAR(100),
  color VARCHAR(20)
);

-- Countries Table
CREATE TABLE countries (
  country_code VARCHAR(10) PRIMARY KEY,
  country_name VARCHAR(100)
);

-- Visited Countries (Join Table)
CREATE TABLE visited_countries (
  id SERIAL PRIMARY KEY,
  user_id INT REFERENCES users(id),
  country_code VARCHAR(10) REFERENCES countries(country_code)
);


UI Overview
Homepage displays total countries visited by a selected user.

Form to add new countries (fuzzy search).

Option to switch user or create a new one.

Clean, responsive layout with user-specific theme colors.




How to Run Locally
1. Clone the Repo
bash
Copy
Edit
git clone https://github.com/yourusername/travel-tracker.git
cd travel-tracker
2. Install Dependencies
bash
Copy
Edit
npm install
3. Setup PostgreSQL
Create a PostgreSQL database and run the schema above.

4. Configure Environment Variables
Create a .env file and add:

env
Copy
Edit
DATABASE_URL=your_postgres_connection_string
5. Run the App
bash
Copy
Edit
node index.js
Visit: http://localhost:3000




👨‍💻 Author
Gopal Verma
Passionate Full Stack Developer • PostgreSQL enthusiast • Web lover
📧 gopal@example.com | LinkedIn | GitHub

