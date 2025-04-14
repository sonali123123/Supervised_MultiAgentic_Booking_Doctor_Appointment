# Supervised Multi-Agentic Booking Doctor Appointment

This repository provides the scaffolding for a multi-agent system designed to book doctor appointments using supervised learning techniques combined with modern AI tools. The project leverages a combination of FastAPI for backend API development, Streamlit for interactive UI, and a host of language model–driven tools from the LangChain ecosystem.




## Modules Description

### Data Models (`data_models/`)
- **Purpose:**  
  Define the core entities and schemas used across the application (e.g., models for doctor, patient, and appointment).
- **Key File:**  
  - `models.py`: Contains class definitions and utility methods for data validation and serialization.

### Booking Agent (`agent.py`)
- **Purpose:**  
  Implements the autonomous agents responsible for handling appointment bookings.
- **Key Features:**
  - **Decision-Making:** Uses a supervised learning model trained on historical or simulated booking data.
  - **Agent Coordination:** Implements logic for multi-agent communication and conflict resolution when booking overlapping time slots.

### Main Application (`main.py`)
- **Purpose:**  
  Acts as the central orchestrator for initializing agents, loading configurations, and managing the overall booking workflow.
- **Responsibilities:**
  - Initialize application components and configurations.
  - Coordinate agent interactions and execute booking simulations.

### Interactive User Interface (`streamlit_ui.py`)
- **Purpose:**  
  Offers a real-time, interactive front-end using Streamlit.
- **Key Features:**
  - **Real-Time Interactions:** Simulate booking scenarios and visualize agent actions.
  - **Data Visualization:** Display scheduling information, booking statuses, and other key data points.

### Notebooks (`notebook/`)
- **Purpose:**  
  Provide interactive Jupyter notebooks for:
  - Prototyping agent behavior and supervised learning models.
  - Demonstrating the booking simulation process.
  - Analyzing experimental results.

