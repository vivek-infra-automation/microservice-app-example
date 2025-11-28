FROM eclipse-temurin:8-jdk
WORKDIR /usr/src/app

RUN apt-get update && apt-get install -y maven && rm -rf /var/lib/apt/lists/*

COPY pom.xml ./
COPY . .

RUN mvn install -DskipTests

EXPOSE 8083

CMD ["java", "-jar", "./target/users-api-0.0.1-SNAPSHOT.jar"]
