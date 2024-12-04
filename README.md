# FastAPI GraphQL API with Strawberry

This project is a simple GraphQL API built using FastAPI and Strawberry. The API provides movie data including the title and director of several movies.

## Features
- GraphQL endpoint available at `/graphql` to query for movie data.
- Basic REST endpoint at `/` to test server connectivity.

## Prerequisites
- Python 3.12 installed.
- `pip` to manage packages.

## Installation

1. Clone this repository or download the files.
2. Navigate to the project directory:
   ```sh
   cd go-GraphQL
   ```
3. Create a virtual environment:
   ```sh
   python -m venv venv
   ```
4. Activate the virtual environment:
   - On Windows (Command Prompt):
     ```sh
     venv\Scripts\activate
     ```
   - On Windows (PowerShell):
     ```sh
     .\venv\Scripts\Activate
     ```
   - On MacOS/Linux:
     ```sh
     source venv/bin/activate
     ```
5. Install the required dependencies:
   ```sh
   pip install fastapi strawberry uvicorn
   ```

## Running the Application

1. With the virtual environment activated, run the server:
   ```sh
   python main.py
   ```
   Alternatively, you can use `uvicorn` to run the application:
   ```sh
   uvicorn main:app --host 0.0.0.0 --port 8000
   ```
2. The server will be available at `http://127.0.0.1:8000`.

## Usage of the API

### GraphQL Endpoint
- Visit the `/graphql` endpoint to interact with the GraphQL API.
- You can query for a list of movies with the following query:
  ```graphql
  query {
    movies {
      title
      director
    }
  }
  ```

### REST Endpoint
- Visit `/` to receive a simple welcome message.
- Example response:
  ```json
  {
    "message": "Welcome to the GraphQL API"
  }
  ```

## Deactivating the Virtual Environment

When you are done working, you can deactivate the virtual environment with:
```sh
deactivate
```

## License
This project is distributed under the MIT license.
