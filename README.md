# Let's Encrypt with Certbot

| Command | Description |
| -------- | ------------- |
| <code>$ certbot certificates</code> | List the Certificates to Find the Certificate Name: Run this command to view all certificates managed by Certbot. This will display a list of certificates, showing the certificate name (under "Certificate Name") for each one. |
| <code>$ certbot renew --dry-run</code> | You the command to test whether the TLS certificate renew is working properly, whether there are any errors in the command, etc., without actually updating. |
| <code>$ certbot renew --cert-name yourdomain.com</code> | Renew the Certificate for a Specific Domain: Once you know the "certificate name", use the `--cert-name` option to renew only that specific certificate. |
| <code>$ openssl rsa -in jwtRS256.key -pubout -out jwtRS256.key.pub</code> | Generates public key in SPKI format (into file path `jwtRS256.key.pub`) from private key in PEM format (file path `jwtRS256.key`) |
| <code>$ ssh-keygen -t rsa -P '""' -b 2048 -m PEM -f jwtRS256.key</code> | Generates the RSA Private Key in PEM format into `jwtRS256.key` file |
| <code>$ ssh-keygen -e -m PEM -f jwtRS256.key > jwtRS256.key.pub</code> | Generates the RSA Public Key (into `jwtRS256.key.pub`) from Private Key in PEM format (from `jwtRS256.key`) |
| <code>$ mysqldump -u root -p mydatabase > backup_$(date +%Y%m%d_%H%M%S).sql</code> | Backup MySQL database with timestamp and `mysqldump` utility |
| <code>$ mysqldump -u root -p --all-databases > full_backup_$(date +%Y%m%d_%H%M%S).sql</code> | Backup MySQL all database with timestamp and `mysqldump` utility |

