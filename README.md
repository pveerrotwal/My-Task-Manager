# FastAPI (Task-Manager) Application Documentation:

Hi All, I created a documentation for Technical Assignemnt (VE3), Coding Exercise: Task Management Web Application !!

## **Introduction**

This documentation provides an overview of the FastAPI ToDo App, a simple application built using the FastAPI framework in Python. The app allows users to manage their todo tasks including adding, updating, and deleting tasks.

Live Demo (Deploye onrender) : https://my-task-manager-5.onrender.com/
## **Setup**

### **1. Installation**

First, make sure you have Python installed on your system. Then, follow these steps to set up the environment and install the necessary packages:

```bash
# Create project directory and navigate into it
mkdir fastapi-app && cd fastapi-app

# Create a Python Virtual Environment and Activate it
python3 -m venv venv && source venv/bin/activate

# Upgrade pip
python3 -m pip install --upgrade pip

# Install FastAPI
pip install fastapi

# Install an ASGI server (Uvicorn)
pip install uvicorn[standard]

# Install required packages
pip install python-multipart jinja2 sqlalchemy

```

### **2. Project Structure**

After installation, open the project in your preferred code editor (e.g., VSCode) and create the following files:

- **`app.py`**: Main FastAPI application file
- **`database.py`**: Database configuration file
- **`models.py`**: File containing SQLAlchemy models
- **`templates/base.html`**: HTML template for rendering the user interface

## **Usage**

### **1. Running the App**

To run the app, use the following command:

```bash
uvicorn app:app --reload
```

This command starts the Uvicorn server and reloads the app automatically whenever changes are detected.

### **2. Accessing the App**

Once the server is running, you can access the app in your web browser at **`http://localhost:8000`**.

![alt text](<Screenshot 2024-05-09 at 5.41.44 PM.png>)

## **Functionality**

### **1. Home Page (`/`)**

- Displays a list of todo tasks.
- Allows users to add, update, or delete tasks.

### **2. Adding a Task (`/add`)**

- Allows users to add a new todo task.
- Redirects to the home page after adding the task.

### **3. Updating a Task (`/update/{todo_id}`)**

- Allows users to mark a task as complete or incomplete.
- Redirects to the home page after updating the task.

### **4. Deleting a Task (`/delete/{todo_id}`)**

- Allows users to delete a task.
- Redirects to the home page after deleting the task.

## **Code Explanation**

### **`app.py`**

- Defines the FastAPI application and routes.
- Uses Jinja2 templates for rendering HTML.
- Handles requests for adding, updating, and deleting tasks.

### **`database.py`**

- Configures the database connection using SQLAlchemy.

### **`models.py`**

- Defines the **`Todo`** model using SQLAlchemy.

### **`templates/base.html`**

- Provides the HTML template for rendering the user interface.
- Includes form for adding tasks and displays a list of tasks.

### **API Backend**
The API backend of the FastAPI ToDo App consists of several routes for managing todo tasks:

You can access the api in your web browser at **`http://localhost:8000/docs`**.

- `app.py`: Defines the FastAPI application and routes. Handles requests for adding, updating, and deleting tasks.
- `database.py`: Configures the database connection using SQLAlchemy.
- `models.py`: Defines the Todo model using SQLAlchemy.
- `templates/base.html`: Provides the HTML template for rendering the user interface. Includes a form for adding tasks and displays a list of tasks.

<img width="1433" alt="Screenshot 2024-05-10 at 8 33 30 AM" src="https://github.com/pveerrotwal/My-Task-Manager/assets/108364147/ec8be281-3e40-42d6-9574-d9b33fa99ce0">


## **Conclusion**

The FastAPI ToDo App provides a simple yet effective way to manage todo tasks using FastAPI and SQLAlchemy. Users can easily add, update, and delete tasks through a user-friendly web interface.
