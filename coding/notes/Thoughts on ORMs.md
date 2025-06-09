- The object/relational mapping problem is _hard_
- you either have to make your in-memory model more relational, or you complicate your mapping code
- it's reasonable to have a more relational domain model to simplify your object-relational mapping


- To avoid the mapping problem you have two alternatives. Either you use the relational model in memory, or you don't use it in the database.
- To use a relational model in memory basically means programming relations
-  I think NoSQL is serious technology. If you have an application problem that maps well to a NoSQL data model - such as [aggregates](https://martinfowler.com/bliki/AggregateOrientedDatabase.html) or graphs - then you can avoid the nastiness of mapping. Indeed this is often a reason I've heard teams go with a NoSQL solution.

