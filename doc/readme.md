#  LMS Architecture Overview

This document describes the structure of the Library Management System (LMS) using a simple Three-Tier Architecture.

## Architectural Tiers

The system is split into three main, separate components:

### 1. Presentation Tier (Frontend)

* **What it is:** The User Interface (UI) that users and librarians see and interact with (e.g., website pages).
* **Role:** Sends requests (like searching for a book) to the Backend.
* **Tech:** [Specify your Frontend choice, e.g., HTML/JavaScript]

### 2. Application Tier (Backend)

* **What it is:** The server that runs the system's business rules and logic.
* **Role:** Processes all requests, enforces rules (like calculating fines), and manages data access.
* **Tech:** [Specify your Backend choice, e.g., Python/Flask]
* **Communication:** Uses **REST APIs** to talk to the Frontend and a database connector to talk to the Database.

### 3. Data Tier (Database)

* **What it is:** The storage location for all project data.
* **Role:** Safely stores and retrieves records for Books, Members, and Circulation Transactions.
* **Tech:** [Specify your Database choice, e.g., SQLite]

## Data Flow

1.  The **Frontend** sends a request (e.g., "Issue Book") to the **Backend**.
2.  The **Backend** checks the rules (business logic) and updates the **Database**.
3.  The **Database** confirms the update to the **Backend**.
4.  The **Backend** sends the result back to the **Frontend** to display to the user.
