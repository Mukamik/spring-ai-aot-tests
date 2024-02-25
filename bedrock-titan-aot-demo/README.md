# Spring AI OpenAI AOT Demo Application

```
export JAVA_HOME=/Library/Java/JavaVirtualMachines/graalvm-jdk-21.0.2+13.1/Contents/Home
```

```
./mvnw clean install -DskipTests -Pnative native:compile
```

```
./target/bedrock-titan-aot-demo
```

## Generate GraalVM configs

```
java -Dspring.aot.enabled=true \
    -agentlib:native-image-agent=config-output-dir=target/config-dir/ \
    -jar target/bedrock-titan-aot-demo-0.0.1-SNAPSHOT.jar
```