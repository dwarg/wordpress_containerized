# GENEROWANIE CERTYFIKATÓW
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout ssl/nginx.key -out ssl/nginx.crt

# INFO
Optionally, a private network visible only to the containers could be created

nginx:
  [...]
  networks:
  - mynetwork

networks:
 mynetwork:
 driver: bridge
