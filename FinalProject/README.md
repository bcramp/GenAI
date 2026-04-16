# Team Introduction
# Welcome to the team 404 Robot Nurse project! Below, each team member will introduce themselves

## Team Members

### Brennen
Hi there! I'm Brennen. I'm working on ....

### Mark
Hi! I'm Mark. I'll focus on ....

## Project Details
Robot nurses are automated systems designed to assist medical staff in various tasks, including delivering medication to patients. The A* algorithm, a variant of Dijkstra's algorithm, is often used in robotics for its efficiency in finding the shortest path from one point to another while considering obstacles.

In this project, we will use the A* and Dijkstra's algorithms to help a robot nurse deliver medication, collect test samples, and function as a telemedicine interface allowing nurses to provide remote patient care. The hospital used has a total of 12 wards and will be represented with a 40x40 grid structure. Instead of command-line arguments to execute the code, just installing the "uv" package manager and running "uv run app" in your terminal will start the application; allowing for only UI interactions to test the robot nurse.


# Information on Building the Project

## Languages/Packages Version Control

1. python: v3.12
2. uv: v0.9.7 (hash: 0adb44480; commited on: 2025-10-30)
    - This version of uv will contain these packages:
        - app: v0.0.1
        - numpy: v2.3.4
        - opencv-python: v4.11.0.86

## UV Information

- "uv" is a fast, all-in-one Python package and project manager that can replace tools like pip, venv, pipx, and pyenv.
- This project manager can manage project dependencies, install Python versions, create and manage virtual environments, and even run single-file scripts in isolated environments.
- To learn more, visit their website: https://docs.astral.sh/uv/

## How to Run the Application

To run the application, for linux/macOS users, follow these steps:

1. Ensure you have Python 3.14 or higher and uv package manager installed.
    - Install Python 3.14 for language (https://www.python.org/downloads/release/python-3140/)
        - After clicking on the link, hover-over the "Downloads" section on the ribbon at the top of the page to select your OS download.
            - Windows/Linux: https://www.python.org/downloads/windows/
            - macOS: https://www.python.org/downloads/macos/
        - Download Python version 3.14+ and follow the instructions with the "Installation Wizard"
    - Install uv for the package manager (https://docs.astral.sh/uv/getting-started/installation/#__tabbed_1_1)
        - Run this for linux/macOS in your terminal: `curl -LsSf https://astral.sh/uv/install.sh | sh`
        - There are options for PowerShell/Windows users as well on the site, so follow the directions at the link above.

Note: As said prior, the following instructions are for linux/macOS users!

2. Restart your terminal once finished running the commands listed in step 1.
3. Clone the project repo: `git clone https://github.com/SJUCS/ai-final-project-team4.git`
4. Navigate to the project directory in your terminal: `cd ai-final-project-team4`
5. Ensure you have checked out the "main" branch: `git checkout main`
6. Finally, run the application: `uv run app`

# Project File Structure

```text
.
├── assets # Contains the images of the hospital used for creating the floorplan.
├── scripts # Contains the image to matrix converter and PyInstaller bundle scripts.
├── src/app
│   ├── assets
│   │   ├── icon.ico # Reduced application's UI icon.
│   │   └── icon.png # Application's UI icon image.
│   ├── config
│   │   ├── __init__.py # Contains the application's configuration and constants.
│   │   └── settings.py # Application configuration and constants.
│   ├── core
│   │   ├── __init__.py # Contains the application's core module for pathfinding and search algorithms.
│   │   └── search.py # A* and Dijkstra search algorithm implementations.
│   ├── data
│   │   ├── __init__.py # Data module for the robot pathfinding application.
│   │   └── edge_walls.json # Contains the edge walls for the internal walls for the hospital.
│   │   ├── floorplan.py # Contains the hard-coded hospital floorplan matrix used by the robot pathfinding system.
│   │   └── manager.py # Floorplan data manager for hospital pathfinding application.
│   ├── ui
│   │   ├── __init__.py # UI module for hospital floorplan pathfinding visualizer.
│   │   └── animator.py # Responsible for animating pathfinding visualizations.
│   │   ├── builder.py # Constructs all UI components including the canvas, control panels, buttons, and interactive elements.
│   │   └── controller.py # Responsible for managing pathfinding operations.
│   │   └── editor.py # Manages edge wall editing functionality.
│   │   ├── handler.py # Responsible for processing all user interactions with the visualizer interface.
│   │   └── renderer.py # Responsible for all canvas drawing operations.
│   │   └── updater.py # Responsible for updating the information panel that shows statistics, instructions, and current state information to the user.
│   │   ├── visualizer.py # Serves as the central coordinator for the entire visualization system and integration of UI components.
│   ├── utils
│   │   ├── __init__.py # Utility functions and helpers for the robot pathfinding application.
│   │   └── logger.py # Logging configuration and utilities.
│   │   ├── paths.py # Path utilities for resource management in development and bundled environments.
│   │   └── theme.py # Theme and styling utilities.
│   └── __init__.py # provides a graphical interface for visualizing and interacting with hospital floorplans, including pathfinding algorithms, interactive editing, and hospital ward information.
│   └── main.py # Initialize and run the robot pathfinding application.
├── .gitignore # Specifies files and directories that Git should intentionally ignore and not track within the repo.
├── .python-version # Identifies the python version that should be utilized to run the application.
└── README.md # Describes the project, team members, and how to run the application.
