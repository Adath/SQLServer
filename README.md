<p align="center"><img src="microsoft-sql-server.svg" width="400"></p>

<p align="center">Repository containing the queries developed in <a href="https://www.microsoft.com/pt-br/sql-server?rtc=1">👉 SQLServer 👈</a></p>

<p align="center">
    <a href="https://opensource.org/licenses/MIT">
        <img alt="License" src="https://img.shields.io/badge/License-MIT-yellow.svg">
    </a>
    <a href="#">
        <img alt="License" src="https://img.shields.io/github/languages/count/Adath/SQLServer">
    </a>
    <a href="#">
        <img alt="License" src="https://img.shields.io/github/last-commit/Adath/SQLServer">
    </a>
    <a href="#">
        <img alt="License" src="https://img.shields.io/github/followers/Adath?style=social">
    </a>
</p>

<h2 align="center">Website</h2>

<h6 align="center">
    <a href="https://www.microsoft.com/pt-br/sql-server?rtc=1">https://www.microsoft.com/sql-server</a>
</h6>

<h2 align="center">Installation on <img src="microsoft-windows-22.svg" width=100 height=100 alt="Windows"></h2>

```sql
```

<h6 align="center">Login</h6>

```sql
    SQLCMD -S DESKTOP-SQITKN4\SQLEXPRESS -E
```

<h6 align="center">CREATE DATABASE</h6>

```sql
    CREATE DATABASE db

    GO
```

<h6 align="center">CREATE TABLE</h6>

```sql
    CREATE TABLE users (
        id INT NOT NULL IDENTITY(1,1) PRIMARY KEY,
        name VARCHAR(64) NOT NULL,
        username VARCHAR(32) NOT NULL,
        password VARCHAR(32) NOT NULL,
        created_at DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP,
        updated_at DATETIME NULL,
        deleted_at DATETIME NULL,
        sex CHAR(1) NOT NULL CHECK (sex IN ('F', 'M')),
        CONSTRAINT UsersNomeUnique UNIQUE (name),
        CONSTRAINT UsersUserUnique UNIQUE (username),
    );
```

<h6 align="center">DROP TABLE</h6>

```sql
    DROP TABLE users;
```

<h6 align="center">INSERT INTO</h6>

```sql
    INSERT INTO users (name, username, password, sex, deleted_at) VALUES ('Sarah', 'rook', 'XxH$4IlgbjBIZQHnXA^n', 'F', NULL);

    INSERT INTO users (name, username, password, sex, deleted_at) VALUES ('John Doe', 'root', 'dRFAMl#H31DeqkRXglIT', 'M', NULL);

    INSERT INTO users (name, username, password, sex, deleted_at) VALUES ('Bruna', 'jasmin', 'grNo$ZIt3DCRsa%k!%OF', 'F', CURRENT_TIMESTAMP);
```