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
      POSTGRES_DB: mydb
      POSTGRES_USER: myuser
      POSTGRES_PASSWORD: mypassword
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

Time to set sail and start orchestrating your containers with Docker Compose. Happy containerizing! 🐳🎉
