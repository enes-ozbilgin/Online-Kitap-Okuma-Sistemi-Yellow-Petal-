# Yellow Petal - Online Book Evaluation System

![Java](https://img.shields.io/badge/Language-Java-orange) ![Database](https://img.shields.io/badge/Database-MySQL-blue) ![GUI](https://img.shields.io/badge/Interface-Swing-lightgrey)

**Yellow Petal** is a comprehensive Java desktop application designed to manage an online book reading and evaluation community. The system connects Readers, Writers, and Managers, allowing users to publish books, write reviews, organize events, and manage library content through a graphical user interface.

## 🌟 Features

The system is divided into three distinct user roles, each with specific capabilities:

### 📖 For Readers
* **User Authentication:** Sign up and login securely.
* **Browse Content:** View top-rated books and search the library.
* **Engagement:** Rate books, provide feedback, and join reading events.
* **Support:** Submit tickets for issues.

### ✍️ For Writers
* **Content Management:** Publish new books and manage existing drafts.
* **Analytics:** View reports on book performance and reader feedback.
* **Events:** Create and participate in literary events.

### 🛡️ For Managers
* **Administration:** Full control over the system's content.
* **Reporting:** Access detailed reports on system usage, popular books, and user activity.
* **Event Oversight:** Manage and approve events.

## 🏗️ Technical Architecture

The project follows a layered architecture (DAO Pattern) to separate data logic from the user interface.

* **Database:** MySQL (schema provided in `mydb.sql`).
* **Core (Model & DAO):**
    * `*DAO.java` files (e.g., `BookDAO`, `UserDAO`) handle all SQL database operations.
    * Entity classes (`Book`, `Reader`, `Writer`) represent the data models.
* **UI (View):**
    * Located in the `src/panel` package.
    * Uses `JPanel` and `JFrame` for a responsive desktop experience (e.g., `ManagerPanel`, `ReaderMainPanel`).

## 📂 Project Structure

```text
Online-Kitap-Okuma-Sistemi-Yellow-Petal/
├── src/
│   ├── core/           # Data Access Objects (DAO) and Models
│   │   ├── BookDAO.java
│   │   ├── ReaderDAO.java
│   │   └── ...
│   └── panel/          # GUI Components (Swing)
│       ├── ManagerLoginPanel.java
│       ├── AddBookPanel.java
│       └── ...
├── mydb.sql            # Database backup/schema file
└── mysql-connector.jar # JDBC Driver for MySQL connectivity
