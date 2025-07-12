<div align="center">

# Chapter 4 -  Developing the FastAPI Code

![Language](https://img.shields.io/badge/Language-Python-blue)
![SQLAlchemy](https://img.shields.io/badge/ORM-SQLAlchemy-green)
![Pytest](https://img.shields.io/badge/Testing-Pytest-blue)
![FastAPI](https://img.shields.io/badge/API-FastAPI-teal?logo=fastapi&logoColor=white)
![Pydantic](https://img.shields.io/badge/Data%20Validation-Pydantic-orange?logo=pydantic&logoColor=white)
![Uvicorn](https://img.shields.io/badge/Web%20Server-Uvicorn-purple?logo=uvicorn&logoColor=white)

</div>

 You will learn how to:

*   **Define Pydantic schemas** to represent the data that your API consumers wanted to receive.
*   **Created a FastAPI**  program to process consumer requests and return data responses, tying everything together.
*   **Tested** the API with pytest and then ran it successfully on the web server.

---

### 🚀 Getting Started: Prerequisites

Before diving into the code, you'll need to install the project's dependencies. 

From your terminal, run:
```bash
pip3 install -r requirements.txt
```
### 🗃️ Database Setup

Review Creating_Database Repository

---
### 📁 Directory Layout

| Path | Component | **Purpose & Description** |
| :--- | :--- | :--- |
| `Fast_API/` | **Root Directory** | Contains all the assets and source code for this chapter. |
| 📁 `src/` | **Application Core** | It contains all the Python modules and the live database that power the application. |
| 📄 `main.py` | **API Entrypoint** | The primary file that launches the FastAPI application, defines the API endpoints (routes), and ties everything together. |
| 📄 `schemas.py` | **Data Contracts (Pydantic)** | Defines the "shape" of data for API requests and responses. These Pydantic models ensure data validation and generate clear API documentation. |
| 📄 `src/crud.py` | **The Query Interface** | Contains the business logic for all data operations (**C**reate, **R**ead, **U**pdate, **D**elete). This is where functions like `get_player` and `get_leagues` live. |
| 📄 `src/database.py` | **The DB Connector** | Manages all connection logic. This module configures the SQLAlchemy engine and handles how our application communicates with the SQLite database. |
| 🗃️ `src/fantasy_data.db` | **Live Database** |  The live, local database file that stores all the application's data. |
| 📄 `test_crud.py` & `test_main.py` | **Quality Assurance Suite** | These files contain all the `pytest` tests to verify that our business logic and API endpoints are working correctly and reliably. |
| `requirements.txt` | **Project Dependencies** | A list of all the Python packages required to run this application. Install them with `pip install -r requirements.txt`. |
| `readme.md` | **Project Guide** | The main documentation for the project (you're reading it!). |
