# Docker Compose

The docker compose file is called: `docker-compose.yml`, and it looks like this:

```
version: "3.8"

services:
    app:
        image: platziapp
        environment:
            MONGO_URL: "mongodb://db:27017/test"
        depends_on:
            - db
        ports:
            - "3000:3000"
        volumes:
    db:
        image: mongo

```