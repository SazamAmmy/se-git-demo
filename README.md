# se-git-demo
Demonstration on how to use git collaboratively

Add a change
Another change
change more things
Add another change

Project Overview: This project is structured to run a Node.js web application within Docker containers, making use of a MySQL database for data storage.The application's source code is located in the "src" directory, and database setup files are in the "data" directory.

Key Components

- Dockerfile: Located in the "src" directory, it specifies how to build the Docker image for the Node.js application. It uses Node.js as the base image and sets up the working directory within the container.

- docker-compose.yml: This file (located at the root of the extracted directory) defines the services, networks, and volumes for the
application. Running "docker-compose up" will start your entire application as specified in this file.

- Data Directory: Contains the "world.sql" file, a MySQL dump file, which is presumably used to set up your application's database schema and initial data.

- Src Directory: Contains the application's source code, including:
  - ".dockerignore" and ".gitignore" for ignoring "node_modules" in Docker builds and Git respectively.
  - "index.js" as the entry point for the Node.js application, utilizing "express" for web server functionality and "mysql2" for database interactions.
  - "package.json" and "package-lock.json" for managing project dependencies.
  - "static" subdirectory for static assets like CSS files ("gallery.css" and "style.css"), which style the web application.

Steps to Run the Project

1. Open the Project in Visual Studio Code: Navigate to the extracted project directory and open it in Visual Studio Code to begin working on it.

2. Install Dependencies: Run "npm install" within the "src" directory to install necessary Node.js dependencies specified in "package.json".

3. Docker Compose Up: In the terminal, run "docker-compose up" from the root directory (where "docker-compose.yml" is located) to start your application. Docker Compose will read the "docker-compose.yml" file to start and run the configured services.

4. Accessing Your Application: Once the Docker containers are up and running, you can access your web application by navigating to the specified host port mapped to the application's port in a web browser.

5. Development and Testing: Make changes to your application's code in the "src" directory as needed. You can test your application by accessing it through a browser and using tools like Postman for API testing or directly interacting with the MySQL database.
