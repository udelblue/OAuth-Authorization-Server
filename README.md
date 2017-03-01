# OAuth Server


### Installation

Application requires ms sql server driver to run.

Open command line in project directory and navigate to 'MavenScripts.bat'. Execute .bat to install sqljdbc jar in maven repository. 

```sh
cd src
cd main
cd resources
MavenScripts.bat
```

Configure connection string. Open 'application.yml' to configure. Currently pointed to localhost

```sh
spring:
  datasource:
    url: jdbc:sqlserver://localhost:1433;databaseName=OAuth
    username: oauth
    password: oauth#1234
    driver-class-name: com.microsoft.sqlserver.jdbc.SQLServerDriver
    initialize: true
```

### Build
Open command line in project directory. Run 'mvn clean package' to clean and build project. 

```sh
mvn clean package
```

### Run

Open command line in project directory. Run jar 

```sh
cd target
java -jar oauth_sql_server-1.3.5.RELEASE.jar
```


Verify the deployment by navigating to your server address in your preferred browser.

```sh
127.0.0.1:8080
```




