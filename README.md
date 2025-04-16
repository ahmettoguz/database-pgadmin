<h1 id="top" align="center">pgAdmin <br/> 🚢 v2.0.0 🚢</h1>

<br>

<div align="center">
    <img height=120 src="assets/banner.png">
</div>

<br>

## 🔍 Table of Contents

- [Features](#features)
- [System Startup](#system-startup)

<br/>

<h2 id="features">🔥 Features</h2>

- **Docker Containerization:** The application is containerized using Docker to ensure consistent deployment, scalability, and isolation across different environments.
- **Docker Compose Deployment:** Simplifies deployment with Docker Compose configuration, enabling easy setup and service orchestration without complex commands.
- **Network Compatibility:** Uses shared Docker network to work with other services.
- **Persistent Data:** Binds the data directory from the host machine to the container, ensuring persistent data storage even with container restarts.
- **Bind Mount Backup Directory:** Enables persistent data storage and backup using a bind mount directory.
- **.env Configuration:** All environment variables are easily configurable using the `.env` file, simplifying configuration management.

<br/>

<h2 id="system-startup">🚀 System Startup</h2>

- Refer to [`PostgreSQL`](https://github.com/ahmettoguz/database-postgresql) repository to launch PostgreSQL database.

- Create a new directory named `database`.

```
mkdir database
cd database
```

- Clone project.

```
git clone https://github.com/ahmettoguz/database-pgadmin
cd database-pgadmin
```

- Create `.env` file based on the `.env.example` file with credentails.

```
cp .env.example .env
```

- Create `network-database` network if not exists.

```
docker network create network-database
```

- Run container.

```
docker stop                      database-pgadmin-c
docker rm                        database-pgadmin-c
docker compose -p database up -d pgadmin
docker logs -f                   database-pgadmin-c
```

- Once the UI is accessible, register a new server.

- Under the General tab, set the Name to `postgresql`.

- Under the Connection tab, set the Host name to `postgresql`.

- When create a backup, the file will be saved in the backup directory specified by the path in the .env file.

- Refer to [`Initializer-Postgresql`](https://github.com/ahmettoguz/database-initializer-postgresql) repository to easily initialize and reset the database using SQL scripts.

- Refer to [`Traefik`](https://github.com/ahmettoguz/proxy-traefik) repository to launch reverse proxy to access the pgAdmin dashboard via a custom domain and path.

<br/>

### [🔝](#top)
