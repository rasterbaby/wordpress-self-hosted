# WordPress Self-Hosted with Docker

This repository provides a `docker compose` setup to run a self-hosted [WordPress](https://wordpress.org/) instance, complete with a [MySQL](https://www.mysql.com/) database, [phpMyAdmin](https://www.phpmyadmin.net/), and [WP-CLI](https://wp-cli.org/).

It is pre-configured to join a shared Docker network, allowing easy integration with other services like [n8n](https://github.com/AiratTop/n8n-self-hosted).

## Features

-   Uses official Docker images for **WordPress**, **MySQL**, **phpMyAdmin**, and **WP-CLI**.
-   Includes a full-featured environment for development and management.
-   Persists WordPress files and MySQL data in local volumes (`./data/wp` and `./data/wp-db`).
-   Pre-configured for a shared network for easy inter-service communication.
-   Includes helper scripts for easy management (`restart-docker.sh`, `update-docker.sh`).
-   Includes a `backup.sh` script for creating compressed database backups.
-   Includes a sample `Caddyfile` for use with a reverse proxy.

## Getting Started

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/AiratTop/wordpress-self-hosted.git
    cd wordpress-self-hosted
    ```

2.  **Create the shared network:**
    If it doesn't exist yet, create the shared Docker network:
    ```bash
    docker network create shared_network
    ```

3.  **Configure environment variables:**
    Create a `.env` file and specify your database credentials.

4.  **Start the services:**
    ```bash
    docker compose up -d
    ```

## Accessing Services

-   **WordPress:** [http://localhost:8888](http://localhost:8888)
-   **phpMyAdmin:** [http://localhost:8081](http://localhost:8081)

## Usage

-   **Start:** `docker compose up -d`
-   **Stop:** `docker compose down`
-   **Restart:** `./restart-docker.sh`
-   **Update:** `./update-docker.sh` (Pulls the latest Docker images and restarts)
-   **Backup:** `./backup.sh` (Creates a compressed backup in the `backups` directory)
-   **WP-CLI:** Use `docker compose exec wp-cli wp <command>`. For example:
    ```bash
    # List installed plugins
    docker compose exec wp-cli wp plugin list
    ```

## Connecting with n8n

This setup is designed to work with the [n8n-self-hosted](https://github.com/AiratTop/n8n-self-hosted) configuration. Since both services are on the `shared_network`, you can connect to MySQL from n8n using the following credentials:

-   **Host:** `wp-db`
-   **Port:** `3306`
-   **Database, User, Password:** (As specified in your `.env` file)

## See Also

Check out other self-hosted solutions:

-   [postgresql-self-hosted](https://github.com/AiratTop/postgresql-self-hosted)
-   [mysql-self-hosted](https://github.com/AiratTop/mysql-self-hosted)
-   [clickhouse-self-hosted](https://github.com/AiratTop/clickhouse-self-hosted)
-   [qdrant-self-hosted](https://github.com/AiratTop/qdrant-self-hosted)
-   [redis-self-hosted](https://github.com/AiratTop/redis-self-hosted)
-   [n8n-self-hosted](https://github.com/AiratTop/n8n-self-hosted)
-   [caddy-self-hosted](https://github.com/AiratTop/caddy-self-hosted)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Author

**Airat Halitov**

- Website: [airat.top](https://airat.top)
- GitHub: [@AiratTop](https://github.com/AiratTop)
- Repository: [wordpress-self-hosted](https://github.com/AiratTop/wordpress-self-hosted)