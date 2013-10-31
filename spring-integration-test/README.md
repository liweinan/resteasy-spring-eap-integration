# spring-integration-test #

This is a project demonstrates how to deploy a project into JBoss AS7. First is to package it with Maven command:

	mvn package

Then deploy it into AS7. After the WAR deployed, run the test from project directory:

	mvn integration-test

