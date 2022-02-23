FROM openjdk:8-jre-slim

WORKDIR /kafka-server

COPY kafka/ /kafka-server/

ENTRYPOINT ["./bin/kafka-console-producer.sh","--bootstrap-server","kafka:9092","--topic"]

CMD [ "test" ]
