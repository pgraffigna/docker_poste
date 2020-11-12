# docker_poste

Docker-compose para desplegar un servidor de correo con POSTE.

---
### notas
registros DNS:
- A @ IP
- A mail IP
- MX @ mail.DOMINIO
- TXT @ "v=spf1 ipv4:IP ~all" 
- CNAME DOMINIO
- TXT dkim._domainkey v=DKIM1; k=rsa; p=PUBLIC_DKIM_KEY;
- TXT _dmarc v=DMARC1; p=quarantine;

- https://DOMINIO/admin/login
- https://DOMINIO/webmail/
- https://DOMINIO/admin/install/server
