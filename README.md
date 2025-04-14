# Supervised Multi-Agentic Booking Doctor Appointment

This repository provides the scaffolding for a multi-agent system designed to book doctor appointments using supervised learning techniques combined with modern AI tools. The project leverages a combination of FastAPI for backend API development, Streamlit for interactive UI, and a host of language model–driven tools from the LangChain ecosystem.

## Overview

The **Supervised Multi-Agentic Booking Doctor Appointment** project is intended to build a robust and scalable system for managing doctor appointment bookings. While core modules such as the agent logic and backend orchestration are currently placeholders, the repository structure and extensive dependency list (see [requirements.txt](requirements.txt)) indicate an ambitious design that integrates:

- **Data Model Validation:** Using Pydantic to ensure that inputs like dates and identification numbers adhere to strict formats.
- **API Layer:** Utilizing FastAPI to expose RESTful endpoints for appointment management.
- **User Interface:** Providing a responsive front-end built with Streamlit.
- **Multi-Agent Framework:** Integrating various agents (planned to be defined in `agent.py`) which may leverage generative AI and the LangChain toolkit to handle tasks such as appointment negotiation, availability checking, and more.
- **Data Handling:** Using a sample dataset (`notebook/doctor_availability.csv`) to demonstrate the booking process.

## Project Structure

- **data_models/**  
  Contains Pydantic models for data validation:
  - `models.py`  
    Defines:
    - `DateTimeModel`: Validates date strings in the format **DD-MM-YYYY HH:MM**.
    - `DateModel`: Validates dates in the format **DD-MM-YYYY**.
    - `IdentificationNumberModel`: Ensures an ID is a 7 or 8 digit integer.

- **notebook/**  
  Contains example data:
  - `doctor_availability.csv`: A CSV file with sample data for doctor availability.

- **agent.py**  
  Intended to implement agent behavior for handling appointment booking.  
  *Status: Currently empty – to be developed.*

- **main.py**  
  Expected to be the main entry point for launching the API server.  
  *Status: Currently empty – to be developed.*

- **streamlit_ui.py**  
  Designed for the front-end interface using Streamlit.  
  *Status: Currently empty – to be developed.*

- **requirements.txt**  
  Lists all external dependencies including FastAPI, Streamlit, Pydantic, LangChain libraries, and many others required for a full-scale implementation.

- **setup.py**  
  A standard setup script for packaging the project.


