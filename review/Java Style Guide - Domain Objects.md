Java Style Guide - Domain Objects
=================================

Database Domain Object
----------------------
- XXXX.domain.database.* package
- Includes hibernate annotations
- Typically excludes JSON annotations
- Typically excludes validation annotations


UI domain object
----------------
- XXXX.domain.page.* package
- Excludes hibernate annotations
- Includes validation annotations
- Can include JSON annotations
- Requires converters to map from database domain to UI domain and back
- With complex hibernate objects, converters can be complex, ie initialized child objects
- Required for some ui forms that have complex validation or properties that don't map to database domain


JSON domain object
------------------
- XXXX.domain.page.* package
- XXXX.domain.json.* package (possible)
- Typically objects end with Request or Response, ie UserRegistrationRequest, UserRegistrationResponse
- Excludes hibernate annotations
- Includes validation annotations
- Includes JSON annotations
- Requires converters to map from database domain to JSON domain and back
- With complex hibernate objects, converters can be complex, ie initialized child objects


Commentary
----------
- There is not a strong seperation between UI domain objects and JSON domain objects.
- If project is mostly RESTful, use JSON domain objects

