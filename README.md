React + Dockerized
This project uses React , and is set up to run in Docker containers for both development and production environments.

Running in Development Mode
This will allow you to make changes to the code and see them reflected automatically.

Open a terminal in the project root (codin1/codin).

Run the following command:

docker compose -f docker-compose.dev.yml up --build
Open your browser and go to: (http://localhost:7775)

Running in Production Mode
This will build the application and serve it using Nginx.

Open a terminal in the project root (codin1/codin).

Run the following command:

docker compose -f docker-compose.prod.yml up --build
Open your browser and go to: (http://localhost:7775)

Notes
The exposed port is 7775.

To stop the containers, press Ctrl+C in the terminal or run:

docker compose -f docker-compose.dev.yml down
# or for production
docker compose -f docker-compose.prod.yml down
React + Vite
This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

@vitejs/plugin-react uses Babel for Fast Refresh
@vitejs/plugin-react-swc uses SWC for Fast Refresh
Expanding the ESLint configuration
If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the TS template for information on how to integrate TypeScript and typescript-eslint in your project.
