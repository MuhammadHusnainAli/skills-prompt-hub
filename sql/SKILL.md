# SQL Skills

Comprehensive SQL skill suite covering query writing, optimization, debugging, analytics, and cross-dialect translation.

## Overview

This skill provides guidance for all SQL-related tasks across major database systems (PostgreSQL, MySQL, SQL Server, Oracle, SQLite). Use when writing queries, optimizing performance, debugging issues, or translating between dialects.

## Trigger Conditions

Activate this skill when the user:
- Asks to write, create, or generate SQL queries
- Needs help with SELECT, INSERT, UPDATE, DELETE, or DDL statements
- Wants to optimize slow queries or improve database performance
- Has SQL errors or unexpected query results
- Needs to understand or explain complex queries
- Wants to translate SQL between database dialects
- Requires window functions, CTEs, or advanced SQL features
- Needs analytics, reporting, or data quality queries

## Sub-Skills Directory

| Skill | Purpose | When to Use |
|-------|---------|-------------|
| [query-writer](query-writer/SKILL.md) | Write SQL queries from requirements | Creating new queries from scratch |
| [syntax-checker](syntax-checker/SKILL.md) | Validate SQL syntax and structure | Checking queries for errors before execution |
| [query-explainer](query-explainer/SKILL.md) | Explain complex queries in plain language | Understanding existing SQL code |
| [optimizer](optimizer/SKILL.md) | Improve query performance | Slow queries, execution plan analysis |
| [debugger](debugger/SKILL.md) | Debug failing or incorrect queries | Error messages, wrong results |
| [window-functions](window-functions/SKILL.md) | Advanced window/analytic functions | Rankings, running totals, comparisons |
| [performance-tuning](performance-tuning/SKILL.md) | Database-level performance | Indexing, query profiling, bottlenecks |
| [analytics-sql](analytics-sql/SKILL.md) | Analytical and aggregation queries | Reports, metrics, OLAP operations |
| [dialect-translator](dialect-translator/SKILL.md) | Convert between SQL dialects | Migrating queries between databases |
| [data-quality](data-quality/SKILL.md) | Data validation and integrity | NULL handling, constraints, cleansing |
| [reporting](reporting/SKILL.md) | Business reporting queries | KPIs, dashboards, scheduled reports |

## Skill Selection Logic

```
User Request -> Analyze Intent -> Select Appropriate Sub-Skill

"Write a query to..." -> query-writer
"Check this SQL..." -> syntax-checker
"Explain this query..." -> query-explainer
"This query is slow..." -> optimizer or performance-tuning
"Why is this failing..." -> debugger
"I need a ranking..." -> window-functions
"Convert this to PostgreSQL..." -> dialect-translator
"Check for duplicate data..." -> data-quality
"Create a monthly report..." -> reporting
"Calculate running total..." -> window-functions or analytics-sql
```

## Supported Database Dialects

| Dialect | Version Support | Key Differences |
|---------|-----------------|-----------------|
| PostgreSQL | 12+ | Rich functions, JSONB, arrays, CTEs |
| MySQL | 8.0+ | AUTO_INCREMENT, backticks, LIMIT syntax |
| SQL Server | 2016+ | TOP, IDENTITY, T-SQL extensions |
| Oracle | 19c+ | ROWNUM, sequences, PL/SQL |
| SQLite | 3.35+ | Lightweight, limited types, file-based |

## Query Structure Reference

### SELECT Statement Components

```sql
SELECT [DISTINCT] columns
FROM table
[JOIN other_table ON condition]
[WHERE filter_condition]
[GROUP BY grouping_columns]
[HAVING aggregate_condition]
[ORDER BY sort_columns]
[LIMIT n OFFSET m]
```

### Common Clause Order

1. SELECT - What columns to return
2. FROM - Source table(s)
3. JOIN - Additional tables with relationships
4. WHERE - Row-level filtering (before grouping)
5. GROUP BY - Aggregate grouping
6. HAVING - Aggregate filtering (after grouping)
7. ORDER BY - Result sorting
8. LIMIT/OFFSET - Pagination

## Best Practices Summary

### Query Writing
- Use explicit column names, avoid SELECT *
- Alias tables and complex expressions
- Use parameterized queries to prevent SQL injection
- Format queries for readability

### Performance
- Index columns used in WHERE, JOIN, ORDER BY
- Avoid functions on indexed columns in WHERE
- Use EXISTS instead of IN for subqueries
- Limit result sets with appropriate filtering

### Maintainability
- Use CTEs for complex multi-step queries
- Add meaningful aliases
- Break complex logic into views or functions
- Document business logic in comments

## Error Handling Pattern

```sql
-- PostgreSQL
BEGIN;
    -- your queries here
    IF condition THEN
        RAISE EXCEPTION 'Error message';
    END IF;
COMMIT;

-- SQL Server
BEGIN TRY
    BEGIN TRANSACTION;
    -- your queries here
    COMMIT TRANSACTION;
END TRY
BEGIN CATCH
    ROLLBACK TRANSACTION;
    THROW;
END CATCH;
```

## Quick Reference Cards

### Aggregation Functions
| Function | Purpose |
|----------|---------|
| COUNT(*) | Total rows |
| COUNT(col) | Non-NULL values |
| SUM(col) | Total of values |
| AVG(col) | Average value |
| MIN(col) | Minimum value |
| MAX(col) | Maximum value |
| GROUP_CONCAT / STRING_AGG | Concatenate values |

### JOIN Types
| Type | Returns |
|------|---------|
| INNER JOIN | Matching rows only |
| LEFT JOIN | All left + matching right |
| RIGHT JOIN | All right + matching left |
| FULL OUTER JOIN | All rows from both |
| CROSS JOIN | Cartesian product |

### Common Operators
| Operator | Usage |
|----------|-------|
| = | Exact match |
| <> or != | Not equal |
| LIKE | Pattern match |
| IN | Value in list |
| BETWEEN | Range inclusive |
| IS NULL | NULL check |
| EXISTS | Subquery has results |

## Validation Checklist

Before outputting any SQL:

- [ ] Syntax is valid for target dialect
- [ ] Table and column names exist
- [ ] JOIN conditions are complete (no cartesian products)
- [ ] WHERE clause has appropriate filters
- [ ] GROUP BY includes all non-aggregated columns
- [ ] ORDER BY columns are in SELECT or valid
- [ ] Parameters are properly escaped/parameterized
- [ ] Query handles NULL values appropriately
