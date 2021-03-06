ps-guitar-rest
============

A Basic Spring Data JPA app with an H2 DB running on Spring Boot

Prerequisites
-------------
You will need to following tools in order to work with this project and code

* git (http://git-scm.com/)
* JDK 1.8+ (http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
* Maven 3.x+ (http://maven.apache.org/)
* An IDE of your choice.  (Eclipse, IntelliJ, Spring STS, Netbeans, etc.)

Getting Started
---------------
To run this project locally, perform the following steps.

* Clone project to your machine using git - "git clone https://github.com/dlbunker/ps-guitar-rest.git"
* Import the project into your IDE using the maven pom.xml.  In spring STS suite this is done by importing an existing maven project
* Run the JUnit tests in the src/test/java folder.  If all the tests pass, pat yourself on the back.
* Next try running the app as a Spring Boot app.  You can do this by running the Main.java file in this project as a standard java project or you can run spring boot at your project's root with Maven using the following command.  'mvn spring-boot:run'


# Integrating Spring Data Rest
```
<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-data-rest</artifactId>
</dependency>

Second way is to supply the spring-data-rest-webmvc dependency

<dependency>
	<groupId>org.springframework.data</groupId>
	<artifactId>spring-data-rest-webmvc</artifactId>
	<version>2.3.0.RELEASE</version>
</dependency>


@Configuration
public class CustomizedRestMvcConfiguration extends RepositoryRestMvcConfiguration {
	@Override
	public RepositoryRestConfiguration config() {
		RepositoryRestConfiguration config = super.config();
		config.setBasePath("/api");
		return config;
	}
}
```

**Supported Technologies**
- Spring Data Commons
	- Spring Data JPA
	- Spring Data MongoDB
	- Spring Data Neo4j
	- Spring Data Gemfire
	- Spring Data Cassandra