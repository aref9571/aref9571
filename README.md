Aref Hosseini
Junior Backend / Software Engineer · Java · Python · PostgreSQL

Final-year Computer Science student at Ventspils University of Applied Sciences, Latvia (graduating June 2027). I build backend services with Java/Spring Boot and Python/FastAPI, and I care about tests, database design and clean, maintainable code.

📍 Ventspils, Latvia · 🕒 Available part-time (20 h/week) now, full-time from July 2027

 

Featured projects
Everything in this section is public. You can check it in the code, the tests and the CI runs.

TraceLite: error-monitoring backend · in progress
Java 21 Spring Boot 3.5 Spring Data JPA PostgreSQL 17 Flyway Testcontainers Docker Compose GitHub Actions

Applications send error events to a REST API. TraceLite groups them into issues so developers can triage repeated failures as one problem.

Event ingestion API (POST /api/v1/events) with request validation, a streaming request-size limit and RFC 9457 problem-detail error responses that never expose internal details.
Groups errors into issues with a deterministic SHA-256 fingerprint of the exception type and the normalised stack frames. The fingerprint ignores generated names such as lambdas, proxies and CGLIB classes.
Uses a PostgreSQL INSERT … ON CONFLICT upsert, so simultaneous events never create duplicate issues. A new event automatically reopens a resolved issue.
Issue search with filters, case-insensitive text search (backed by pg_trgm indexes), sorting and pagination. The API also covers per-issue event history, daily statistics and a resolve/reopen lifecycle with optimistic locking.
PostgreSQL schema managed by Flyway migrations, with check constraints, a unique key and indexes.
239 automated tests: unit tests with JUnit 5, Mockito and AssertJ, web-layer tests with MockMvc, and integration tests against a real PostgreSQL through Testcontainers.
GitHub Actions CI builds the project, runs all tests, lints the shell scripts and smoke-tests the packaged JAR against a Docker Compose database.
Documented with architecture decision records plus API, database, security and testing docs.
HookLine: webhook delivery service · early stage
Python 3.12 FastAPI Pydantic v2 pytest ruff mypy GitHub Actions

A service for delivering events to subscriber endpoints, with signed payloads, retries with backoff and a full delivery history planned.

Current stage: application factory, typed settings loaded from the environment, a health endpoint, and a documented modular-monolith design with an API process and a worker process.
CI checks formatting, linting, type checking and tests with coverage on every push.
Numerical Methods in Java: math expression engine
Java 21 Maven JUnit 5

Hand-written tokenizer and recursive-descent parser for real-valued expressions: correct operator precedence, right-associative ^, functions, constants and variables.
Clear error messages that point to the exact column. Detects domain errors such as sqrt(-1) and ln(0), division by zero and non-finite results.
174 JUnit 5 tests, many of them parameterised, run in GitHub Actions CI.
Java Foundations / JobTrackr: structured Java learning project
Java 21 Maven JUnit 5

A day-by-day Java training project built around one domain, a job-application tracker. It covers immutable domain objects and value objects, a repository and service layer, custom exceptions, file persistence with atomic writes, Streams, Optional, and concurrency with executors, atomics and scheduled tasks. It has 268 JUnit 5 tests, run in GitHub Actions CI.

Earlier Python projects

Smart Vending Machine CLI: service layer, JSON persistence with atomic writes, greedy change-making algorithm, pytest.
Expense Tracker: CRUD expense tracker with category summaries and JSON storage, pytest.
Task Manager CLI: layered task manager with JSON persistence, pytest.
Tech stack
Shown in the projects above

Area	Technologies
Languages	Java 21, Python 3.12, SQL
Backend	Spring Boot, Spring Data JPA / Hibernate, FastAPI, Pydantic, REST API design
Databases	PostgreSQL (constraints, indexes, upserts, pg_trgm), Flyway migrations
Testing	JUnit 5, Mockito, AssertJ, MockMvc, Testcontainers, pytest
Tooling	Maven, Git, Docker Compose, GitHub Actions, ruff, mypy
Also used in work, study and other projects: TypeScript, Next.js, C#, SQLAlchemy, Supabase, Docker, AWS (EC2, RDS, S3), JWT authentication and role-based access control, Vitest, Playwright.

Experience
IT & Software Trainee, Istanbul Arel University, Istanbul, Türkiye (Erasmus+ traineeship) · Jul 2026 – Aug 2026

Developed and maintained applications with Java, FastAPI and PostgreSQL. Tested and debugged them, fixing software defects. Used Git for version control.
Backend Developer (part-time), Sama Tajhiz Vira, Tehran, Iran · Feb 2023 – May 2024

Contributed to REST API development with FastAPI and PostgreSQL as part of a backend team.
Took part in Docker-based deployment and hosting of services on AWS. Worked with Git and CI/CD workflows in a shared codebase.
Education
BSc (Academic Bachelor of Natural Sciences) in Computer Science, Ventspils University of Applied Sciences, Latvia · Sep 2024 – Jun 2027 (expected)

Average grade 8.5/10. Relevant courses: Object-Oriented Programming, Data Structures and Algorithms, Database Design and SQL, Software Testing, Cloud Computing.
Erasmus+ Exchange, Computer Science, University of Oulu, Finland · Sep 2025 – May 2026

Average grade 4.3/5.
Certificates & languages
Certificates: Python for Everybody series (University of Michigan, Coursera); Object-Oriented Programming in Python (Duke University, Coursera); Production Machine Learning Systems (Google Cloud)
Languages: Persian (native), English (professional working proficiency)
GitHub activity
 


💬 Open to junior backend / software engineering roles and internships in Latvia, the EU, or remote. Feel free to reach out on LinkedIn or by email.
