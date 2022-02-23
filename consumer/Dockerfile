FROM openjdk:8-jre-slim

WORKDIR /kafka-server

COPY kafka/ /kafka-server/


ENTRYPOINT [ "./bin/kafka-console-consumer.sh","--bootstrap-server","kafka:9092","--from-beginning","--topic" ]

CMD [ "test" ]
