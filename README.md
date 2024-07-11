# Task Tracker API
## Backend Developer (Django Rest) Technical Task

- ### Task Description
Develop an API that will allow users to register, create tasks and receive analytics of their performance based on the tasks they have completed.

- ### Requirements
1. Models:
    - TaskItem: A model that represents a task.
        - Fields: Name, Description, Priority (Low, Medium, High), Due Date.
    TaskRecord: A record of a user completing a task.
        - Fields: User, TaskItem, Date Completed, Time Taken (in minutes).
2. API Endpoints:
    - CRUD for TaskItem:
        - Create: POST /api/task/
        - Task List: GET /api/task/
        - Task Detail: GET /api/task/{id}/
        - Update: PUT /api/task/{id}/
        - Delete: DELETE /api/task/{id}/
    - CRUD for TaskRecord:
        - Create: POST /api/task_record/
        - TaskRecord List: GET /api/task_record/
        - TaskRecord Detail: GET /api/task_record/{id}/
        - Update: PUT /api/task_record/{id}/
        - Delete: DELETE /api/task_record/{id}/
    - Analytics:
        - Daily: GET /api/summary/daily/
            - Returns the number of tasks completed, average time taken to complete tasks, and distribution of tasks by priority for the current day.
            - Add filters for days
3. Authentication:
    - Users should be able to register and login - use JWT for authentication.
    - Only authenticated users should be able to manage tasks and view analytics.
    - Users should only be able to view their own tasks and analytics.
4. Additional Requirements:
    - Write tests for the API.
    - Add API documentation using Swagger or Redoc.
    - Use Django Rest Framework.
    - Use Django ORM for database operations.
    - Use PostgreSQL for the database.
