[![Build Status](https://datamountaineer.ci.landoop.com/buildStatus/icon?job=stream-reactor&style=flat&.png)](https://datamountaineer.ci.landoop.com/job/stream-reactor/)
[![Documentation Status](https://readthedocs.org/projects/streamreactor/badge/?version=latest)](http://docs.datamountaineer.com/en/latest/?badge=latest)
[![Alt text](images/slack.jpeg)](http://datamountaineer.com/contact/)

# Stream Reactor
Streaming reference architecture built around Kafka. 

![Alt text](https://datamountaineer.files.wordpress.com/2016/01/stream-reactor-1.jpg?w=1320)

A collection of components to build a real time ingestion pipeline.

### Connectors


|Connector       | Type   | Description                                                                                 | Docs |
|----------------|--------|---------------------------------------------------------------------------------------------|------|
| BlockChain     | Source | Kafka connect Blockchain source to subscribe to Blockchain streams and write to Kafka.      | [Docs](http://docs.datamountaineer.com/en/latest/blockchain.html)        |
| Bloomberg      | Source | Kafka connect Blockchain source to subscribe to Blockchain streams and write to Kafka.      | [Docs](http://docs.datamountaineer.com/en/latest/bloomberg.html)         |
| Cassandra      | Source | Kafka connect Cassandra source to read Cassandra and write to Kafka.                        | [Docs](http://docs.datamountaineer.com/en/latest/cassandra-source.html)  |
| *DSE Cassandra | Sink   | Certified DSE Kafka connect Cassandra sink task to write Kafka topic payloads to Cassandra. | [Docs](http://docs.datamountaineer.com/en/latest/cassandra-sink.html)    |
| Druid          | Sink   | Kafka connect Druid sink to write Kafka topic payloads to Druid.                            | [Docs](http://docs.datamountaineer.com/en/latest/druid.html)             |
| Elastic        | Sink   | Kafka connect Elastic Search sink to write Kafka topic payloads to Elastic Search.          | [Docs](http://docs.datamountaineer.com/en/latest/elastic.html)           |
| HBase          | Sink   | Kafka connect HBase sink to write Kafka topic payloads to HBase.                            | [Docs](http://docs.datamountaineer.com/en/latest/hbase.html)             |
| Hazelcast      | Sink   | Kafka connect Hazelcast sink to write Kafka topic payloads to Hazelcast.                    | [Docs](http://docs.datamountaineer.com/en/latest/hazelcast.html)         |
| Kudu           | Sink   | Kafka connect Kudu sink to write Kafka topic payloads to Kudu.                              | [Docs](http://docs.datamountaineer.com/en/latest/kudu.html)              |
| MongoDB        | Sink   | Kafka connect Kudu sink to write Kafka topic payloads to MongoDB.                           | [Docs](http://docs.datamountaineer.com/en/latest/mongo.html)             |
| InfluxDb       | Sink   | Kafka connect InfluxDb sink to write Kafka topic payloads to InfluxDb.                      | [Docs](http://docs.datamountaineer.com/en/latest/influx.html)            |
| JMS            | Sink   | Kafka connect JMS sink to write Kafka topic payloads to JMS.                                | [Docs](http://docs.datamountaineer.com/en/latest/jms.html)               |
| Redis          | Sink   | Kafka connect Redis sink to write Kafka topic payloads to Redis.                            | [Docs](tree/feature/improve-redis-integration/kafka-connect-redis)       |
| ReThinkDB      | Source | Kafka connect RethinkDb source subscribe to ReThinkDB changefeeds and write to Kafka.       | [Docs](http://docs.datamountaineer.com/en/latest/rethink_source.html)    |
| ReThinkDB      | Sink   | Kafka connect RethinkDb sink to write Kafka topic payloads to RethinkDb.                    | [Docs](http://docs.datamountaineer.com/en/latest/rethink.html)           |
| Yahoo Finance  | Source | Kafka connect Yahoo Finance source to write to Kafka.                                       | [Docs](http://docs.datamountaineer.com/en/latest/yahoo.html)             |
| VoltDB         | Sink   | Kafka connect Voltdb sink to write Kafka topic payloads to Voltdb.                          | [Docs](http://docs.datamountaineer.com/en/latest/voltdb.html)            |


### [Kafka-Socket-Streamer](kafka-socket-streamer/README.md)

Akka Http and Reactive Kafka with Websocket and Server Send Event support.
Supports limited SQL statements to stream and select from Kafka topics in real time.


### Building

***Requires gradle 3.0 to build.***

To build

```bash
gradle compile
```

To test

```bash
gradle test
```

To create a fat jar

```bash
gradle shadowJar
```

You can also use the gradle wrapper

```
./gradlew shadowJar
```
