<h1 id="top" align="center">pgAdmin</h1>

<br>

<div align="center">
    <img height=120 src="assets/banner.png">
</div>

<br>

## 🔍 Table of Contents

- [About Project](#intro)
- [Technologies](#technologies)
- [Features](#features)
- [Releases](#releases)
- [System Startup](#system-startup)
- [Contributors](#contributors)

<br/>

<h2 id="intro">📌 About Project</h2>

This project simplifies the deployment of pgAdmin, using Docker Compose. It provides pre-configured `.env` variable configurations.

<br/>

<h2 id="technologies">☄️ Technologies</h2>

&nbsp; [![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)

&nbsp; [![pgAdmin](https://img.shields.io/badge/pgadmin-316192?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.pgadmin.org/)

&nbsp; [![.Env](https://img.shields.io/badge/.ENV-ECD53F.svg?style=for-the-badge&logo=dotenv&logoColor=black)](https://www.ibm.com/docs/bg/aix/7.2?topic=files-env-file)

<br/>

<h2 id="features">🔥 Features</h2>

- **Docker Containerization:** The application is containerized using Docker to ensure consistent deployment, scalability, and isolation across different environments.
- **Docker Compose Deployment:** Simplifies deployment with Docker Compose configuration, enabling easy setup and service orchestration without complex commands.
- **Network Compatibility:** Uses shared Docker network to work with other services.
- **Persistent Data:** Utilizes a named Docker volume to ensure persistent storage of application data, allowing data to persist across container restarts, rebuilds, and removals.
- **Bind Mount Backup Directory:** Enables persistent data storage and backup using a bind mount directory.
- **.env Configuration:** All environment variables are easily configurable using the `.env` file, simplifying configuration management.

<br/>

<h2 id="releases">🚢 Releases</h2>

&nbsp; [![.](https://img.shields.io/badge/2.1.0-233838?style=flat&label=version&labelColor=111727&color=1181A1)](https://github.com/ahmettoguz/database-pgadmin/tree/v2.1.0)

&nbsp; [![.](https://img.shields.io/badge/2.0.0-233838?style=flat&label=version&labelColor=111727&color=1181A1)](https://github.com/ahmettoguz/database-pgadmin/tree/v2.0.0)

&nbsp; [![.](https://img.shields.io/badge/1.0.0-233838?style=flat&label=version&labelColor=470137&color=077521)](https://github.com/ahmettoguz/database-pgadmin/tree/v1.0.0)

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
nano .env
```

- Create `network-database` network if not exists.

```
docker network create network-database
```

- Run container.

```
docker stop                      database-pgadmin-c
docker rm                        database-pgadmin-c
docker volume rm                 volume-pgadmin
docker compose -p database up -d pgadmin
docker logs -f                   database-pgadmin-c
```

- Once the UI is accessible, register a new server.

- Under the General tab, set the name to `postgresql`.

- Under the Connection tab, set the Host name to `postgresql`.

- When create a backup, the file will be saved in the backup directory specified by the path in the `.env` file.

- Refer to [`Postgresql Initializer`](https://github.com/ahmettoguz/database-initializer-postgresql) repository to easily initialize and reset the database using SQL scripts.

- Refer to [`Traefik`](https://github.com/ahmettoguz/proxy-traefik) repository to launch reverse proxy to access the pgAdmin dashboard via subdomain.

<br/>

<h2 id="contributors">👥 Contributors</h2>

<a href="https://github.com/ahmettoguz" target="_blank"><img width=60 height=60 src="https://avatars.githubusercontent.com/u/101711642?v=4"></a>

### [🔝](#top)
