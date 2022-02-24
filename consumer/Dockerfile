FROM openjdk:8-jre-slim

WORKDIR /mykafka

COPY kafka/ /mykafka/

ENTRYPOINT [ "./bin/kafka-console-consumer.sh","--bootstrap-server","kafka:9092","--from-beginning","--topic" ]

CMD [ "test" ]
