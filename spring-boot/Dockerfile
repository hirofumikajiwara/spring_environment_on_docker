FROM openjdk:17-jdk-alpine
VOLUME /tmp
RUN mkdir /project
WORKDIR /project
RUN apk add bash procps curl maven gradle
CMD sh -c "(while :; do date; sleep 10; done) >&2"