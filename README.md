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

# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.
