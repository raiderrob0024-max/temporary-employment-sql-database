# Portfolio review notes

## Source selection
- Chosen schema: `UPDATED DATABASE FILE.sql`, the later expanded version with more placement, job history, and session records compared with the two earlier phase-2 database drafts.
- Chosen queries: `TEC_PROJECT QWERY 2.0.sql`, which contains all ten numbered business queries; the earlier `TEC_PROJECT QWERY.sql` is incomplete.
- Group report: `MIS 150 Group Project-Phase 2.docx` provides a final ERD and explicit member contributions.

## Changes made for GitHub usability
- Files were renamed into descriptive paths.
- `sql/02_business_queries.sql` was prepended with `USE tec_project;` and an initial exploratory `SELECT * FROM tec_project.opening;` was removed. The numbered reporting queries themselves are preserved as supplied.
- The original queries file is preserved in `docs/original_submitted_queries.sql`.
- The database setup script is included unmodified, aside from renaming the file.

## Important caution
- The database script executes `DROP DATABASE IF EXISTS tec_project;` and replaces the database.
- This is an academic prototype and has not been independently run in a MySQL instance during this portfolio packaging. Some sample record dates are not in chronological order relative to enrollment/session dates; no claim of production data consistency is made.
- Phase 2 is a group deliverable. The final report identifies Robert's contribution as schema/relationship and integrity review, and does not individually attribute all SQL queries to him.
- Do not upload textbook pages, instructional slide excerpts, or CourseHero materials from the working folder to this public portfolio; these are external reference materials.
