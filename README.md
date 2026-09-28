# lao-system_reijiro-mw600

Student Records Registry — a mini CRUD system built with Express and MySQL.
It stores student records (ID, name, program, year, email, status) and lets you
view, search, add, edit, and delete them from a simple web interface.

## Stack

- Node.js + Express (REST API + static file server)
- MySQL / MariaDB (`mysql2`)
- Plain HTML, CSS, and vanilla JavaScript on the front end

## Setup

1. Install dependencies:

   ```bash
   npm install
   ```

2. Create the database. Import `lao_student_db.sql` into MySQL (e.g. through
   phpMyAdmin) or run it from the CLI:

   ```bash
   mysql -u root < lao_student_db.sql
   ```

   This creates the `lao_student_db` database, the `students` table, and one
   sample record.

3. Check the connection settings in `server.js` match your MySQL setup
   (host, user, password, database).

4. Start the server:

   ```bash
   npm start
   ```

5. Open the app at http://localhost:3000

## API

| Method | Route                | Description          |
| ------ | -------------------- | -------------------- |
| GET    | `/api/students`      | List all students    |
| GET    | `/api/students/:id`  | Get one student      |
| POST   | `/api/students`      | Add a student        |
| PUT    | `/api/students/:id`  | Update a student     |
| DELETE | `/api/students/:id`  | Delete a student     |

## Files

- `server.js` — Express server and REST API
- `repository.js` — front-end data access layer (fetch wrappers)
- `index.html` — records list, search, and delete
- `add.html` — add a new record
- `edit.html` — edit or delete a record
- `style.css` — styling
- `lao_student_db.sql` — database schema and seed data
