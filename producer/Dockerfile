# syntax=docker/dockerfile:1.2

FROM openjdk:8-jre-slim

WORKDIR /mykafka

COPY kafka/ /mykafka

ENTRYPOINT ["./bin/kafka-console-producer.sh","--bootstrap-server","kafka:9092","--topic"]

CMD [ "test" ]
