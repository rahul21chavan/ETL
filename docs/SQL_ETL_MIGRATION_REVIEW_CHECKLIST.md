# SQL and ETL Migration Review Checklist

Use this checklist when evaluating a proposed legacy SQL or ETL migration.

## Discovery and scope
- [ ] Identify source systems, SQL dialects, ETL tools, and target platform.
- [ ] Inventory tables, views, stored procedures, jobs, schedules, and dependencies.
- [ ] Record business owners, data sensitivity, and operational constraints.
- [ ] Separate in-scope workloads from unsupported or unknown constructs.

## Translation quality
- [ ] Validate joins, filters, aggregations, window functions, and NULL semantics.
- [ ] Review date/time functions, casting, string handling, and numeric precision.
- [ ] Check temporary tables, variables, macros, and procedural control flow.
- [ ] Flag unsupported syntax instead of silently generating a guessed translation.
- [ ] Keep a traceable link between source statements and generated target code.

## Data and execution validation
- [ ] Compare source and target schemas.
- [ ] Run representative test cases with controlled input data.
- [ ] Compare row counts, key aggregates, null rates, and business-critical outputs.
- [ ] Test incremental loads, retries, idempotency, and late-arriving data where relevant.
- [ ] Measure runtime and resource usage on representative volumes.

## Security and operations
- [ ] Use least-privilege service identities and approved secret storage.
- [ ] Avoid embedding credentials in generated code or logs.
- [ ] Review PII handling, retention, and access controls.
- [ ] Define monitoring, alerting, rollback, and recovery procedures.
- [ ] Require human approval for production cutover.

## AI-assisted migration controls
- [ ] Treat LLM output as a proposal, not a verified translation.
- [ ] Preserve prompts, model/version metadata, and review decisions where appropriate.
- [ ] Evaluate semantic equivalence, not only syntactic validity.
- [ ] Record confidence, unsupported constructs, and manual-review outcomes.
- [ ] Do not claim production readiness without repeatable test evidence.

## Status

This is a general review checklist for the migration architectures described in this repository. It does not assert that a production migration tool or automated test suite is implemented here.
