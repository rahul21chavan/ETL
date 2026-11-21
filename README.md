# Data & AI Migration Engineering

A documentation-focused portfolio repository covering AI-assisted modernization of legacy SQL, ETL, and SAS workloads for cloud data platforms.

## Project areas

### 1. SQL Migration Suite
The [SQL Migration Suite whitepaper](SQL_Migration_Suite_Whitepaper.md) describes a modular platform for assessing and modernizing SQL and ETL workloads.

- SQL complexity analysis and migration-effort estimation
- LLM-assisted conversion across legacy SQL dialects and cloud targets
- SQL optimization and before/after review
- Informatica and DataStage ETL complexity analysis
- ETL migration concepts for Snowpark PySpark, Snowflake SQL, Matillion, and dbt
- Reporting, bulk processing, and security considerations

### 2. SAS to Snowflake multi-agent migration
The [SAS-to-Snowflake whitepaper](hi.md) outlines a multi-agent approach to legacy SAS modernization:

1. **Parse Agent** — identifies SAS structures and creates an intermediate representation.
2. **LLM Rule Agent** — proposes Snowflake SQL translations for parsed blocks.
3. **Validation Agent** — checks generated SQL and flags potential semantic or syntax issues.
4. **Feedback Agent** — records failures and supports iterative refinement.

The document describes a proposed stack using React, FastAPI, Python, LangChain, and hosted LLMs.

## Repository contents

| File | Description |
|---|---|
| `SQL_Migration_Suite_Whitepaper.md` | Architecture and module-level design for SQL and ETL modernization |
| `hi.md` | SAS-to-Snowflake multi-agent migration concept and architecture |

## Scope and status

This repository currently presents technical design and whitepaper material. The documents describe intended capabilities and architecture; they should not be interpreted as proof that every described module is implemented, production-ready, or independently runnable from this repository.

## Suggested review areas

- Validate SQL and SAS-to-Snowflake translations against representative test cases.
- Measure semantic equivalence, execution correctness, and manual-review rates.
- Add reproducible examples, test fixtures, and implementation links as modules become available.
- Keep credentials in environment variables or a secrets manager; never commit API keys.

## Topics

Data Engineering · SQL Migration · ETL Modernization · SAS · Snowflake · PySpark · Databricks · Generative AI · Multi-Agent Systems · LLM-assisted Code Generation
