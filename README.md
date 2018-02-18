## Extremely simple maven project that is deployed onto a locally running instance of tomcat.

Remember to:
- add `manager-script` role to `tomcat-users.xml`.
- `<plugin>
	<groupId>org.apache.tomcat.maven</groupId>
	<artifactId>tomcat7-maven-plugin</artifactId>
	<version>2.2</version>
	<configuration>
	<url>http://localhost:8080/manager/text</url>
	<server>TomcatServer</server>
	<path>/mkyongWebApp</path>
	</configuration>
  </plugin>` into `pom.xml`
- `<server>
	<id>TomcatServer</id>
	<username>TOMCATUSRNM</username>
	<password>TOMCATPSSWD</password>
   </server>` into maven conf `settings.xml`
