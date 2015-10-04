# Google App Engine Datastore:
## Naming conventions (Terminologies) in GAE
* Tables --> Entities
  * Entities:
    - The colums are not fixed. In a table you had to have a fixed number of columns that you define when you define a table and in a GAE Entity, you can have whatever columns you want. Even entities of the same type don't have to have the same column.

    - The entities all have an ID. And this id can either be assigned automatically by the Datastore or you can use your own IDs (integers/strings/etc.)

    - Entities have this notion or parents / ancestors. And this is a relationship to other entities that has a couple of very specific use-cases.
    See: https://www.udacity.com/course/viewer#!/c-cs253/l-48756013/m-48734227 for examples

* SQL --> GQL
	* Its a simplified version of SQL that works only in datastore. The main difference is all queries begin with SELECT * so there is no way to select individual columns. So this actually simplifies a lot of queries we can do. For Eg: We can't do joins.
	* In the App Engine datastore, we won't be doing any joins whatsoever because its not possible.

	* Another difference is, in generic SQL Databases, you can arbitrary queries, no matter how slow with or without indices however in App Engine, all queries must be indexed.

## Datastore is sharded and replicated
	* Google doesn't share the details of how this is implemented at a very low level, but a lot of the constraints that we would be dealing with imply that the database is both sharded and replicated.
	* 