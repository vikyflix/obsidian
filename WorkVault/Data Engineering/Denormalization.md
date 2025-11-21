---
title: "Denormalization - Wikipedia"
source: "https://en.wikipedia.org/wiki/Denormalization"
author:
published: 2001-09-30
created: 2025-11-13
description:
tags:
---
**Denormalization** is a strategy used on a previously- [normalized](https://en.wikipedia.org/wiki/Database_normalization "Database normalization") database to increase performance. In [computing](https://en.wikipedia.org/wiki/Computing "Computing"), denormalization is the process of trying to improve the read performance of a [database](https://en.wikipedia.org/wiki/Database "Database"), at the expense of losing some write performance, by adding [redundant](https://en.wikipedia.org/wiki/Redundancy_\(information_theory\) "Redundancy (information theory)") copies of data or by grouping data.[^1] [^2] It is often motivated by [performance](https://en.wikipedia.org/wiki/Computer_performance "Computer performance") or [scalability](https://en.wikipedia.org/wiki/Scalability "Scalability") in [relational](https://en.wikipedia.org/wiki/Relational_model "Relational model") [database software](https://en.wikipedia.org/wiki/DBMS "DBMS") needing to carry out very large numbers of read operations. Denormalization differs from the [unnormalized form](https://en.wikipedia.org/wiki/Unnormalized_form "Unnormalized form") in that denormalization benefits can only be fully realized on a data model that is otherwise normalized.

## Implementation

A [normalized](https://en.wikipedia.org/wiki/Database_normalization "Database normalization") design will often "store" different but related pieces of information in separate logical tables (called relations). If these relations are stored physically as separate disk files, completing a database [query](https://en.wikipedia.org/wiki/Information_retrieval "Information retrieval") that draws information from several relations (a *[join operation](https://en.wikipedia.org/wiki/Join_\(SQL\) "Join (SQL)")*) can be slow. If many relations are joined, it may be prohibitively slow. There are two strategies for dealing with this by denormalization:

- "DBMS support": The database management system stores redundant copies in the background, which are kept consistent by the DBMS software
- "DBA implementation": The database administrator (or designer) design around the problem by denormalizing the logical data design

### DBMS support

With this approach, database administrators can keep the logical design normalized, but allow the [database management system](https://en.wikipedia.org/wiki/Database_management_system "Database management system") (DBMS) to store additional redundant information on disk to optimize query response. In this case it is the DBMS software's responsibility to ensure that any redundant copies are kept consistent. This method is often implemented in [SQL](https://en.wikipedia.org/wiki/SQL "SQL") as indexed views ([Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server "Microsoft SQL Server")) or [materialized views](https://en.wikipedia.org/wiki/Materialized_view "Materialized view") ([Oracle](https://en.wikipedia.org/wiki/Oracle_Database "Oracle Database"), [PostgreSQL](https://en.wikipedia.org/wiki/PostgreSQL "PostgreSQL")). A view may, among other factors, represent information in a format convenient for querying, and the index ensures that queries against the view are optimized physically.

### DBA implementation

With this approach, a database administrator or designer has to denormalize the logical data design. With care this can achieve a similar improvement in query response, but at a cost — it is now the database designer's responsibility to ensure that the denormalized database does not become inconsistent. This is done by creating rules in the database called *[constraints](https://en.wikipedia.org/wiki/Constraint_satisfaction "Constraint satisfaction")*, that specify how the redundant copies of information must be kept synchronized, which may easily make the de-normalization procedure pointless. It is the increase in logical [complexity](https://en.wikipedia.org/wiki/Complexity_of_constraint_satisfaction "Complexity of constraint satisfaction") of the database design and the added complexity of the additional constraints that make this approach hazardous. Moreover, constraints introduce a [trade-off](https://en.wikipedia.org/wiki/Trade-off "Trade-off"), speeding up reads (`SELECT` in SQL) while slowing down writes (`INSERT`, `UPDATE`, and `DELETE`). This means a denormalized database under heavy write load may offer *worse* performance than its functionally equivalent normalized counterpart.

A denormalized data model is not the same as a data model that has not been normalized, and denormalization should only take place after a satisfactory level of normalization has taken place and that any required constraints and/or rules have been created to deal with the inherent anomalies in the design. For example, all the relations are in [third normal form](https://en.wikipedia.org/wiki/Third_normal_form "Third normal form") and any relations with [join dependencies](https://en.wikipedia.org/wiki/Join_dependency "Join dependency") and [multi-valued dependencies](https://en.wikipedia.org/wiki/Multivalued_dependency "Multivalued dependency") are handled appropriately.

Examples of denormalization techniques include:

- "Storing" the count of the "many" elements in a [one-to-many relationship](https://en.wikipedia.org/wiki/One-to-many_\(data_model\) "One-to-many (data model)") as an attribute of the "one" relation
- Adding attributes to a relation from another relation with which it will be joined
- [Star schemas](https://en.wikipedia.org/wiki/Star_schema "Star schema"), which are also known as fact-dimension models and have been extended to [snowflake schemas](https://en.wikipedia.org/wiki/Snowflake_schema "Snowflake schema")
- Prebuilt summarization or [OLAP cubes](https://en.wikipedia.org/wiki/OLAP_cube "OLAP cube")

With the continued dramatic increase in all three of storage, processing power and bandwidth, on all levels, denormalization in databases has moved from being an unusual or extension technique, to the commonplace, or even the norm. For example, one specific downside of denormalization was, simply, that it "uses more storage" (that is to say, literally more columns in a database). With the exception of truly enormous systems, increased storage requirements is considered a relatively small problem in the 2020s.

## See also

- [Cache (computing)](https://en.wikipedia.org/wiki/Cache_\(computing\) "Cache (computing)")
- [Normalization](https://en.wikipedia.org/wiki/Database_normalization "Database normalization")
- [Scalability](https://en.wikipedia.org/wiki/Scalability "Scalability")

## References

[^1]: G. L. Sanders and S. K. Shin. [Denormalization effects on performance of RDBMS](https://web.archive.org/web/20171201030308/https://pdfs.semanticscholar.org/2c79/069c01ba8d598f32e61fe367ef6d261a0cb4.pdf). In Proceedings of the HICSS Conference, January 2001.

[^2]: S. K. Shin and G. L. Sanders. [Denormalization strategies for data retrieval from data warehouses](http://portal.acm.org/citation.cfm?id=1217757). Decision Support Systems, 42(1):267-282, October 2006.