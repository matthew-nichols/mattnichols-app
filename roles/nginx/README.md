nginx/tls role
=========

A role to handle nginx installation/configuration with TLS (Let's Encrypt or
self-signed).

Role Variables
--------------

nginx_letsencrypt_email: email for ACME process. Required

nginx_certificates:
  - cert_name: a certificate name, used for certbot --cert-name and nginx_websites
    domains:
      - example.com
      - www.example.com

nginx_websites:
  - cert_name: a certificate name, used for certbot --cert-name and nginx_websites
    domain: only a single domain is supported and is required to support TLS
    directory: /srv/website
  - cert_name: main
    domain: non.canonical.com
    redirect_domain_301: canonical.com

nginx_resolver: defaults to 8.8.8.8, used by nginx in resolver directive (for OCSP stapling and upstream servers)