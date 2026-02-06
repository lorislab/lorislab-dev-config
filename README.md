# Lorislab development configuration

Centralized development configuration and code quality rules for lorislab projects. This repository provides shared resources for Maven plugins to ensure consistent code style and quality across multiple libraries and applications.

## Purpose
Maintaining a consistent code style across various repositories is difficult. This project packages configuration files (Formater, ImportSort, etc.) into a single artifact that can be included as a dependency in the  quality tools.

## What's Included?

- Formatter

## Usage in Maven

To use these configurations in your project, add this repository as a dependency within your plugin configurations in the `pom.xml`.

```xml
<plugin>
    <groupId>net.revelc.code.formatter</groupId>
    <artifactId>formatter-maven-plugin</artifactId>
    <dependencies>
        <dependency>
            <groupId>org.lorislab.dev</groupId>
            <artifactId>lorislab-dev-config</artifactId>
            <version>${lorislab-dev-config.version}</version>
        </dependency>
    </dependencies>
    <configuration>
        <configFile>eclipse-format.xml</configFile>
        <lineEnding>LF</lineEnding>
        <skip>${format.skip}</skip>
    </configuration>
</plugin>
```

## Build

To build the project locally and verify the configurations:

```shell
mvn clean install
```

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.