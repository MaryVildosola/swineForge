# SwineForge — Smart Pig Farm Management

SwineForge is a comprehensive farm management system designed for modern piggery operations. It features real-time livestock tracking, inventory management, and an offline-first synchronization engine for field workers.

---

## 👨‍💻 Default Demo Credentials
If you have imported the dummy database (`database-dummy-data.sql`), use the following accounts to see the fully populated views:

| Role | Email | Password |
| :--- | :--- | :--- |
| **Administrator** | `admin@porcitrack.com` | `admin123` |
| **Worker View (With Data)** | `user1@gmail.com` | `12345678` |

## 🚀 Key Features
- **Live Analytics Dashboard**: 360° visibility over farm performance.
- **Offline-First Workflow**: Workers can log check-ins and medical data without internet.
- **Critical Alert System**: Immediate escalation of animal health emergencies.
- **Nutritional Management**: Feed formula building and inventory tracking.
- **QR Tracking**: Individual pig record access via mobile scanning.
- **Real-time Synchronization**: Built with Firebase for instantaneous data updates without page reloads.

## 🛠 Tech Stack
- **Backend**: Laravel 12 / PHP 8.4
- **Frontend**: Blade, Vanilla CSS, JavaScript (ES6+)
- **Database**: MySQL / MariaDB
- **Tools**: SweetAlert2, Boxicons, Mermaid.js

## 📚 Documentation
- **[Database Schema & Architecture](DATABASE.md)**: Detailed ERD and table references.
- **[Installation Guide](DOCUMENTATION.md)**: Step-by-step setup guide for buyers.

---

## 🛠 Setup Instructions

Follow these steps carefully to set up the project on your local machine:

1. **Clone the repository**
2. **Install Backend Dependencies**: 
   ```bash
   composer install
   ```
3. **Install Frontend Dependencies**:
   ```bash
   npm install
   ```
4. **Environment Setup**:
   - Create a copy of the environment file: `cp .env.example .env`
   - Generate application key: `php artisan key:generate`
   - **Important**: Create a database named `swineforge` (or your preferred name) in your MySQL server.
5. **Database Initialization**:
   - For an instant setup with dummy data, import the `database-dummy-data.sql` file into your database manager.
   - For a fresh slate, run migrations:
     ```bash
     php artisan migrate
     ```
6. **Compile Assets**:
   ```bash
   npm run build
   ```
7. **Start the Application**:
   ```bash
   php artisan serve
   ```

---

## ⚠️ Troubleshooting

- **403 Unauthorized**: This happens if your account doesn't have a role assigned. Register a new account ensuring you select a role or use the default accounts above.
- **Vite/Manifest Error**: Run `npm install && npm run build` to ensure assets are compiled.
