Dockerized Strapi Application with PostgreSQL and Nginx

Description:
This pull request adds a fully Dockerized Strapi application integrated with PostgreSQL as the database and Nginx as a reverse proxy. The setup allows for seamless local development, testing, and deployment with minimal configuration.

Strapi Application
Dockerized Strapi backend.
Configured environment variables for database connection, admin path, and telemetry settings.
Includes automated admin panel build during container startup.

PostgreSQL Database
Dockerized PostgreSQL container.
Persistent volume setup for data storage.
Environment variables for user, password, and database configuration.

Nginx Reverse Proxy
Dockerized Nginx setup as a reverse proxy for Strapi.
Configured to route / and /admin requests to the Strapi container.
Handles connection errors gracefully with proper upstream configuration.

Docker Compose Setup
Multi-container orchestration for Strapi, PostgreSQL, and Nginx.
Ensures proper startup order with dependency management (depends_on).
Ready-to-use docker-compose.override.yml for local development.
