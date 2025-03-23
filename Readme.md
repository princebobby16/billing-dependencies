# Docker Compose for RabbitMQ and MinIO

## Prerequisites
Before running this setup, ensure you have the following installed:
- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Services
This `docker-compose.yml` file sets up the following services:

1. **RabbitMQ**: A message broker used for asynchronous communication.
2. **MinIO**: A high-performance object storage server.

## Usage

### Start the Services
Run the following command to start the services:
```sh
docker-compose up -d
```

### Stop the Services
To stop the running services, use:
```sh
docker-compose down
```

### Accessing RabbitMQ
- Management UI: [http://localhost:15672](http://localhost:15672)
- Default username: `guest`
- Default password: `guest`

### Accessing MinIO
- Console: [http://localhost:9001](http://localhost:9001)
- API: [http://localhost:9000](http://localhost:9000)
- Default Access Key: `minioadmin`
- Default Secret Key: `minioadmin`

## Persistent Data
- RabbitMQ data is stored in `~/greyparrot/docker-installations/rabbit/rabbitmq/data/`.
- MinIO stores data in a volume managed by Docker.

## Network Configuration
Both services are connected via a custom bridge network (`rabbitmq_go_net`).
