# Docker

Docker is actually really easy to use. I would highly recommend the use of Docker-Compose over Docker Desktop.

## Docker Desktop

For Windows this requires the installation of WSL2.

## Docker-Compose

- Compose files are written in YAML, and define the containers, their parameters, and how they operate
- To run a compose file, use `docker-compose up -d`

### SQL Server

#### Volumes & Persisting Data

In theory, you're using this to run a SQL Server instance, so naturally you'll want to persist your data. Doing so is actually pretty easy.  
You just need to utilize volumes.

#### Sample SQL Server Compose File

```yml
version: "3.3"

services:
  sqlserver:
    container_name: sqlserver
    image: mcr.microsoft.com/mssql/server:2019-latest
    hostname: sqlserver
    ports:
      - "1433:1433"
    environment:
      ACCEPT_EULA: "Y"
      MSSQL_PID: "Developer"
      SA_PASSWORD: "passwordgoeshere"
    volumes:
      - "sql-data:/var/opt/mssql/data"
      - "sql-data:/var/opt/mssql/log"
      - "sql-data:/var/opt/mssql/secrets"

volumes:
  sql-data:
```

**File Breakdown:**

| Element                                     | Meaning                                                     |
| ------------------------------------------- | ----------------------------------------------------------- |
| ACCEPT_EULA                                 | End User Licence Agreement Acceptance Confirmation          |
| MSSQL_PID                                   | Version of SQL Server to Run (see licencing)                |
| SA_PASSWORD                                 | Sysadmin Password                                           |
| volumes: "sql-data:/var/opt/mssql/data"     | Location to map the SQL Data to                             |
| volumes: "sql-data:/var/opt/mssql/log"      | Location to map the SQL Logs to                             |
| volumes: "sql-data:/var/opt/mssql/secrets"  | Location to map secrets to                                  |
| volumes: sql-data:                          | Create/map the volume for SQL data                          |

#### Restoring Databases using T-SQL

```sql

```

## Docker Hub

Has a pull limit of 100 per hour unless you have an account!
