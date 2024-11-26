Sentry spring boot example with Opentelemetry

1. put DSN in application.properties file
2. run `gradle assemble` to build app
3. run app with `java -javaagent:'./sentry-opentelemetry-agent-6.34.0.jar' -jar ./build/libs/sentry-spring-opentelemetry.jar`
4. `curl localhost:8080/rolldice` to get a transaction event with OpenTelemetry spans and context
5. `curl localhost:8080/error` to get normal Sentry error event