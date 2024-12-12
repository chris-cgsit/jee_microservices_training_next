# Workshop : JEE Microservice Development with Quarkus
## jee_microservice_restapi

This project includes:

- examples for quarkus and jaxrs rest api development
- rest api parameter handling
  - rest api Query parameter handling
  - rest api Path parameter handling
  - DTO transport objects
  - JsonProperty and JsonbProperty usage for jackson annotations
  - JsonbDateFormat usage for jackson annotations
- Quarkus 
  - Usage of configuration properties from quarkus
  - Quarkus Console
- JaxRS Security
  - quarkus-security-jpa usage
- exception handling in rest api jaxrs with JsonExceptoionMapper
- Microprofile OpenAPI and Swagger UI
- OpenAPI generate code from OpenAPI specification
- Postman Rest API Tests
- Quarkus Rest Assured Tests for Rest APIs
- JaxRs Application and Resource Configuration
- Bean Validation
  - Bean Validation with JaxRs
  - Bean Validation with Quarkus 
  - Bean Validation DTO Annotations
  - Bean Validation Custom Validator
  - AssertTrue and AssertFalse Methods for Bean Validation
- JaxRs REst Client usage to call other Rest Services with
  - RegisterRestClient
  - fallback methods for rest client
  - Microprofile health check and Metrics 
  - Builder Client manually

This project is used as an example project for jee microservice development with quarkus 
and is part of the course material for the course "Microservice Development with Quarkus" 
see ./license.txt for license information.

This project uses Quarkus, the Supersonic Subatomic Java Framework.
If you want to learn more about Quarkus, please visit its website: https://quarkus.io/ .

This work © 2023 by CGS-IT Solutions GmbH is licensed under Attribution-NonCommercial 4.0 International

## Running the application in dev mode

You can run your application in dev mode that enables live coding using:

```shell script
./mvnw compile quarkus:dev
```

> **_NOTE:_**  Quarkus now ships with a Dev UI, which is available in dev mode only at http://localhost:8080/q/dev/.

## Packaging and running the application

The application can be packaged using:

```shell script
./mvnw package
```

It produces the `quarkus-run.jar` file in the `target/quarkus-app/` directory.
Be aware that it’s not an _über-jar_ as the dependencies are copied into the `target/quarkus-app/lib/` directory.

The application is now runnable using `java -jar target/quarkus-app/quarkus-run.jar`.

If you want to build an _über-jar_, execute the following command:

```shell script
./mvnw package -Dquarkus.package.type=uber-jar
```

The application, packaged as an _über-jar_, is now runnable using `java -jar target/*-runner.jar`.

## Creating a native executable

You can create a native executable using:

```shell script
./mvnw package -Pnative
```

Or, if you don't have GraalVM installed, you can run the native executable build in a container using:

```shell script
./mvnw package -Pnative -Dquarkus.native.container-build=true
```

You can then execute your native executable with: `./target/kurs_jeemicro-1.0-SNAPSHOT-runner`

If you want to learn more about building native executables, please consult https://quarkus.io/guides/maven-tooling.

## Related Guides

- RESTEasy Classic ([guide](https://quarkus.io/guides/resteasy)): REST endpoint framework implementing Jakarta REST and
  more

## Provided Code

### RESTEasy JAX-RS

Easily start your RESTful Web Services

[Related guide section...](https://quarkus.io/guides/getting-started#the-jax-rs-resources)