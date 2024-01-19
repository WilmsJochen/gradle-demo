# Gradle demo
In this repo we setup a java springboot project with a build tool called gradle.

## Download the gradle binary.
Install the gradle binary following this guide. https://docs.gradle.org/current/userguide/installation.html

## Init project
Init the java project following this guide, https://docs.gradle.org/current/userguide/partr1_gradle_init.html.
`gradle init`

## Implement dependencies
The `build.gradle` file contains a list of dependencies required to build the application. You can add following basic spring-boot dependencies in this list and build the project again.
```
    implementation("org.springframework.boot:spring-boot-starter-web")
    implementation("org.springframework.boot:spring-boot-starter-jdbc")
    implementation("org.springframework.boot:spring-boot-starter-actuator")
    implementation("org.springframework.boot:spring-boot-starter-security")
    implementation("org.springframework.boot:spring-boot-starter-data-jpa")
    implementation("org.springframework.boot:spring-boot-starter-logging")
    implementation("org.springframework.boot:spring-boot-starter-websocket")
    implementation("org.springframework.boot:spring-boot-starter-quartz")
```


## Create a groovy task
Add in the gradle.build file following task
```
tasks.register('hello') {
    group = "Custom"
    description = "A lovely greeting task."
    doLast {
        println("Hello world!")
    }
}
```

List your gradle tasks `./gradlew tasks` and execute the task `./gradlew hello`


