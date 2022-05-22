# Read Me First
The following was discovered as part of building this project:

* The following dependencies are not known to work with Spring Native: 'MS SQL Server Driver, Spring Web Services, Spring Boot DevTools, Spring Configuration Processor'. As a result, your application may not work as expected.

# Getting Started

### Reference Documentation
For further reference, please consider the following sections:

* [Official Apache Maven documentation](https://maven.apache.org/guides/index.html)
* [Spring Boot Maven Plugin Reference Guide](https://docs.spring.io/spring-boot/docs/2.7.0/maven-plugin/reference/html/)
* [Create an OCI image](https://docs.spring.io/spring-boot/docs/2.7.0/maven-plugin/reference/html/#build-image)
* [Spring Web Services](https://docs.spring.io/spring-boot/docs/2.7.0/reference/htmlsingle/#boot-features-webservices)
* [Spring Native Reference Guide](https://docs.spring.io/spring-native/docs/current/reference/htmlsingle/)
* [Spring Boot DevTools](https://docs.spring.io/spring-boot/docs/2.7.0/reference/htmlsingle/#using-boot-devtools)
* [Spring Configuration Processor](https://docs.spring.io/spring-boot/docs/2.7.0/reference/htmlsingle/#configuration-metadata-annotation-processor)

### Guides
The following guides illustrate how to use some features concretely:

* [Producing a SOAP web service](https://spring.io/guides/gs/producing-web-service/)

### Additional Links
These additional references should also help you:

* [Configure the Spring AOT Plugin](https://docs.spring.io/spring-native/docs/0.12.0-SNAPSHOT/reference/htmlsingle/#spring-aot-maven)

## Spring Native

This project has been configured to let you generate either a lightweight container or a native executable.

### Lightweight Container with Cloud Native Buildpacks
If you're already familiar with Spring Boot container images support, this is the easiest way to get started with Spring Native.
Docker should be installed and configured on your machine prior to creating the image, see [the Getting Started section of the reference guide](https://docs.spring.io/spring-native/docs/0.12.0-SNAPSHOT/reference/htmlsingle/#getting-started-buildpacks).

To create the image, run the following goal:

```
$ ./mvnw spring-boot:build-image
```

Then, you can run the app like any other container:

```
$ docker run --rm demo:0.0.1-SNAPSHOT
```

### Executable with Native Build Tools
Use this option if you want to explore more options such as running your tests in a native image.
The GraalVM native-image compiler should be installed and configured on your machine, see [the Getting Started section of the reference guide](https://docs.spring.io/spring-native/docs/0.12.0-SNAPSHOT/reference/htmlsingle/#getting-started-native-build-tools).

To create the executable, run the following goal:

```
$ ./mvnw package -Pnative
```

Then, you can run the app as follows:
```
$ target/demo
```
