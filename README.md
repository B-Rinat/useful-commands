# Let's Encrypt with Certbot

| Command | Description |
| -------- | ------------- |
| <code>$ certbot certificates</code> | List the Certificates to Find the Certificate Name: Run this command to view all certificates managed by Certbot. This will display a list of certificates, showing the certificate name (under "Certificate Name") for each one. |
| <code>$ certbot renew --dry-run</code> | You the command to test whether the TLS certificate renew is working properly, whether there are any errors in the command, etc., without actually updating. |
| <code>$ certbot renew --cert-name yourdomain.com</code> | Renew the Certificate for a Specific Domain: Once you know the "certificate name", use the `--cert-name` option to renew only that specific certificate. |


