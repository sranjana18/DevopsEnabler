FROM openjdk:11-jdk AS build

COPY HelloWorld.java .
RUN javac HelloWorld.java
EXPOSE 8082

FROM openjdk:11-jre 
COPY --from=build HelloWorld.class .
CMD java HelloWorld
