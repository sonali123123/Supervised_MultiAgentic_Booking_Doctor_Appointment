# Supervised Multi-Agentic Booking Doctor Appointment

This repository provides the scaffolding for a multi-agent system designed to book doctor appointments using supervised learning techniques and modern AI tools. The current structure integrates modules for data validation, prompt handling, toolkits for multi-agent orchestration, and user interfaces via both API and Streamlit-based UI. Future implementations will fill in the core logic for agents and workflows.

## Overview

The Supervised Multi-Agentic Booking Doctor Appointment system is conceived as a robust platform to manage doctor appointment bookings through an orchestrated multi-agent framework. The key ideas include:

Data Validation & Modeling: Ensuring input information (dates, identification numbers) adheres to expected formats using Pydantic.

Prompt and Agent Communication: Leveraging a dedicated prompt library and a toolkit for coordinating interactions between various agents.

Backend Services: A FastAPI-based service (planned within main.py) will serve as the API endpoint, integrating with the multi-agent backend.

User Interfaces: A Streamlit-based front-end (in streamlit_ui.py) offers an interactive visual interface for users.

Supervision with AI: The design supports incorporating modern language models and the LangChain ecosystem to manage negotiation, appointment scheduling, and more.



## Project Structure

Below is an overview of the repository structure along with brief explanations of each component:

### data_models

Located in the data_models folder, this module defines Pydantic models for data validation. It includes:

 models.py:

DateTimeModel:
Validates date and time strings based on the format DD-MM-YYYY HH:MM. It uses a regular expression to enforce proper formatting.

DateModel:
Validates date strings in the DD-MM-YYYY format.

IdentificationNumberModel:
Ensures that the provided identification number is either a 7-digit or 8-digit number by converting the integer to a string and matching it against the expected pattern.

These models help ensure that any data entering the system follows strict formats, reducing potential errors further downstream.



### prompt_library
The prompt_library folder is intended to store prompt templates and related code that guides the multi-agent system’s behavior. Although details are to be implemented, you can use this folder to:

Develop and refine natural language prompts

Configure templates for agent interactions

Store sample dialogues or instruction sets for training or supervising agent communication

### toolkit

The toolkit folder is designed to house various utility functions, modules, or classes that aid the multi-agent orchestration. Examples include:

Functions to dispatch tasks between agents

Wrappers to call external APIs or services (e.g., scheduling services)

Integration helpers for LangChain or other AI libraries

### utils

This folder is dedicated to general utility scripts and helper functions that support the overall project. Contents may include:



agent.py
The agent.py file is intended as the core definition for the agent(s) responsible for managing appointment booking negotiations. Potential future content includes:

Core logic for decision-making

Integration with prompt templates and toolkit functionalities

Communication routines between agents (e.g., querying availability, finalizing slots)

Currently, it serves as a placeholder for the eventual multi-agent logic that will drive the application.

main.py

The main.py file is expected to serve as the entry point for launching backend services. Planned features include:

Bootstrapping a FastAPI server for handling RESTful requests

Orchestrating communication between various system components (agents, UI, data models)

Connecting the appointment booking flow through defined endpoints

At this stage, it sets the foundation for API integration that you can build upon.

streamlit_ui.py

This file is aimed at providing a user-friendly front-end interface through Streamlit. The UI module may include:

Interactive forms for booking appointments

Display of doctor availability and confirmation of bookings

Visualization and feedback elements for the end-user

As with other modules, this file is to be extended with interactive components tailored to user needs.

Other Files
.gitignore:
Standard file specifying patterns for files and directories to be excluded from version control.

requirements.txt:
Lists project dependencies including FastAPI, Streamlit, Pydantic, LangChain libraries, and any additional packages required for AI-based task management.

setup.py:
The standard setup script for packaging and installing the project as a module. It defines metadata about the project and handles dependency installations.

