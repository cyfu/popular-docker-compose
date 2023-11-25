
## Build and Start Keycloak

```bash
# Use docker build command to create an image
docker build --build-arg KEYCLOAK_VERSION=21.1.1 -t mykeycloak --progress=plain --no-cache .

# Or use docker compose build command to create an image
docker compose build --no-cache keycloak

# Start up keycloak and postgresql
docker compose up -d

# Show container status
docker compose ps

# Check container logs
docker compose logs keycloak
```

To access keycloak, open your browser in incognito mode and access the following URL:
http://127.0.0.1:8380/

Login to the admin console with the username `admin` and password `password`

To access postgresql using the pgadmin4, open your browser in incognito mode and access the follow URL:
http://127.0.0.1:5050/

Login to the admin console with the useranme `$PGADMIN_MAIL` and password `$PGADMIN_PW`

## Reference:
[Run Keycloak in docker with extenal DB](https://medium.com/@ozbillwang/run-keycloak-in-docker-with-extenal-db-1b504ad00eae)

[Keycloak image tags](https://quay.io/repository/keycloak/keycloak?tab=tags&tag=latest)
