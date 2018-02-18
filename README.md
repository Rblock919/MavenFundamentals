## Extremely simple maven project that is deployed onto a locally running instance of tomcat.

Remember to:
- add `manager-script` role to `tomcat-users.xml`.
- `<plugin> `<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<groupId>org.apache.tomcat.maven</groupId> `<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<artifactId>tomcat7-maven-plugin</artifactId> `<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<version>2.2</version> `<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<configuration> `<br /> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<url>http://localhost:8080/manager/text</url> `<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<server>TomcatServer</server> `<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<path>/mkyongWebApp</path> `<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`</configuration> `<br />
  `</plugin>` into `pom.xml`
- `<server> `<br />
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<id>TomcatServer</id> `<br />
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<username>TOMCATUSRNM</username> `<br />
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`<password>TOMCATPSSWD</password> `<br />
   `</server>` into maven conf `settings.xml`
