# SQL Linter

A configurable SQL linter and formatter derived from the open-source SQLFluff project.

Dechapon25 provides SQL linting and formatting capabilities with support for multiple SQL dialects, templating, automated fixes, command-line tooling, and optional Rust-backed parsing and lexing.

> **Project status:** Dechapon25 is an independent fork/development project derived from SQLFluff. It is not an official SQLFluff distribution and is not affiliated with or endorsed by the SQLFluff maintainers.
>
> Changes in this repository may differ from the upstream SQLFluff project.

## Table of Contents

- [About](#about)
- [Supported Dialects](#supported-dialects)
- [Supported Templates](#supported-templates)
- [Getting Started](#getting-started)
- [Rust Parser and Lexer](#rust-parser-and-lexer)
- [Docker](#docker)
- [Documentation](#documentation)
- [Development](#development)
- [Security](#security)
- [Contributing](#contributing)
- [Upstream Project](#upstream-project)
- [Attribution](#attribution)
- [License](#license)

## About

Dechapon25 is a configurable SQL linter designed to help developers and data teams produce clean, consistent, and maintainable SQL.

The project is derived from the open-source SQLFluff project and retains compatibility with upstream functionality where practical.

### Key capabilities

- SQL linting
- Automated SQL formatting and fixing
- Support for multiple SQL dialects
- Jinja templating
- SQL parameter placeholders
- Python format strings
- dbt integration
- Command-line tooling
- Optional Rust-backed parsing and lexing
- Extensible linting rules
- Automated testing and development tooling

The goal of this repository is to provide a maintained development branch with project-specific improvements while preserving compatibility with the upstream SQLFluff ecosystem where practical.

Because this is an independent fork, behavior, compatibility, supported versions, and release schedules may differ from upstream SQLFluff.

## Supported Dialects

The project supports a broad range of SQL dialects, including:

- ANSI SQL
- Athena
- BigQuery
- ClickHouse
- Databricks
- Db2
- Doris
- DuckDB
- Exasol
- FlinkSQL
- Greenplum
- Hive
- Impala
- MariaDB
- Materialize
- MySQL
- Oracle
- PostgreSQL
- Redshift
- Snowflake
- SOQL
- SparkSQL
- SQLite
- StarRocks
- Teradata
- Transact-SQL (T-SQL)
- Trino
- Vertica

Dialect support may vary depending on the version and changes introduced in this repository.

If you require support for a dialect or syntax that is not currently available, open an issue with a minimal example of the relevant SQL syntax.

Do not include passwords, API keys, access tokens, private credentials, or other sensitive information in issues.

## Supported Templates

Dechapon25 supports several SQL templating approaches, including:

- Jinja
- SQL parameter placeholders
- Python format strings
- dbt through the appropriate plugin

Additional dependencies may be required depending on your templating workflow.

## Getting Started

### Installation

Before installing a package, verify the distribution name, package owner, release source, and version you intend to use.

For compatibility with upstream SQLFluff, this project may use the `sqlfluff` distribution name. If a separate distribution name is used for Dechapon25 releases, use that distribution name instead.

For example:

```bash
python -m pip install sqlfluff