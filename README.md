# Generate J2EE project using Archtype
How to generate a Maven based J2EE project using Archtype

#Step 1
Create an archetype using the maven command in you terminal

` mvn archetype:generate -DgroupId=com.silverg4te.maven -DartifactId=samplemavenapp -Dversion=1.0-SNAPSHOT`

#Step 2
Maven will download necessary POM files and Jasr into your Local Maven Repo
```
[INFO] Scanning for projects...
[INFO] 
[INFO] ------------------< org.apache.maven:standalone-pom >-------------------
[INFO] Building Maven Stub Project (No POM) 1
[INFO] --------------------------------[ pom ]---------------------------------
[INFO] 
[INFO] >>> maven-archetype-plugin:3.1.2:generate (default-cli) > generate-sources @ standalone-pom >>>
[INFO] 
[INFO] <<< maven-archetype-plugin:3.1.2:generate (default-cli) < generate-sources @ standalone-pom <<<
[INFO] 
[INFO] 
[INFO] --- maven-archetype-plugin:3.1.2:generate (default-cli) @ standalone-pom ---
[INFO] Generating project in Interactive mode
[INFO] No archetype defined. Using maven-archetype-quickstart (org.apache.maven.archetypes:maven-archetype-quickstart:1.0)
```

#Step 3
Maven will display all the available archtype from Maven Repository.
For illustration purpose, choos the quick start archtype.
```
Choose archetype:
1: remote -> am.ik.archetype:elm-spring-boot-blank-archetype (Blank multi project for Spring Boot + Elm)
2: remote -> am.ik.archetype:graalvm-blank-archetype (Blank project for GraalVM)
3: remote -> am.ik.archetype:graalvm-springmvc-blank-archetype (Blank project for GraalVM + Spring MVC)
4: remote -> am.ik.archetype:graalvm-springwebflux-blank-archetype (Blank project for GraalVM + Spring MVC)
5: remote -> am.ik.archetype:maven-reactjs-blank-archetype (Blank Project for React.js)
6: remote -> am.ik.archetype:msgpack-rpc-jersey-blank-archetype (Blank Project for Spring Boot + Jersey)
7: remote -> am.ik.archetype:mvc-1.0-blank-archetype (MVC 1.0 Blank Project)
8: remote -> am.ik.archetype:spring-boot-blank-archetype (Blank Project for Spring Boot)
9: remote -> am.ik.archetype:spring-boot-docker-blank-archetype (Docker Blank Project for Spring Boot)
...
1667: remote -> org.apache.maven.archetypes:maven-archetype-quickstart (An archetype which contains a sample Maven project.)
...
Choose a number or apply filter (format: [groupId:]artifactId, case sensitive contains): 1667: 
```

Select `org.apache.maven.archetypes:maven-archetype-quickstart (An archetype which contains a sample Maven project.)` which in my case is number 1667

#Step 4
Next maven will ask you to choose the version of maven archetype. Select the latest version.
```
Choose org.apache.maven.archetypes:maven-archetype-quickstart version: 
1: 1.0-alpha-1
2: 1.0-alpha-2
3: 1.0-alpha-3
4: 1.0-alpha-4
5: 1.0
6: 1.1
7: 1.3
8: 1.4
Choose a number: 8: 
```

Press `enter` to select `8` or the latest version.

#Step 5
Next maven will display the given properties for confirmation. Press `enter` to select `Y`

```
[INFO] Using property: groupId = com.silverg4te.maven
[INFO] Using property: artifactId = samplemavenapp
[INFO] Using property: version = 1.0-SNAPSHOT
[INFO] Using property: package = com.silverg4te.maven
Confirm properties configuration:
groupId: com.silverg4te.maven
artifactId: samplemavenapp
version: 1.0-SNAPSHOT
package: com.silverg4te.maven
 Y: : 
```

#Step 6
Maven will create a product as given in the `DartifactId` parameter and display that the build is successful.
```
[INFO] ----------------------------------------------------------------------------
[INFO] Using following parameters for creating project from Archetype: maven-archetype-quickstart:1.4
[INFO] ----------------------------------------------------------------------------
[INFO] Parameter: groupId, Value: com.silverg4te.maven
[INFO] Parameter: artifactId, Value: samplemavenapp
[INFO] Parameter: version, Value: 1.0-SNAPSHOT
[INFO] Parameter: package, Value: com.silverg4te.maven
[INFO] Parameter: packageInPathFormat, Value: com/silverg4te/maven
[INFO] Parameter: package, Value: com.silverg4te.maven
[INFO] Parameter: groupId, Value: com.silverg4te.maven
[INFO] Parameter: artifactId, Value: samplemavenapp
[INFO] Parameter: version, Value: 1.0-SNAPSHOT
[INFO] Project created from Archetype in dir: /Users/phionic/samplemavenapp
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  01:06 min
[INFO] Finished at: 2020-08-22T00:18:44+08:00
[INFO] ------------------------------------------------------------------------
```

#Conclusion
You have successful create a J2EE project using Maven Archtype. 
