# phpdocker81

## Start Docker
```bash
docker-compose up
```

## Destroy and rebuild
```
docker compose up -d --no-deps --build [servicename]
```

## Access shell
docker exec -it phpdocker81-webserver-1 sh

## App address
http://myapp.internal

You should get a "Hello World!" message.

To change, edit the hostname docker-compose.yml
You will also need to edit your local machine's hosts file. In OSX and Linux it's in /etc/hosts.

## Debugging
If you get something like this:
```
Cannot start service mysql: Mounts denied: The paths /sites/blah/... and /sites/blah/... are not shared from OS X and
are not known to Docker.
```
[Check this stack overflow](https://stackoverflow.com/questions/45122459/docker-mounts-denied-the-paths-are-not-shared-from-os-x-and-are-not-known)

If you're using a MySQL GUI client, don't forget to add a user from an address other than localhost. MySQL will add a
localhost user on a new install only, so you'll need to add a user for other locations. The sample below adds a user
from any location:

```mysql
CREATE USER 'root'@'%' IDENTIFIED BY 'root';
GRANT ALL PRIVILEGES ON * . * TO 'root'@'%';
```
