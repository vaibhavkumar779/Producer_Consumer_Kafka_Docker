# ASSIGNMENT
 Dockerize and demonstrate how to solve producer/consumer problem via Kafka. 

# PreRequisites:

* docker installed on system ( Installation Steps: https://docs.docker.com/engine/install/ )
* docker-compose installed as well ( Installation Steps: https://docs.docker.com/compose/install/ )

Note: please go through post install steps as well in both steps for root privileges

**1. To run kafka use command:**

```bash
docker-compose up --build
```

Now kafka & consumer is running in this terminal.

**2. Run producer in other terminal to enter message.**

**Option1:**

```bash
cd Producer_Consumer_Kafka_Docker
docker-compose run producer
```

**Option2:**

```bash
cd Producer_Consumer_Kafka_Docker
docker exec -it kafka_server /bin/sh

# this brings the shell for interacting server

cd opt/kafka/bin
kafka-console-producer.sh --broker-list kafka:9092 --topic test

```


**3. In producer terminal type messages**

```text
> Welcome!
> Your Procucer executions
> Shown at Consumer side
>
```

**4. Run consumer in other terminal to enter message.**

**Option1:**

```bash
cd Producer_Consumer_Kafka_Docker
docker-compose run consumer
```

**Option2:**

```bash
cd Producer_Consumer_Kafka_Docker
docker exec -it kafka_server /bin/sh

# this brings the shell for interacting server

cd opt/kafka/bin
kafka-console-consumer.sh --bootstrap-server kafka:9092 --topic test --from-beginning

```

**5. In consumer terminal you will see messages.**

```text
Welcome
Your Producer executions
Shown at Consumer side
```