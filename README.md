# FastAPI Todo List Application

A full-stack todo list application built with FastAPI, SQLAlchemy, and SQLite. This application includes user authentication, todo management, and a web interface.

## Features

- User registration and authentication
- Create, read, update, and delete todos
- User-specific todo lists
- Web interface with Bootstrap styling
- SQLite database for data persistence

## Requirements

- Python 3.7+
- UV package manager (recommended) or pip

## Installation

1. Clone the repository:
```bash
git clone https://github.com/code-wizard/fastapi-fullstack-tod-list.git
cd fastapi-fullstack-tod-list
```

2. Install dependencies:

### Using UV (recommended):
```bash
uv pip install -r requirements.txt
```

### Using pip:
```bash
pip install -r requirements.txt
```

## Required Dependencies

The application requires the following packages:
- fastapi
- uvicorn
- sqlalchemy
- jinja2
- python-multipart
- passlib
- python-jose
- bcrypt
- aiosqlite

## Running the Application

1. Start the FastAPI server:
```bash
uvicorn main:app --reload
```

2. The application will be available at:
   - **Main application**: http://127.0.0.1:8000
   - **API documentation**: http://127.0.0.1:8000/docs
   - **Alternative API docs**: http://127.0.0.1:8000/redoc

## Database

The application uses SQLite as the database. The database file (`todos.db`) will be created automatically when you first run the application.

## Project Structure

```
├── main.py              # FastAPI application entry point
├── database.py          # Database configuration and connection
├── models.py           # SQLAlchemy models
├── requirements.txt    # Python dependencies
├── routers/
│   ├── auth.py         # Authentication routes
│   └── todos.py        # Todo management routes
├── static/             # Static files (CSS, JS)
│   └── todo/
├── templates/          # HTML templates
└── todos.db           # SQLite database (created automatically)
```

## Usage

1. **Register a new account**: Navigate to the registration page to create a new user account
2. **Login**: Use your credentials to log into the application
3. **Manage todos**: Create, edit, and delete your personal todo items
4. **View todos**: See all your todos in an organized list format

## API Endpoints

- `GET /` - Redirects to todos page
- `POST /auth/register` - User registration
- `POST /auth/` - User login
- `GET /todos/` - View todos
- `POST /todos/add-todo` - Create new todo
- `GET /todos/edit-todo/{todo_id}` - Edit todo page
- `POST /todos/edit-todo/{todo_id}` - Update todo
- `GET /todos/delete/{todo_id}` - Delete todo

## Development

To run the application in development mode with auto-reload:

```bash
uvicorn main:app --reload --port 8000
```

## Troubleshooting

- **Port already in use**: If port 8000 is busy, use a different port:
  ```bash
  uvicorn main:app --reload --port 8001
  ```

- **Module not found errors**: Make sure all dependencies are installed:
  ```bash
  uv pip install fastapi uvicorn sqlalchemy jinja2 python-multipart passlib python-jose bcrypt
  ```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This project is open source and available under the MIT License.
