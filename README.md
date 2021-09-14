# [Book My Doctor - A Clinic Appointment Management System]
[![CodeQL](https://github.com/meet63380/BookMyDoctor/actions/workflows/codeql-analysis.yml/badge.svg)](https://github.com/meet63380/BookMyDoctor/actions/workflows/codeql-analysis.yml)
[![Git Inspector](https://github.com/meet63380/BookMyDoctor/actions/workflows/gitinspector.yml/badge.svg)](https://github.com/meet63380/BookMyDoctor/actions/workflows/gitinspector.yml)
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/50d6890e21f743e2b4736ea36e102310)](https://www.codacy.com/gh/meet63380/BookMyDoctor/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=meet63380/BookMyDoctor&amp;utm_campaign=Badge_Grade)
[![Maven Publish](https://github.com/meet63380/BookMyDoctor/actions/workflows/maven-publish.yml/badge.svg)](https://github.com/meet63380/BookMyDoctor/actions/workflows/maven-publish.yml)

## Getting started
### Prerequisites:
- Java 16
- Maven
- MySQL
- Your preferred IDE (Eclipse/ Spring Tool Suite/ IntelliJ)
## Understanding BookMyDoctor with a few diagrams
### class diagram
<img width=1042 src="https://github.com/meet63380/BookMyDoctor/tree/master/src/main/docs/class_diagram.png">

## Some Screenshots
### Login Screen
![login-screen](https://github.com/meet63380/BookMyDoctor/tree/master/src/main/docs/login.png)

### Doctors
![doctors](https://github.com/meet63380/BookMyDoctor/tree/master/src/main/docs/doctors.png)


### Doctor's schedule
![doctor's schedule](https://github.com/meet63380/BookMyDoctor/tree/master/src/main/docs/doctor_schedule.png)


### Appointments
![appointments](https://github.com/meet63380/BookMyDoctor/tree/master/src/main/docs/my_appointments.png)


### Edit profile
![edit-profile](https://github.com/meet63380/BookMyDoctor/tree/master/src/main/docs/edit_profile.png)

## Running BookMyDoctor locally
BookMyDoctor is a [Spring Boot](https://spring.io/guides/gs/spring-boot) application built using [Maven](https://spring.io/guides/gs/maven/). You can build a jar file and run it from the command line:


```
git clone https://github.com/meet63380/BookMyDoctor.git
cd BookMyDoctor
./mvnw package
java -jar target/*.jar
```

You can then access BookMyDoctor here: http://localhost:8081/

Or you can run it from Maven directly using the Spring Boot Maven plugin. If you do this it will pick up changes that you make in the project immediately (changes to Java source files require a compile as well - most people use an IDE for this):

```
./mvnw spring-boot:run
```

> NOTE: Windows users should set `git config core.autocrlf true` to avoid format assertions failing the build (use `--global` to set that flag globally).



## Database configuration

In its default configuration, BookMyDoctor uses a MySQL database which doesn't get populated automatically with data.
To populte the database, import data from BookMyDoctordump folder

You could start MySql locally with whatever installer works for your OS, or with docker:

### Steps:

1) On the command line
    ```
    git clone https://github.com/meet63380/BookMyDoctor.git
    ```
2) Inside Eclipse or STS
    ```
    File -> Import -> Maven -> Existing Maven project
    ```

    Then either build on the command line `./mvnw generate-resources` or using the Eclipse launcher (right click on project and `Run As -> Maven install`) to generate the css. Run the application main method by right clicking on it and choosing `Run As -> Java Application`.

3) Inside IntelliJ IDEA
    In the main menu, choose `File -> Open` and select the BookMyDoctor [pom.xml](pom.xml). Click on the `Open` button.

    CSS files are generated from the Maven build. You can either build them on the command line `./mvnw generate-resources` or right click on the `BookMyDoctor` project then `Maven -> Generates sources and Update Folders`.

    A run configuration named `BookMyDoctorApplication` should have been created for you if you're using a recent Ultimate version. Otherwise, run the application by right clicking on the `BookMyDoctorApplication` main class and choosing `Run 'BookMyDoctorApplication'`.

4) Navigate to BookMyDoctor

    Visit [http://localhost:8081](http://localhost:8081) in your browser.

