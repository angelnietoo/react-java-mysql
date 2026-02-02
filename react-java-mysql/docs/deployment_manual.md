# Steps for Application Deployment

# 1. Credential Preparation: Create the db/ directory and inside it a file named password.txt containing the database password so Docker’s secrets system can recognize it.

# 2. Proxy Configuration: Make sure the proxy/nginx.conf file points to port 3000 for the frontend service and to port 8080 for the backend.

# 3. Build and Launch: Run docker compose up -d --build to compile the Java and React source code, build the custom images, and bring up the four containers simultaneously.

# 4. Health Check: Verify that all services are running with docker compose ps, ensuring the mysql-db container shows a (healthy) status.

# 5. Accessing the Application: Open your browser at http://localhost. Traffic will enter through the Reverse Proxy on port 80 and be routed internally to the appropriate services.