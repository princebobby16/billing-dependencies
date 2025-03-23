# Affinity Project - Docker Setup

## Prerequisites
Before running this setup, ensure you have the following installed:
- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Services
This setup includes the following services:
- RabbitMQ (for messaging)
- MinIO (for object storage)
- PostgreSQL (for the database)

## Running the Services
To start all services, run:
```sh
docker-compose up -d
```

## Stopping the Services
To stop all services, run:
```sh
docker-compose down
```

## PostgreSQL Setup
The PostgreSQL service is configured with the following environment variables:
- **Database Name**: `affinity`
- **User**: `postgres`
- **Password**: `postgres`

To connect to the PostgreSQL database from a client:
```sh
psql -h localhost -p 5432 -U postgres -d affinity
```

To check the logs of the PostgreSQL container:
```sh
docker logs postgres
```

### Accessing MinIO
- Console: [http://localhost:9001](http://localhost:9001)
- API: [http://localhost:9000](http://localhost:9000)
- **Default Access Key**: `minioadmin`
- **Default Secret Key**: `minioadmin`

## RabbitMQ Setup
To access RabbitMQ go to the management UI with Default credentials:
- **Management UI**: [http://localhost:15672](http://localhost:9001)
- **Username**: `guest`
- **Password**: `guest`

## Troubleshooting
If you encounter issues, check container logs with:
```sh
docker-compose logs -f
```
