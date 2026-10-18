# Temporary Employment Corporation (TEC) | MySQL Database Project

**Relational Database Design · SQL · ERD · Referential Integrity · Business Reporting**

## Overview
A university team project for a hypothetical temporary staffing agency that needed to manage job candidates, qualifications, client companies, job openings, placements, employment histories, courses, and training enrollment. The team translated business rules into a relational model and implemented a MySQL database to support staffing and training decisions.

**Context:** Sacramento State, MIS 150, Fall 2025. This is an **academic group project**, not a deployed production system.

## My role: Database Architect (group project)
As documented in the team's final report, **Robert Velazquez** focused on defining table relationships and referential integrity across foreign keys; reviewed the schema's consistency and composite key definitions; helped prepare table descriptions; and reviewed `CREATE TABLE` statements for constraints and alignment with the ERD. Other team members led project management, ERD drafting, data loading, query development, and documentation.

## What the database models
- Client companies and their job openings
- Candidate qualifications and placement records
- Employment history and hours worked
- Training courses, prerequisites, scheduled sessions, and candidate enrollment
- Employees associated with client companies

The final SQL schema has **12 tables**, including bridge tables that resolve many-to-many relationships. The team documented its assessment of normalization through **Third Normal Form (3NF)**.

## SQL and reporting
The query collection contains **10 analytical queries** covering topics such as:
- Prerequisite requirements and available training sessions
- Candidate job histories and placement frequency
- Available job openings by company
- Course enrollment revenue and qualification distribution

These use joins, grouping, filtering, and aggregate functions such as `COUNT()` and `SUM()`.

## Files
| File | Purpose |
| --- | --- |
| [`sql/01_create_and_populate_database.sql`](sql/01_create_and_populate_database.sql) | Final expanded MySQL table definitions and sample records |
| [`sql/02_business_queries.sql`](sql/02_business_queries.sql) | Ten business reporting queries; adds `USE tec_project;` for convenience |
| [`docs/MIS150_Final_Group_Report.docx`](docs/MIS150_Final_Group_Report.docx) | Group report, final ERD, data dictionary, normalization explanation, query examples |
| [`docs/original_submitted_queries.sql`](docs/original_submitted_queries.sql) | Unaltered reference copy of the original query script |
| [`PORTFOLIO_NOTES.md`](PORTFOLIO_NOTES.md) | Provenance, scope, and technical limitations |

## Running locally
1. Open **MySQL Workbench** (or another MySQL-compatible SQL client).
2. Run `sql/01_create_and_populate_database.sql`. **Warning:** it starts with `DROP DATABASE IF EXISTS tec_project;`, which deletes an existing database with that name.
3. Run `sql/02_business_queries.sql` against the newly created `tec_project` database.
4. Examine the results to see how the queries answer staffing and training business questions.

## What this project demonstrates
Understanding of relational database structure, primary and foreign keys, many-to-many relationship resolution, SQL reporting, business rules analysis, and technical documentation as part of a cross-functional student team.

## Transparency
This portfolio repository documents the team's submitted academic work, **not** a claim that every SQL statement or diagram was produced individually by Robert. Sample company and candidate records were created for the classroom exercise. The queries have not been independently executed or fully regression-tested in this portfolio preparation; see `PORTFOLIO_NOTES.md`.
