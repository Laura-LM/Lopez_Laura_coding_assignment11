# React + Dockerized

This project uses React , and is set up to run in Docker containers for both development and production environments.

## Running in Development Mode

This will allow you to make changes to the code and see them reflected automatically.

1. Open a terminal in the project root (`codin1/codin`).
2. Run the following command:

   ```sh
   docker compose -f docker-compose.dev.yml up --build
   ```

3. Open your browser and go to: (http://localhost:7775)

## Running in Production Mode

This will build the application and serve it using Nginx.

1. Open a terminal in the project root (`codin1/codin`).
2. Run the following command:

   ```sh
   docker compose -f docker-compose.prod.yml up --build
   ```

3. Open your browser and go to: (http://localhost:7775)

## Notes

- The exposed port is **7775**.
- To stop the containers, press `Ctrl+C` in the terminal or run:

  ```sh
  docker compose -f docker-compose.dev.yml down
  # or for production
  docker compose -f docker-compose.prod.yml down
  ```

---