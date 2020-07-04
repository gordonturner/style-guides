SQL Style Guide
===============

Schema Naming
-------------
- Schema names should be uppercase with underscores between words.


Table and Column Naming
-----------------------
- Singular, eg USER not USERS.
- Tables and column names should be uppercase with underscores between names.
- Tables of similar usage, or logically associated, should share a consistant prefix.
- Table names should be consistant with the application domain names.
- Any id value should be ID, not TABLE_NAME_ID.
  - Prevents duplicating the name of the table in the id column.
  - Prevents foreign key names that invalid due to length
  
- Reference: 
http://stackoverflow.com/questions/1369593/primary-key-foreign-key-naming-convention
http://stackoverflow.com/questions/338156/table-naming-dilemma-singular-vs-plural-names


Created, Updated Data
---------------------

- Recommendation to include `CREATED_DATE` on most tables
- Recommendation to include `UPDATED_DATE` on tables that are changed


Foreign Key Naming
------------------
- Foreign key names should be uppercase.
- Double underscores between table names.
- Maintain single underscores from original table names.
- Start with `FK__`.
- Example:
``` 
FK__REFERENCING_TABLE__REFERENCED_TABLE
```


Index Naming
------------
- Indexes names should be uppercase.
- Double underscores before table name.
- Maintain single underscores from original table name and column name.
- Start with `IDX__`.
- Example:
``` 
IDX__TABLE_NAME__COLUMN_NAME
```


Uniqueness Naming
-----------------
- Uniqueness names should be uppercase.
- Double underscores before table name.
- Maintain single underscores from original table name and column name.
- Start with `UNQ__`.
- Example:
``` 
UNQ__TABLE_NAME__COLUMN_NAME
```


