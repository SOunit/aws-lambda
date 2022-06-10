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

- table design
- url design
