# TODO List

## 1. Project Setup
- [ x ] Set up the project directory structure for a Flask application.
- [ x ] Create a Python virtual environment (`venv` or `conda`) for isolated development.
- [ x ] Install Flask and essential dependencies:
  - `flask`
  - `flask-admin` (for the admin panel)
  - `cadquery` (for geometry generation)
  - `numpy`
  - `pytest` (for testing)
- [ x ] Initialise a Git repository and push to GitHub using the desktop app.
- [ ] Add a `.gitignore` file (e.g., ignore `__pycache__`, `.DS_Store`, virtual environments, STL files, etc.).
- [ ] Create a basic Flask project structure:
  - `app/` for core logic.
  - `templates/` and `static/` for web interface assets (if needed).
- [ ] Set up Docker for local deployment:
  - Create a `Dockerfile` to containerize the Flask application.
  - Create a `docker-compose.yml` file to manage dependencies and services.
    
---

## 2. Core Functionality

### a. Database Models
- [ ] Define models for track components in `models.py`:
  - Straight Track: Include length and other parameters.
  - Chairs: Include dimensions and types (minimal for MVP).
  - Rails: Placeholder for future iterations.
- [ ] Use Flask-SQLAlchemy to implement the database.
- [ ] Create migrations and populate the database with example data using Flask-Migrate.

### b. Geometry and STL Export
- [ ] Implement a function to generate geometry for straight tracks.
- [ ] Integrate geometry generation with Flask routes.
- [ ] Use CadQuery to generate STL files based on user input.
- [ ] Validate the integrity of exported STL files using an STL viewer (e.g., MeshLab).
- [ ] Provide a downloadable STL file through the Flask app.

### c. Admin Panel
- [ ] Use Flask-Admin to create an admin interface for managing:
  - Database entries for chairs, rails, and straight tracks.
  - Configuration settings.
- [ ] Ensure the admin panel allows CRUD operations on database models.

### d. User Interface
- [ ] Create a simple web interface for:
  - Submitting track parameters (e.g., length).
  - Viewing and downloading the generated STL file.
- [ ] Test for usability and responsiveness.

---

## 3. Testing
- [ ] Write unit tests for models, routes, and geometry generation functions using `pytest`.
- [ ] Test STL export functionality with various track lengths.
- [ ] Test the admin panel for proper CRUD operations.
- [ ] Perform manual testing to validate the complete MVP workflow.
- [ ] Validate edge cases, such as:
  - Extremely short or long tracks.
  - Invalid user inputs.

---

## 4. Deployment (Local Testing Only)
- [ ] Deploy the Flask app on Docker Desktop for local testing.
- [ ] Verify the Docker setup:
  - Ensure all dependencies are included.
  - Validate the app runs correctly within the container.
- [ ] Document the steps for building and running the Docker container.

---

## 5. Documentation
- [ ] Write a clear **Getting Started** guide for contributors.
- [ ] Document all database models and their relationships.
- [ ] Provide usage examples for the admin panel and web interface.
- [ ] Create a troubleshooting guide for common issues.
- [ ] Include detailed steps for setting up the Flask app locally and in Docker.
