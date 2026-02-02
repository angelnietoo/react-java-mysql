# 1. Start the system by running docker compose up -d --build to build the images and launch all services in the background.

# 2. Use docker compose ps to check that the database healthcheck is correct and that all services are in a Healthy state.

# 3. If a 502 Bad Gateway error appears, inspect the logs with docker compose logs -f to verify port synchronization and identify the source of the problem.

# 4. Apply the necessary changes to the Reverse Proxy configuration file and run docker compose restart reverse-proxy to reload the proxy without stopping the rest of the infrastructure.

# 5. When environment variables or secrets are modified, run docker compose down and then start the system again to ensure that the Backend and the Database reload the credentials securely.