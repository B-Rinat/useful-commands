# Docker

| Command | Description |
| -------- | ------------- |
| <code>$ docker ps</code> | List only running docker containers (CONTAINER_ID, IMAGE, COMMAND, CREATED, STATUS, PORTS, NAMES) |
| <code>$ docker ps -a</code> | List all running and stopped docker containers (CONTAINER_ID, IMAGE, COMMAND, CREATED, STATUS, PORTS, NAMES) |
| <code>$ docker restart NAME/CONTAINER_ID</code> | Restart docker container with CONTAINER_ID, data does not vanish. Combination of 2 commands `docker stop` and `docker start` |
| <code>$ docker stop NAME/CONTAINER_ID</code> | Stop docker container with CONTAINER_ID, data does not vanish. |
| <code>$ docker start NAME/CONTAINER_ID</code> | Start docker container with CONTAINER_ID, data does not vanish. |
| <code>$ docker logs --tail 100 NAME/CONTAINER_ID</code> | Inspect the last 100 lines of the logs with CONTAINER_ID |
| <code>$ docker inspect NAME/CONTAINER_ID</code> | Retrieving low-level information about Docker objects (by default in JSON array format). Provides a comprehensive view of various Docker constructs (Container: ID, name, Mounted volumes and bind mounts, Log path, Network settings, CPU, memory; Images; Networks; Volumes; etc.) |

# Linux Commands

| Command | Description |
| -------- | ------------- |
| <code>$ mv PATH_TO_FILE PATH_TO_FOLDER_TO_MOVE</code> | Moves file into directory. The file will disappear from original PATH_TO_FILE file path and be moved to PATH_TO_FOLDER_TO_MOVE directory |
| <code>$ ls -l path/to/directory</code> | Lists contents of the directory without actually changing directory. Good for quick inspection |
| <code>$ netstat -tulpn | grep ":PORT"</code> | lists all processes/programs PID that listen on port PORT (ex, 18084) |


# Let's Encrypt with Certbot

| Command | Description |
| -------- | ------------- |
| <code>$ certbot certificates</code> | List the Certificates to Find the Certificate Name: Run this command to view all certificates managed by Certbot. This will display a list of certificates, showing the certificate name (under "Certificate Name") for each one. |
| <code>$ certbot renew --dry-run</code> | You the command to test whether the TLS certificate renew is working properly, whether there are any errors in the command, etc., without actually updating. |
| <code>$ certbot renew --cert-name yourdomain.com</code> | Renew the Certificate for a Specific Domain: Once you know the "certificate name", use the `--cert-name` option to renew only that specific certificate. |

# Key Generation & Management (openssl, ssh-keygen, ...)

| Command | Description |
| -------- | ------------- |
| <code>$ openssl rsa -in jwtRS256.key -pubout -out jwtRS256.key.pub</code> | Generates public key in SPKI format (into file path `jwtRS256.key.pub`) from private key in PEM format (file path `jwtRS256.key`) |
| <code>$ ssh-keygen -t rsa -P '""' -b 2048 -m PEM -f jwtRS256.key</code> | Generates the RSA Private Key in PEM format into `jwtRS256.key` file |
| <code>$ ssh-keygen -e -m PEM -f jwtRS256.key > jwtRS256.key.pub</code> | Generates the RSA Public Key (into `jwtRS256.key.pub`) from Private Key in PEM format (from `jwtRS256.key`) |

# Databases (Mysql, Postgre, etc.)

| Command | Description |
| -------- | ------------- |
| <code>$ mysqldump -u root -p mydatabase > backup_$(date +%Y%m%d_%H%M%S).sql</code> | Backup MySQL database with timestamp and `mysqldump` utility |
| <code>$ mysqldump -u root -p --all-databases > full_backup_$(date +%Y%m%d_%H%M%S).sql</code> | Backup MySQL all database with timestamp and `mysqldump` utility |

