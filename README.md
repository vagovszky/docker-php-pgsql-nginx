# docker-php-pgsql-nginx
Docker composed image containing php-fpm, postgres and nginx

# Usage
`docker-compose up`

Working directory is *application*

# Available ports
- 80 - Nginx HTTP
- 5432 - Postgres

# Configuration
Each service ahas its own configuration.
To run SQL on image initialization - put your SQL under docker/postgres/configuration/init.sql
In case of troubles with SELINUX and mounting volumes use this "hack" - put :Z or :z at the end on the volume mount directive in docker-compose.yml

Example:
- Before: - ./application/:/var/www/html
- After: - ./application/:/var/www/html:Z 
