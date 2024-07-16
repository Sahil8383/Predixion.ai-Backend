# Backend - FastAPI

## Setup Instructions

### Prerequisites

- Python 3.8 or higher
- Virtual environment tool (venv, virtualenv, conda, etc.)
- SQLite (for development purposes)
- Git (for version control)

### Installation

1. **Clone the repository:**

    ```sh
    git clone https://github.com/yourusername/yourproject.git
    cd yourproject/backend
    ```

2. **Create and activate a virtual environment:**

    ```sh
    python -m venv env
    source env/bin/activate  # On Windows, use `env\Scripts\activate`
    ```

3. **Install dependencies:**

    ```sh
    pip install -r requirements.txt
    ```

4. **Set up the database:**

    ```sh
    python -c "from database import Base, engine; Base.metadata.create_all(bind=engine)"
    ```

5. **Run the application:**

    ```sh
    uvicorn main:app --reload
    ```

### Endpoints

- `GET /api/tasks`: Retrieve all tasks
- `POST /api/tasks`: Create a new task
- `PUT /api/tasks/{task_id}`: Update a task's status
- `DELETE /api/tasks/{task_id}`: Delete a task

### CORS Configuration

The backend is configured to allow requests from the frontend URL. Make sure to update the CORS origins list if needed.

```python
origins = [
    "http://localhost:3000",
    "https://predixion-ai-frontend.vercel.app"
]
