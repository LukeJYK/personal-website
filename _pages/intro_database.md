---
layout: page
permalink: /notes/intro_database
title: Database Systems
description: CMU 15-445/645 (FALL 2021) 
nav: false
---
<aside>
📌 CMU Fall 2021, [https://15445.courses.cs.cmu.edu/fall2021/](https://15445.courses.cs.cmu.edu/fall2021/)

</aside>

<aside>
📌 Instructor: Andrew Crotty

</aside>

# Lecture 1: Introduction

**Focus on**: Relational database, storage, execution, concurrency control, recovery, distributed databases and potpourri.

1. For getting data from a data form using Python, several Data Integrity problems:
- Different names of one artist
- Overwrite the year (integer) with an invalid string
- one album contains several artists
- Delete artist

Several Implementation problems:

- Particular record
- Create new application uses same database.
- Concurrency problem
- Delete artist

Several Durability problems:

- Machine crash while uploading new records
- Replicate the database on multiple machines for high availability.

> **DBMS**: to allow definition, creation, querying, update, and administration of databases
> 

1. **Data Model**: collection of concepts for describing the data in a database.
    
    such as: Relational, K/V, Graph, Document, Column-family, Array/Matrix(Machine Learning), Hierarchical, Network, Multi-value.
    
    **Schema**: Description of a particular collection of data , using a given data model.
    

1. **Relational Model**

Database abstraction to avoid maintenance:

- Store database in simple data structures.
- Access data through high-level language, DBMS figures out best strategy.
- Physical storage left up to the DBMS implementation.

**Structure**: Definition of the database’s relations and their contents.

**Integrity**: Ensure database’s contents satisfy constraints.

**Manipulation**: Programming interface for accessing and modifying a database’s contents.

e.g.  Artist(name, year, country) **NULL** is a member of every domain.

***n-ary Relation = Table with n columns***

Primary key identifies a single tuple. (Some DBMSs create an internal primary key if a table does not define one. e.g. SEQUENCE AUTO_INCREMENT)

Foreign Key specifies that an attribute from on relation has to map to a tuple in another relation.

1. Data Manipulation Languages()