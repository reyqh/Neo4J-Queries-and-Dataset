# Neo4J-Queries-and-Dataset
Neo4j graph database project using Cypher to model movie and personalised-learning data, implement CRUD operations, import CSV data, and perform graph-based queries and analysis.

# Neo4j Graph Database & Cypher

This project explores graph database development using Neo4j and Cypher. It covers CRUD operations, graph modelling, relationships, CSV data import, filtering, aggregation and analysis across two different datasets.

## Project Overview

### 1. Movie Graph Database

The first part uses Neo4j's Movie Graph dataset and focuses on CRUD operations and relationship-based queries.

The project involved:

- Adding a movie, actors and director to the graph
- Creating `ACTED_IN` and `DIRECTED` relationships
- Finding actors who also directed movies they appeared in
- Finding actor pairs who appeared together in multiple movies
- Finding movies and co-actors associated with Keanu Reeves
- Identifying and deleting movies with the lowest rating

`MERGE` was used when adding the new movie and people to avoid creating duplicate nodes. `DETACH DELETE` was used when removing movies so that their connected relationships were also removed. 

### 2. Personalised Learning Database

The second part involved importing a personalised-learning CSV dataset into Neo4j and modelling the data using students, courses and relationships.

The dataset contains information including:

- Student ID
- Age and gender
- Education level
- Course
- Video engagement
- Quiz performance
- Assignment completion
- Engagement level
- Final exam scores
- Learning style
- Feedback scores
- Dropout likelihood 

The CSV data was imported using `LOAD CSV WITH HEADERS`, with `MERGE` used to prevent duplicate students, courses and relationships when running the import multiple times. 

### 3. Cypher Queries & Data Analysis

Cypher queries were developed to analyse the personalised-learning dataset, including:

- Finding young female high-school students who prefer visual learning and are unlikely to drop out
- Identifying courses with high student engagement and assignment completion
- Finding the course with the highest feedback rating
- Counting male cybersecurity students who scored below 40% in their final exam with low engagement
- Grouping students likely to drop out by learning style and education level

The queries demonstrate graph traversal using relationships, conditional filtering with `WHERE`, aggregation using functions such as `MAX()` and `COUNT()`, grouping, sorting and limiting results.

## Key Technologies & Concepts

- Neo4j
- Cypher
- Graph Databases
- Graph Data Modelling
- CRUD Operations
- Nodes & Relationships
- `MATCH`
- `MERGE`
- `CREATE`
- `DETACH DELETE`
- `LOAD CSV`
- Aggregation
- Graph Traversal
- Data Filtering
- Data Grouping & Sorting
- CSV Data Import
