## Hashed Password
```
openssl passwd -apr1 your-password

```
Copy the resulted hash to the .env of Traefik, it need to be inside ''.

## ADMIN_TOKEN

```
echo -n "MySecretPassword" | argon2 "$(openssl rand -base64 32)" -e -id -k 65540 -t 3 -p 4
```
Copy the derived key to the Vaultwarden .env, it need to be inside ''.

