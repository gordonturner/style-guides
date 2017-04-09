Java Style Guide
================

- Google Javascript Style Guide
http://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml


General
-------
- The Allman Style, putting the brace associated with a control statement on the next line, indented to the same level 
  as the control statement. 
- Statements within the braces are indented to the next level.

- If blocks must be used with opening and closing brackets.
- Inline if statements are discouraged.
- The intent is to emphasize readability and safety of opening an closing blocks.
  
- Reference:
http://en.wikipedia.org/wiki/Indent_style#Allman_style

- When using if statements, always use the form that use brackets.

- JPL coding standard:
http://lars-lab.jpl.nasa.gov/JPL_Coding_Standard_Java.pdf

- Documentation style:
http://learn.jquery.com/style-guide/


Comments
--------
- Comments should be properly capitalized and punctuated full sentences.
- If the comment is important, consider logging instead.

- If there is a long block, consider marking the closing bracket with a comment.
```
// Start of long block
if( flag )
{
...
} // END flag 
```


Logging
-------
- Logging statements should be properly capitalized and punctuated full sentences.
- Logging variable should be called 'logger' and should be initialized with the class name.
```
private static final Logger logger = Logger.getLogger( FooServlet.class );
```

- Logging statements at start of method and at end should be of the form:
```
logger.debug("Called");
...
logger.debug("Ended");
```

- The log4j ConversionPattern should include the package and method:
```
x.ConversionPattern=%d{yyyy-MM-dd HH:mm:ss,SSS} %-5p %c %x - %m%n
```

- NOTE: The logger reference is not a constant, but a final reference, and should NOT be in uppercase. A constant 
        VALUE should be in uppercase.
```
private static final Logger logger = Logger.getLogger(MyClass.class);
private static final double MY_CONSTANT = 0.0;
```
- Reference:
http://stackoverflow.com/questions/1417190/should-a-static-final-logger-be-declared-in-upper-case


Package naming
--------------
- Package names should be singular
  - Example service not services


Class Naming
------------
- Always use camel case
- Do not use all caps for acronyms or initialisms.
  - Example HTTP HttpInterceptor, DAO, UserDao

- XxxDao (Data Access Object)
  - Responsible for interacting directly with the EntityManager , JDBC DataSource , file system, etc. 
  - Should contain only persistence logic, such as SQL or JPA-QL, but not (or as little as possible) business logic. 
  - Should be accessed only from Managers.

- XxxManager
  - Manages entites at the business level
  - Usually performs CRUD operations but adds the required business logic.

- XxxService
  - The layer where the business logic resides.
  - Should "speak" in simple objects - Strings, ints, etc. - as much as possible.

- XxxController
  - The UI interaction layer.
  - Should speak to Services only.

- XxxUtil
  - Util may be called in any context, stateless.
  - Should not depend on any service in the system.
  - For example, org.mycompany.util.NumberUtility

- XxxHelper 
  - Functionality that help to achieve a specific package context.
  - For example, AccountHelper in org.mycompany.account.AccountHelper

- Reference:
http://stackoverflow.com/questions/995473/what-naming-convention-do-you-use-for-the-service-layer-in-a-spring-mvc-applicat
http://stackoverflow.com/questions/1866794/naming-classes-how-to-avoid-calling-everything-a-whatevermanager
http://stackoverflow.com/questions/2676704/naming-convention-for-utility-classes-in-java
http://stackoverflow.com/questions/8403535/when-do-i-call-my-class-controller-manager-or-service
http://lcsd05.cs.tamu.edu/slides/keynote.pdf


Class Naming - Interfaces Daos etc
----------------------------------
- NOTE: Work in progress
- No Impl or Dao:
http://isagoksu.com/2009/development/java/naming-the-java-implementation-classes/
http://stackoverflow.com/questions/2814805/java-interfaces-implementation-naming-convention


Property variable naming
------------------------
- When using property variables, the naming of the variable should be hierarchical and reflect the class name
- If it is used in multiple places, the name should be more general, rather then reflecting the class name.

- Start with class name followed by a period.
- Next can either be a unique identifier, for example in the case of a bean that has more then one instance 
  followed by a period.
- Unique identifiers, if used, should be grouped together.
- Multiple unique identifiers can be used to create a hierarchy if required.
- Final value should be the name of the property.

- CamelCaps should be used, with a lowercase first letter.
- Any acronyms or initialism should be converted to lower case.

- Progression of naming hierarchy should be from general to specific.

- Use comment fencing to indicate beginning and end of grouping.


- Example: Class FooServlet.java has three properties, isProduction, externalNameToInternalNameMap and endPointUrl:

# BEGIN FooServlet

fooservlet.productionMode=true
fooservlet.externalNameToInternalNameMap=ABC,123
fooservlet.endPointUrl=http://service.com/service

# END FooServlet


- Example: If there is more then one instance of the class FooServlet:

# BEGIN FooServlet Client ABC

FooServlet.ClientAbc.ProductionMode=true
FooServlet.ClientAbc.ExternalNameToInternalNameMap=ABC,123
FooServlet.ClientAbc.EndPointUrl=http://service.com/service

# END FooServlet Client ABC


# BEGIN FooServlet Client XYZ

FooServlet.ClientXyz.ProductionMode=true
FooServlet.ClientXyz.ExternalNameToInternalNameMap=XYZ,456
FooServlet.ClientXyz.EndPointUrl=http://service.com/service

# END FooServlet Client XYZ


Spring MVC Naming
-----------------
- The backing jsp (or other view technology) should match the name of the requested page.
  - Requested page is `Login.html`, the backing jsp should be `Login.jsp`.
  
- If there is a bean that is used in the view domain, it should also match the name of the requested page, with the
  suffix *page.
  - Request page is `Login.html`, the domain object should be `LoginPage.java`.
 
- The class that maps to the request should also match name of the requested page.
  - It may be appropriate to group the mapping methods into one more generic class.
  - Request page is `Login.html`, the class should be `Login.java`.

- The method in the class that maps the request should start with `handle` and end with either `Post` or `Get`.





