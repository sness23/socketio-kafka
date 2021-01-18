# socketio-kafka
Uses Socket.io to push Kafka messages to clients. Based on the [socket.io chat demo](http://socket.io/get-started/chat/).

## Requirements
- Kafka. The [Apache Kafka Quick Start](https://kafka.apache.org/quickstart) provides instructions on setting up a simple ZooKeeper server and Kafka broker.
- Socket.io. The [Socket.io Get Started Chat App](http://socket.io/get-started/chat/) describes a simple chat app demo using socket.io.
- [Node](http://nodejs.org) and npm

## Running
Start Kafka, e.g. open two shells and start zookeeper, then kafka:
```
kafka_2.10-0.8.2.0$ bin/zookeeper-server-start.sh config/zookeeper.properties
```

```
kafka_2.10-0.8.2.0$ bin/kafka-server-start.sh config/server.properties
```

Within this project's directory, install the Node dependencies and run the app:
```
npm install
node index.js
```
Discover your fortune at `localhost:3000`.

## Running in Docker
```
docker build -t socketio-kafka .
docker run -p 3000:3000 -d socketio-kafka
```
The app should now be running on localhost:3000, or if you are using boot2docker on port 3000 of your boot2docker IP address (run boot2docker ip to find it).
