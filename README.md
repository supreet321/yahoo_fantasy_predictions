# Yahoo Fantasy Basketball Predictions

This project uses Yahoo Fantasy API to make recommendations for fantasy basketball moves for your league.

## Setup

- Install Docker Desktop (which installs docker and docker-compose) https://www.docker.com/
- The in the repo root, run `docker-compose up`
- Navigate to `localhost:8000` in your browser to access the backend API

## Project Structure

- `root` - Contains the docker-compose file
  - `docker-compose` contains information about the different services required for this app to work and how to start them.
  - `backend` - Contains the backend API and the Dockerfile
    - `Dockerfile` - Contains the instructions for building the backend image
    - `api` folder is where the django project lives
  - `frontend` - Contains the frontend app and the Dockerfile
    - `Dockerfile` - Contains the instructions for building the frontend image
    - `src` folder is where the frontend react app lives
