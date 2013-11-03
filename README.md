# spring-integration-test #

This is a project demonstrates how to deploy a project into JBoss EAP 6.2.0.Final. First is to package it with Maven command:

	mvn package

Then deploy it into EAP. After the WAR deployed, run the test from project directory:

	mvn integration-test

# spring-integration-test-nodep #

This project demonstrates how to use EAP modules to enable spring support. To make this project run properly, please follow these instructions:

- Download JBoss Snowdrop 3.0.1.Final from http://www.jboss.org/snowdrop/downloads
- Extract it and put the modules from 'module-spring-3.2' into the 'modules' directory of EAP.
- Copy the resteasy-spring module from "eap-module-def" into the 'modules' directory of EAP.
- Deploy 'spring-integration-test-nodep' into EAP, and the project should be deployed.

The dependency of resteasy-spring module is defined in 'MANIFEST.MF' of 'spring-integration-test-nodep':

https://github.com/liweinan/resteasy-spring-eap-integration/blob/master/spring-integration-test-nodep/META-INF/MANIFEST.MF

It's defined by 'Dependencies':

	Manifest-Version: 1.0
	Dependencies: org.jboss.resteasy.resteasy-spring

You can take Snowdrop and self-defined 'resteasy-spring' approach in WildFly too, but please remember to upgrade the 'resteasy-spring' to 3.x.