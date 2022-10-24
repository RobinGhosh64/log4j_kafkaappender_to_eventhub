# Sending Application Logs to Azure Event Hub

Azure Event Hub is Microsoft's own Kafka product


There are two ways you can send application logs to Azure Event Hub.
1) If your applications are already running on Azure App Service, you can go to the Monitoring section
   of your App instance, go to --Daignostics Settings-- then add a new destination pointing straight to Event Hub
   (This requires no code changes)
<br>
OR

2) Send to Azure Event Hub directly from your application code using standard Log4J appenders. 
   If you are already sending logs to Kafka servers using Log4J appender, replace the connection string parameters in your configuration to point to our Event Hub
   If you have not using log4j appenders and using standard Spring logging only, please update your pom.xml based on this project and add Kafka appender in your log4j settings
   



## Requirements

1. Java - 1.8.x

2. Maven - 3.x.x

## Steps to setup

**1. Clone the application**

```bash
git clone https://github.com/RobinGhosh64/log4j_kafkaappender_to_eventhub.git
```

**2. Build and run the app using maven**

```bash
cd log4j_kafkaappender_to_eventhub
mvn package
java -jar target/log4j2-demo-0.0.1-SNAPSHOT.jar
```

You can also run the app without packaging it using -

```bash
mvn spring-boot:run
```

You should see the following output as shown in the image folders attached. Please verify
