# LLM-Text-to-SQL-Architectures

A comprehensive guide and implementation of architectural patterns that utilize Large Language Models (LLMs) for the efficient generation of SQL from natural language text.

For comprehensive details on the architectural patterns mentioned below, please refer to the accompanying article on Medium. This piece delves into the utilization of LLMS for enhanced BigQuery interactions. You can access the article via this link.

[Architectural Patterns for Text-to-SQL: Leveraging LLMs for Enhanced BigQuery Interactions](https://medium.com/@kumar.Vishalp/architectural-patterns-for-text-to-sql-leveraging-llms-for-enhanced-bigquery-interactions-59756a749e15?source=friends_link&sk=22b06c1644e968023b24db79f2995588)

## Table of Contents

- [Introduction](#introduction)
- [Architectural Patterns](#architectural-patterns)
  - [Pattern I](#pattern-i)
  - [Pattern II](#pattern-ii)
  - [Pattern III](#pattern-iii)
  - [Pattern IV](#pattern-iv)
  - [Pattern V](#pattern-v)
- [Getting Started](#getting-started)
- [Challenges and Limitations](#challenges-and-limitations) (In Progress)
- [Contributing](#contributing)
- [License](#license)

## Introduction 📘

This repository offers an in-depth exploration into Text-to-SQL conversion, emphasizing the role of LLMs in enhancing the SQL generation process. With the advent of LLMs, there is a promising opportunity to streamline the translation of natural language to SQL. We explore various architectural patterns that leverage the capabilities of LLMs in this exciting field.

## Architectural Patterns 🏗️

### Pattern I: Intent Detection and Entity Recognition with Text-to-SQL
Utilizing LLMs to identify intent, extract entities, and subsequently generate SQL.

<div align="center">
<img src="./img/pattern-1.png" alt="Architecture (100-Foot View)" width="800" height="450"/>
</div>

<div align="center">
  Click on image to enlarge
</div>

### Pattern II: LLM Flow with Retrieval-Augmented Generation (RAG)
Incorporating Retriever-Augmented Generation (RAG) with table and column metadata to pinpoint relevant database schema elements, allowing LLMs to formulate queries based on natural language questions.

<div align="center">
<img src="./img/pattern-2.png" alt="Architecture (100-Foot View)" width="800" height="450"/>
</div>

<div align="center">
  Click on image to enlarge
</div>

### Pattern III: Using SQL Agents
Adopting an autonomous agent-based approach where a BigQuery SQL agent, equipped with an ODBC connection, iteratively attempts and refines SQL queries with minimal external guidance.

<div align="center">
<img src="./img/pattern-3.png" alt="Architecture (100-Foot View)" width="800" height="450"/>
</div>

<div align="center">
  Click on image to enlarge
</div>

### Pattern IV: Direct Schema Inference with Self-Correction
Implementing a self-correcting mechanism where the LLM receives direct schema input, generates an SQL query, and upon execution failure, uses the error feedback to self-correct and retry until successful. This pattern also explores using the Code-Chat Bison model to potentially reduce costs and improve latency.

<div align="center">
<img src="./img/pattern-4.png" alt="Architecture (100-Foot View)" width="800" height="450"/>
</div>

<div align="center">
  Click on image to enlarge
</div>

### Pattern V: Direct Schema Inference, Self-Correction & Optimization
Similar to Pattern IV but employs a stochastic approach with a temperature setting of 1. It runs multiple trials and selects the query that executes the fastest.

<div align="center">
<img src="./img/pattern-5.png" alt="Architecture (100-Foot View)" width="800" height="450"/>
</div>

<div align="center">
  Click on image to enlarge
</div>

