# url

https://www.youtube.com/watch?v=OfZgHXsYqNE

# points

- what is data modeling?

  - how to store data

- major databases

  - NoSQL
  - Relational Databases

- Relational

  - optimized for storage with data normalization
  - strict schema
  - more computer power to get data
  - performance may degrade as the database scales

- NoSQL

  - optimized for compute rather than storage
  - flexible schema
  - designed for highly scalable applications

- DynamoDB

  - NoSQL from AWS

- DynamoDB Data Modeling

  - different from relational data modeling
  - identify `access patterns` before table design
  - most application needs only one table
  - identify `primary keys` and `indexes` to minimize the number of requests to dynamodb to satisfy each access patterns

- 1 table for entire application

  - use flexible scheme

    - company
    - projects
    - employees

  - identify most suitable `hash key` and `sort key` for each type of record to satisfy the access patterns
  - identify secondary indexes for additional access patterns that cannot be satisfied with the primary key(`hash key` and `sort key`)

- 5 steps process for data-modeling

  - draw an entity model
  - identity relationship(1:1, 1:N, N:N)
  - list down all access pattern for each entity
  - identify the primary key for each entity
  - identify the secondary indexes for additional access patterns if necessary

- sample
  - project management tool
    - draw an entity model
    - identify relationship
      - make many-many to 1-many
        - projects - employees => projects - projects-employees - employees
