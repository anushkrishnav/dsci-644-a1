# Dive into Docker Compose: Managing Your Containers Made Easy! 🚢

Now that you've got Docker up and running, it's time to explore the magic of Docker Compose. Docker Compose is your best friend for orchestrating multi-container applications. In this guide, we'll use it to spin up essential services like PostgreSQL, Redis, and pgAdmin. Get ready for some container orchestration fun! 🐋🎶

## Assignment 1: Setting Up PostgreSQL, Redis, and pgAdmin 📝

As a part of Assignment 1, we'll utilize Docker Compose to create services for PostgreSQL, Redis, and pgAdmin. These services will play pivotal roles in your data engineering journey. Before we dive into the details, let's take a look at a sample Docker Compose file:

```yaml
version: '1'

services:
  postgres:
    image: postgres:13.0-alpine
    environment:
      POSTGRES_DB: dsci644db
      POSTGRES_USER: username
      POSTGRES_PASSWORD: password
    ports:
      - "5432:5432"
    volumes:
      - postgres_data:/var/lib/postgresql/data

  redis:
    image: redis:alpine
    ports:
      - "6379:6379"

  pgadmin:
    image: dpage/pgadmin4:latest
    environment:
      PGADMIN_DEFAULT_EMAIL: admin@example.com
      PGADMIN_DEFAULT_PASSWORD: admin
    ports:
      - "80:80"
    depends_on:
      - postgres

volumes:
  postgres_data:

```

### Explanation of the Docker Compose File 📃

- **version:** This specifies the Docker Compose file format version.

- **services:** In this section, we define the services we want to run.

#### PostgreSQL Service 🐘

- **image:** Specifies the PostgreSQL Docker image to use (version 13.0-alpine).

- **environment:** Sets environment variables for PostgreSQL, including the database name, user, and password. Please note that in future assignments, we will use environment variables to handle sensitive information like credentials.

- **ports:** Maps the host machine's port 5432 to the container's port 5432, allowing access to the PostgreSQL service.

- **volumes:** Defines a volume named `postgres_data` to persist PostgreSQL data. Volume mounts like this ensure data persistence and enable you to maintain data across container restarts.

#### Redis Service 🔄

- **image:** Specifies the Redis Docker image to use (alpine version).

- **ports:** Maps the host machine's port 6379 to the container's port 6379, enabling access to the Redis service.

#### pgAdmin Service 📊

- **image:** Specifies the pgAdmin Docker image to use (latest version).

- **environment:** Sets environment variables for pgAdmin, including the default email and password.

- **ports:** Maps the host machine's port 80 to the container's port 80, allowing access to the pgAdmin service.

- **depends_on:** Ensures that the pgAdmin service starts after the PostgreSQL service, allowing seamless database management.

- **volumes:** At the end of the file, we define a volume named `postgres_data`. Volume mounts like this are crucial for data persistence, enabling you to keep your data intact across container restarts and upgrades.

With this Docker Compose file, you can effortlessly spin up these services by running `docker-compose up`. It's containerization made simple!

# Running the Docker Compose File 🐳

To run the Docker Compose file located in the `Tasks/Task_3/` directory, follow these steps:

1. **Navigate to the Directory:** Open your terminal or command prompt.

2. **Change Directory:** Use the `cd` command to navigate to the location where the Docker Compose file is stored. In this case, it's the `Tasks/Task_3/` directory. Here's an example for a Linux/Mac system:
   
   ```bash
   cd path/to/Tasks/Task_3/
   ```

  For Windows, use the following command:

  ```bash
  cd path\to\Tasks\Task_3\
  ```
3. **Run Docker Compose**: Once you are in the correct directory, execute the following command to run the Docker Compose file:

   ```bash
   docker-compose up
   ```

   This command will spin up the PostgreSQL, Redis, and pgAdmin services. You can access the services at the following URLs:

   - **PostgreSQL:** `localhost:5432`
   - **Redis:** `localhost:6379`
   - **pgAdmin:** `localhost:80`

> **Note:** Opening localhost 5432 or 6379 should not give any resource,  opening a URL like http://localhost:5432 in a web browser, you're attempting to access a web service via the HTTP protocol. By default, PostgreSQL doesn't provide a web interface accessible via a web browser on port 5432. Port 5432 is the default port used for PostgreSQL database connections, not for web-based interactions.

   You can also run the Docker Compose file in detached mode by using the `-d` flag:

   ```bash
   docker-compose up -d
   ```

   This command will run the Docker Compose file in the background, allowing you to continue using your terminal.


After Docker Compose up you have to go to the pgAdmin web interface and connect to the PostgreSQL server. You can do this by following these steps:


4. pgAdmin web interface: To access the pgAdmin web interface, go to `localhost:80` in your browser. You can log in with the following credentials:

   - **Email:** admin@example.com
    - **Password:** admin

    Once you log in, you can add a new server by clicking on the "Add New Server" button. Then, enter the following details:

    - **Name:** dsci644db
    - **Host name/address:** postgres
    - **Port:** 5432
    - **Username:** username
    - **Password:** password

    Click on "Save" to save the server. You can now access the PostgreSQL server from the pgAdmin web interface.
  
  Refer this guide for a step-by-step walkthrough of the process: [How to run PostgreSQL and Pgadmin using docker](https://www.commandprompt.com/education/how-to-run-postgresql-and-pgadmin-using-docker/).


5. **Stop Docker Compose:** To stop the Docker Compose file, use the following command:

   ```bash
    docker-compose down
    ```

    This command will stop the Docker Compose file and remove the containers, networks, volumes, and images created by the `docker-compose up` command.


Make sure to upload a screenshot of the terminal output to MyCourses. 📸

With this, you have completed Task 3 and all the tasks in Assignment 1 . Congratulations! 🎉

Moving forward we will be working with the tools and services we have set up in this assignment to automate the data collection process. 🚀

Remember to 
- Stop to all the containers you have started.
- Remove all tokens and keys from your submission.
- Push your changes to GitHub.
- Submit your assignment on MyCourses.
