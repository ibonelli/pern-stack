# PERN Stack

The PERN Stack is an acronym for Postgres, Express, React, Node. It's a set of tools to create a complete web application.

To understand this project, I recommend that you could know these tolls:

* Postgres
* Express
* React
* Node

And this other technologies and libraries That I Use in this project:

* Material UI
* Docker

### Installation

This project consists in a *Web Frontend Application* and a *Web Backend Application*.

First, clone the repo:

```bash
git clone https://github.com/FaztWeb/pern-stack
```

To run Postgres you can use docker:

```bash
cd pern-stack
docker-compose up
```

After running postgres you can configure the DB access. In the ```src/config.js``` file add:

```js
	password: process.env.DB_PASSWORD || "faztpassword",
```

By default the DB user in the [dockerized image](https://hub.docker.com/_/postgres/) is "postgres" and the password configured in the ```docker-compose.yml``` is "faztpassword".

To run the backend (in the root directory of the repository):

```bash
npm install
npm start
```

to run the frontend:

```bash
cd client
npm install
npm start
```

On a browser you can now visit:

- http://localhost:3000 for the frontend client React App.
- http://localhost:4000/tasks to check the backend (will return a JSON).
- http://localhost:8080/browser/ to access postgres administration.

To get the postgress usr/psw check in the ```docker-compose.yml``` file the ```ui > environment``` section. It will have the PGADMIN_DEFAULT_EMAIL & PGADMIN_DEFAULT_PASSWORD.
