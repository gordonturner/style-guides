Project Naming Conventions
==========================

There are only two hard things in Computer Science: cache invalidation and naming things.

-- Phil Karlton

https://martinfowler.com/bliki/TwoHardThings.html


- Reference:

https://www.slideshare.net/pirhilton/how-to-name-things-the-hardest-problem-in-programming


Commentary
----------

There is no right or wrong answers.

However, there should be structure and consistency to the naming.  

The test is someone with no knowledge of the project should be able to navigate the project names and understand the convention.

It can be a challenge to name without direction for how many other projects there will be or of what type.

Expect to get it wrong and have to rename them, there should be no ego attached to names. 


Consideration 1
---------------

In general the names should be:

- All lower case
- Hyphens between words  


Consideration 2
---------------

General hierarchy should start with a general identifier and get more specific.

Example, same client and project with different functions:

```
client-project-web
client-project-web-api
client-project-reporting
client-project-job
client-project-iOS-app
client-project-Android-app
```

Example, same client and project with multiple independent websites or campaign micro sites:

```
client-project-web
client-project-web-campaign-2017-winter
client-project-web-campaign-2017-spring
client-project-web-campaign-2017-fall
```

Example, same client, different projects:

```
client-project1-web
client-project2-web
client-project3-web
client-project4-web
```


Consideration 3
---------------

Should the reference projects be named and organized by what they do versus how / with what language they do it?

Is it a series of reference projects contrasting approaches how / with what language?  

Then name them with the same 'root' and suffix with a name identifying the how / with what language.

Example:

```
reference-cli-ssh-tunnel-bash
reference-cli-ssh-tunnel-java
reference-cli-ssh-tunnel-python
```

Example:

```
reference-cli-java-ssh-tunnel-tomcat
reference-cli-java-ssh-tunnel-AEM
reference-cli-java-ssh-tunnel-MySQL
reference-cli-java-nexus-2
reference-cli-java-nexus-3
```

Example:

```
reference-spring-xml-config
reference-spring-java-config
reference-spring-boot-config
```

Example:

```
reference-maven-release-test
reference-maven-release-jgitflow-test
reference-maven-release-jgitflow-test-aem 
```
