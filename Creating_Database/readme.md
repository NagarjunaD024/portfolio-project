<div align="center">

### Chapter 3: Building and Querying a Relational Database

![Language](https://img.shields.io/badge/Language-Python-blue)
![SQLAlchemy](https://img.shields.io/badge/ORM-SQLAlchemy-green)
![Pytest](https://img.shields.io/badge/Testing-Pytest-blue)


</div>

 You will learn how to:

*   **Architect and populate** a SQLite database using foundational DDL scripts.
*   **Map the database schema** to clean, reusable Python objects with the SQLAlchemy ORM.
*   **Build a robust interface** to query and retrieve data programmatically.

---

### 🚀 Getting Started: Prerequisites

Before diving into the code, you'll need to install the project's dependencies. 

From your terminal, run:
```bash
pip3 install -r requirements.txt
```
### 🗃️ Database Setup

Before running the application, you must create and populate the SQLite database.

1.  **Create the tables** by running the `Queries.txt` script.
2.  **Populate the tables** by importing the `.csv` files from the `/data` directory.
---
### 📁 Directory Layout

| Path | Component | **Purpose & Description** |
| :--- | :--- | :--- |
| `Creating_Database/` | **Root Directory** | Contains all the assets and source code for this chapter. |
| 📁 `data/` | **Raw Data Assets** |  The `.csv` files here represent the initial data before it's loaded into the database. |
| 📁 `src/` | **Application Core** | It contains all the Python modules and the live database that power the application. |
| 🗃️ `src/fantasy_data.db` | **Live Database** | This is the final, operational SQLite database file containing all structured and populated data. |
| 📄 `src/database.py` | **The DB Connector** | Manages all connection logic. This module configures the SQLAlchemy engine and handles how our application communicates with the SQLite database. |
| 📄 `src/models.py` | **The Data Blueprints (ORM)** | Defines the "shape" of our data tables as Python classes. These SQLAlchemy models are the architectural blueprints that map our code to the database schema. |
| 📄 `src/crud.py` | **The Query Interface** | Contains the business logic for all data operations (**C**reate, **R**ead, **U**pdate, **D**elete). This is where functions like `get_player` and `get_leagues` live. |
| 📄 `src/test_crud.py` | **Quality Assurance Suite** | This suite of tests verifies that all functions in `crud.py` are working correctly, ensuring our data operations are reliable and bug-free. |

