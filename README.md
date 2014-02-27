# Weblogic SoapUI Mock EAR Module

Wraps the WAR file from a SoapUI mock into an EAR module. Also fixes classloader issues using `weblogic-application.xml`.

## Create WAR file

* Open the SoapUI project in SoapUI.
* Right click the project.
* Select 'Deploy as War'.
* Enter the MockService Endpoint. Make sure it matches the actual URL used for the service (e.g. `http://wlsserver.com/mockService`).
* Enter the location for the WAR File and the War Directory.

## Configuration

* Copy `gradle.properties.example` to `gradle.properties`.
* Change the properties in the file to the appropriate values.

## Build EAR file

* Run `./gradlew build`.
* The EAR will be built in to `build/libs/`.

## Deploy to Weblogic server

* Run `./gradlew deploy`.

## Undeploy from Weblogic server

* Run `./gradlew undeploy`.
