### REDIS STREAM

#### Description

This project is a basic example of a publisher and consumers of a redis stream

Start a local redis with :
```bash
docker-compose up -d
```

#### Setup

```bash
go install -v ./...
```

#### Publisher

The publisher sends 3000 messages to the redis stream
```bash
cd publisher
go run main.go
```

#### Consumer

The consumer reads all the pending messages in the stream then aknowledges them

```bash
cd consumer
go run main.go
```
