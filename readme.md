# Pimcore Docker Compose
Docker compose for Pimcore 5

## Containers
- PHP 7.3
- MariaDB 10
- Nginx
- Redis

## Getting Started
### Requirements
- git
- composer
- docker/docker-compose

## Installation
Create a new project
```bash
COMPOSER_MEMORY_LIMIT=-1 composer create-project pimcore/skeleton:dev-master pimcore
```

Start the containers
```bash
docker-compose up -d
```

Setup the project
```bash
docker exec -it pimcore-php bash
```
```bash
./vendor/bin/pimcore-install --mysql-host-socket=db --mysql-username=pimcore --mysql-password=pimcore --mysql-database=pimcore
```

## Usage
- Frontend: [localhost:8888](http://localhost:8888)
- Backend: [localhost:8888/admin](http://localhost:8888/admin)
