Dechapon25 SQL Linter

A SQL Linter for Humans

Dechapon25 is a SQL linting and formatting project based on the open-source SQLFluff project.

It provides configurable SQL linting, automated fixes, support for multiple SQL dialects, templating capabilities, and development tooling to help teams maintain consistent, readable, and maintainable SQL code.

Project status: Dechapon25 is an independent fork of SQLFluff. Changes introduced in this repository may differ from those in the upstream SQLFluff project.



\

Table of Contents

About

Supported Dialects

Supported Templates

Getting Started

Rust Parser and Lexer

Docker

Documentation

Development

Security

Contributing

Upstream Project

License

About

Dechapon25 is a configurable SQL linter designed to help developers and data teams produce clean, consistent, and maintainable SQL.

The project is derived from SQLFluff and retains compatibility with many capabilities provided by the upstream project.

Key capabilities include:

SQL linting

Automated SQL formatting and fixing

Support for multiple SQL dialects

Jinja templating

SQL parameter placeholders

Python format strings

dbt integration

Command-line tooling

Optional Rust-backed parsing and lexing

Extensible linting rules

Automated testing and development tooling

The objective of this repository is to provide a maintained development branch with project-specific improvements while preserving compatibility with the upstream SQLFluff ecosystem wherever practical.

Supported Dialects

The project supports a broad range of SQL dialects, including:

ANSI SQL

Athena

BigQuery

ClickHouse

Databricks

Db2

Doris

DuckDB

Exasol

FlinkSQL

Greenplum

Hive

Impala

MariaDB

Materialize

MySQL

Oracle

PostgreSQL

Redshift

Snowflake

SOQL

SparkSQL

SQLite

StarRocks

Teradata

Transact-SQL (T-SQL)

Trino

Vertica

Dialect support may vary depending on the version and changes introduced in this repository.

If you require support for a dialect or syntax that is not currently available, please open an issue and include a clear example of the relevant SQL syntax.

Supported Templates

Dechapon25 supports several SQL templating approaches, including:

Jinja

SQL parameter placeholders

Python format strings

dbt through the appropriate plugin

Additional dependencies may be required depending on your templating workflow.

Getting Started

Installation

Install the package using pip:

pip install sqlfluff 

The package name remains sqlfluff for compatibility with the upstream project unless this repository publishes a separately named distribution.

Create a SQL file:

echo " SELECT a + b FROM tbl; " > test.sql 

Run the linter:

sqlfluff lint test.sql --dialect ansi 

To automatically fix supported violations, run:

sqlfluff fix test.sql --dialect ansi 

Example output:

== [test.sql] FAIL L: 1 | P: 1 | LT01 | Expected only single space before 'SELECT' keyword. L: 1 | P: 1 | LT02 | First line should not be indented. L: 1 | P: 11 | LT01 | Expected only single space before binary operator '+'. L: 1 | P: 14 | LT01 | Expected only single space before naked identifier. 

Rust Parser and Lexer

An optional Rust-backed parser and lexer is available through the rs extra:

pip install sqlfluff[rs] 

On supported CPython 3.10+ platforms, this may install a prebuilt ABI3 wheel.

If a compatible wheel is unavailable for your platform, the package may be built from source.

Building from source requires:

Rust

A functional C/C++ build environment

A compatible Python development environment

The recommended method for installing Rust is rustup.

Docker

SQL linting can be run in a containerized environment when Docker is preferred.

Example:

docker run --rm -v "$PWD:/workspace" -w /workspace sqlfluff/sqlfluff lint test.sql --dialect ansi 

For production environments, use an explicitly selected and reviewed image version rather than relying on a mutable latest tag.

Documentation

For SQLFluff-compatible documentation and detailed CLI information, refer to the upstream documentation:

SQLFluff Documentation

Relevant documentation includes:

CLI usage

Configuration

Linting rules

SQL dialects

Templating

dbt integration

Architecture

Development

Documentation specific to Dechapon25 should be added to this repository as project-specific behavior diverges from upstream SQLFluff.

Development

Clone the repository:

git clone https://github.com/Marslevelsafety/Dechapon25.git cd Dechapon25 

Install the development dependencies according to the project's development documentation.

Before submitting changes, run the relevant test and linting commands.

Typical checks may include:

pytest 

and:

ruff check . 

For changes affecting SQL parsing, linting rules, dialects, templating, or CLI behavior, add or update the corresponding tests.

Security

Security issues should not be disclosed publicly through standard GitHub issues when doing so could expose a vulnerability or sensitive information.

Please report security issues privately through the repository's configured security reporting mechanism.

Do not include the following information in public issues:

API keys

Access tokens

Passwords

Private credentials

Private user information

Exploit details that could enable immediate abuse

If you discover a credential that has been accidentally committed to the repository:

Revoke or rotate the credential immediately.

Remove the secret from the affected code.

Determine whether the secret exists in the repository history.

Report the incident privately.

Do not rely solely on deleting the file from the latest commit.

Contributing

Contributions are welcome.

Before beginning a substantial change, please open an issue describing:

The problem

The proposed solution

Expected behavior

Compatibility considerations

Tests that will be added or modified

Pull requests should:

Include appropriate tests.

Keep changes focused.

Avoid unrelated modifications.

Follow the project's formatting and linting requirements.

Avoid committing secrets or credentials.

Clearly describe any behavior changes.

AI-assisted contributions are welcome provided that contributors review, understand, and take responsibility for the resulting code.

Upstream Project

Dechapon25 is derived from the open-source SQLFluff project.

Upstream repository:

https://github.com/sqlfluff/sqlfluff

The upstream project provides the original SQL linting architecture, dialect support, documentation, and much of the functionality used by this repository.

This repository is not an official SQLFluff repository and must not be represented as being operated by or endorsed by the SQLFluff maintainers.

For upstream issues, documentation, releases, and project information, refer to the official SQLFluff repository.

Attribution

This project contains or is derived from software originating from SQLFluff.

Original project:

SQLFluff — The SQL Linter for Humans

https://github.com/sqlfluff/sqlfluff

Copyright and licensing information for upstream components is retained in accordance with the applicable project licenses.

Review the repository's LICENSE files and individual component licenses before redistributing modified versions.

License

Dechapon25 is distributed under the applicable open-source license contained in this repository.

See:

LICENSE 

and any additional license or notice files included with the project.

Third-party components may be distributed under their respective licenses.

Project Identity

Dechapon25

Repository:

https://github.com/Marslevelsafety/Dechapon25

Upstream:

https://github.com/sqlfluff/sqlfluff

This repository is an independent fork and development project. It is not affiliated with or endorsed by the official SQLFluff project.

