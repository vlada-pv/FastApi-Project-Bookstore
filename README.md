# Book Selling Platform Announcement

The application written in FastApi is a platform for selling and buying books.

## Useful Information 

A **Makefile** with useful commands has been added to the repository. The commands are called in the console in this way:

```shell
make linters

make install_reqs
```
## Application Launch

Commands are executed in the console: 

1. Copy project. Start work with changing file .env.example to .env
2. Deploying Postgres DB in a docker container
```shell
make up_compose
```
3. Installing dependencies for the FastAPI server
```shell
make install_reqs
```
4. Starting the FastAPI server
```shell
uvicorn src.main:app --reload
```

## Project Structure

For convenience and adherence to the principles of clean architecture, the project is divided into the following packages:

- `configurations` — layer for storing configurations, constants, parameters, and project settings

- `models` — layer for storing models (ORM or Data Classes)

- `routers` — layer for setting URLs for different endpoints

- `schemas` — layer containing pydantic schemes, responsible for serialization and validation
