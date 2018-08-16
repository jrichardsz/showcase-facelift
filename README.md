# PrimeFaces Showcase

![PrimeFaces icon](https://www.primefaces.org/wp-content/uploads/2016/10/prime_logo_new.png)

# Getting Started

In order to use this repository for development or server builds, the following technologies are required:

- JDK 8
- Maven

# Development purposes

- Download Eclipse IDE
- Check if maven is configured in eclipse
- Add JDK 8 in **Installed JREs** option (eclipse)
- Clone this repository: https://github.com/primefaces/showcase-facelift.git
- Set **community-stable** profile as default in pom.xml
- Import it on eclipse as maven project
- Perform a maven update in eclipse project
- Add tomcat 9 in **server** section in eclipse.
- Execute this **mvn** command to prepare css resources : `mvn sass:scss-lint`
- Right click on eclipse project and select **Run as >> Run on server** 
- Open browser at http://localhost:8080/showcase/

# Build purposes (for testing or production environments)

## Prebuilt war

Deployable version of **PrimeFaces Showcase** war file can be downloaded manually or build it from sources.

For a full list of the available downloads, please visit the [download page](http://www.primefaces.org/downloads). Scroll down to showcase for war file link.

## Build from sources

```
git clone https://github.com/primefaces/showcase-facelift.git
cd showcase
mvn clean                  -- clean temp files from target folder
mvn sass:scss-lint         -- compile css resources (for development purposes)
mvn package                -- create war file (under target directory)
```

# Run from local sources

```
mvn jetty:run
```

Home page is: [http://localhost:8080/showcase/](http://localhost:8080/showcase)

# Run on remote servers like tomcat 9

- After mvn commands, an artifact called **showcase-6.3.0-SNAPSHOT.war** is generated. To make life easier, rename to **showcase.war**
- If you has downloaded the **prebuilt war**, check its name.
- Copy this file to /webapps folder in tomcat.
- Start tomcat server

If your server has a public ip : 10.10.10.20 and public port like : 8080 (for instance)

Home page will be: [http://10.10.10.20:8080/showcase/](http://localhost:8080/showcase)

# Documentation

User Guide is available at [documentation](http://www.primefaces.org/documentation) page along with other additional resoures.

### Contribution

Visit [Contribution Wiki](https://github.com/primefaces/primefaces/wiki/Contributing-to-Primefaces) page for the detailed information.

### License

Licensed under the Apache License, Version 2.0 (the "License") [http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)
