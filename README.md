<h1 id="top" align="center">Core pgAdmin</h1>

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

The core pgAdmin project focuses on building a pgAdmin image for managing PostgreSQL databases using microservice architecture.

<br/>

<h2 id="technologies">☄️ Technologies</h2>

&nbsp; [![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)

&nbsp; [![pgAdmin](https://img.shields.io/badge/pgadmin-316192?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.pgadmin.org/)

<br/>

<h2 id="features">🔥 Features</h2>

- **Docker Containerization:** The application is containerized for consistent deployment and scaling.
- **Bind Mount Backup Directory:** Enables persistent data storage and backup using a bind mount directory.
- **Docker Compose Deployment:** Simplified deployment with `docker-compose`, using `.env` configuration for easy customization without long commands.

<br/>

<h2 id="releases">🚢 Releases</h2>

&nbsp; [![.](https://img.shields.io/badge/1.0.0-233838?style=flat&label=version&labelColor=470137&color=077521)](https://github.com/ahmettoguz/core-pgadmin/tree/v1.0.0)

<br/>

<h2 id="system-startup">🚀 System Startup</h2>

- Create a new directory named `core`.
- Clone the `core-docker-config` and `core-pgadmin` repositories into the `core` directory.

```
git clone https://github.com/ahmettoguz/core-docker-config
git clone https://github.com/ahmettoguz/core-pgadmin
```

- Refer to the documentation provided in the [`core-docker-config`](https://github.com/ahmettoguz/core-docker-config) project for the system startup commands.

<br/>

<h2 id="contributors">👥 Contributors</h2>

<a href="https://github.com/ahmettoguz" target="_blank"><img width=60 height=60 src="https://avatars.githubusercontent.com/u/101711642?v=4"></a>

### [🔝](#top)
