## Distributed Redis Implementation with Go, HAProxy and Docker

This project is a simple implementation of a distributed Redis system using Go, HAProxy and Docker. The project is divided into three main parts:

1. **Redis Cluster**: A Redis cluster with 3 master nodes
2. **Go Client**: A Go client that connects to the Redis cluster and performs some operations
3. **HAProxy Load Balancer**: A HAProxy load balancer that distributes the requests to the Redis cluster

## Running the project

To run the project, you need to have Docker installed on your machine. Then, you can run the following commands:

1. **Build the Docker images**:

```bash
docker-compose build
```

2. **Run the Docker containers**:

```bash
docker-compose up -d
```

3. **Check the logs**:

```bash
docker-compose logs haproxy
```

## Testing the project

To test the project, you can run the following command:

```bash
curl --location 'localhost:8081/key' --head
er 'Content-Type: application/json' --data '{"key": "hello", "value": "world"}'
```

## Endpoints

The project has the following endpoints:

1. **GET /key**: Get the value of a key
2. **POST /key**: Set the value of a key
3. **DELETE /key**: Delete a key
4. **GET /health**: Check the health of the Redis cluster
