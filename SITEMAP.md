# Skills Prompt Hub - Sitemap

Complete index of all AI prompting skills and resources.

## Quick Navigation

| Category | Skills Count | Status |
|----------|-------------|--------|
| [SQL](#sql-skills) | 11 sub-skills | Complete |
| [Excel/XLSX](#excelxlsx-skills) | 3 sub-skills | Complete |

---

## SQL Skills

Comprehensive SQL skill suite for query writing, optimization, debugging, and cross-dialect operations.

### Main Entry Point
- [sql/SKILL.md](sql/SKILL.md) - SQL skills router and overview

### Sub-Skills

| Skill | Description | Files |
|-------|-------------|-------|
| **Query Writer** | Write SQL queries from requirements | [SKILL.md](sql/query-writer/SKILL.md) | [examples.md](sql/query-writer/examples.md) |
| **Syntax Checker** | Validate SQL syntax and structure | [SKILL.md](sql/syntax-checker/SKILL.md) | [examples.md](sql/syntax-checker/examples.md) |
| **Query Explainer** | Explain complex queries in plain language | [SKILL.md](sql/query-explainer/SKILL.md) | [examples.md](sql/query-explainer/examples.md) |
| **Optimizer** | Improve query performance | [SKILL.md](sql/optimizer/SKILL.md) | [examples.md](sql/optimizer/examples.md) |
| **Debugger** | Debug failing or incorrect queries | [SKILL.md](sql/debugger/SKILL.md) | [examples.md](sql/debugger/examples.md) |
| **Window Functions** | Advanced window/analytic functions | [SKILL.md](sql/window-functions/SKILL.md) | [examples.md](sql/window-functions/examples.md) |
| **Performance Tuning** | Database-level performance optimization | [SKILL.md](sql/performance-tuning/SKILL.md) | [examples.md](sql/performance-tuning/examples.md) |
| **Analytics SQL** | Analytical and aggregation queries | [SKILL.md](sql/analytics-sql/SKILL.md) | [examples.md](sql/analytics-sql/examples.md) |
| **Dialect Translator** | Convert between SQL dialects | [SKILL.md](sql/dialect-translator/SKILL.md) | [examples.md](sql/dialect-translator/examples.md) |
| **Data Quality** | Data validation and integrity | [SKILL.md](sql/data-quality/SKILL.md) | [examples.md](sql/data-quality/examples.md) |
| **Reporting** | Business reporting queries | [SKILL.md](sql/reporting/SKILL.md) | [examples.md](sql/reporting/examples.md) |

### SQL Skills Tree

```
sql/
├── SKILL.md                     # Main router
├── query-writer/
│   ├── SKILL.md                 # SELECT, INSERT, UPDATE, DELETE, JOINs, CTEs
│   └── examples.md              # E-commerce, user management, analytics
├── syntax-checker/
│   ├── SKILL.md                 # Syntax rules, dialect validation
│   └── examples.md              # Common errors and corrections
├── query-explainer/
│   ├── SKILL.md                 # Execution order, breakdown templates
│   └── examples.md              # Complex query explanations
├── optimizer/
│   ├── SKILL.md                 # Execution plans, performance issues
│   └── examples.md              # Before/after optimizations
├── debugger/
│   ├── SKILL.md                 # Error categories, debugging techniques
│   └── examples.md              # Real-world debugging scenarios
├── window-functions/
│   ├── SKILL.md                 # ROW_NUMBER, RANK, LAG/LEAD, frames
│   └── examples.md              # Advanced window function patterns
├── performance-tuning/
│   ├── SKILL.md                 # Indexing, profiling, schema design
│   └── examples.md              # Performance case studies
├── analytics-sql/
│   ├── SKILL.md                 # ROLLUP, CUBE, GROUPING SETS, stats
│   └── examples.md              # Revenue, customer, product analytics
├── dialect-translator/
│   ├── SKILL.md                 # PostgreSQL, MySQL, SQL Server, Oracle
│   └── examples.md              # Complete translation examples
├── data-quality/
│   ├── SKILL.md                 # Profiling, duplicates, validation
│   └── examples.md              # Data quality audit scenarios
└── reporting/
    ├── SKILL.md                 # KPIs, dashboards, business reports
    └── examples.md              # Executive, sales, financial reports
```

---

## Excel/XLSX Skills

Excel formula writing and spreadsheet manipulation skills.

### Sub-Skills

| Skill | Description | Files |
|-------|-------------|-------|
| **Formulas** | Standard Excel formulas | [SKILL.md](Xlsx/formulas/SKILL.md) | [Formulas.md](Xlsx/formulas/Formulas.md) | [examples.md](Xlsx/formulas/examples.md) |
| **Advanced Formulas** | LAMBDA, LET, dynamic arrays | [SKILL.md](Xlsx/advanced-formulas/SKILL.md) | [lambda-functions.md](Xlsx/advanced-formulas/lambda-functions.md) |
| **Fundamentals** | Cells, ranges, formatting | [SKILL.md](Xlsx/fundamentals/SKILL.md) | [cells-and-ranges.md](Xlsx/fundamentals/cells-and-ranges.md) |

### XLSX Skills Tree

```
Xlsx/
├── formulas/
│   ├── SKILL.md                 # Formula syntax, validation
│   ├── Formulas.md              # Complete syntax rules
│   ├── examples.md              # Production-ready examples
│   └── functions-reference.md   # Function documentation
├── advanced-formulas/
│   ├── SKILL.md                 # LAMBDA, LET, modern functions
│   ├── lambda-functions.md      # Custom function creation
│   ├── array-manipulation.md    # HSTACK, VSTACK, TAKE, DROP
│   ├── text-parsing.md          # TEXTSPLIT, regex functions
│   └── advanced-patterns.md     # Complex formula patterns
└── fundamentals/
    ├── SKILL.md                 # Excel basics
    ├── cells-and-ranges.md      # Cell references, named ranges
    ├── formatting-and-styles.md # Number formats, conditional
    ├── sheets-and-views.md      # Workbook management
    └── sorting-filtering-tables.md # Data organization
```

---

## Planned Skills (Coming Soon)

| Category | Sub-Skills |
|----------|------------|
| Database | Schema design, migrations, ORMs |
| Data Cleaning | Pandas, data validation, ETL |
| Data Analysis | Statistics, visualization, insights |
| DevOps | CI/CD, Docker, Kubernetes |
| Backend (FastAPI) | Auth, API design, async programming |
| Frontend (React) | Components, state, hooks |
| Code Review | Best practices, security, performance |
| RAG | Chunking, embeddings, retrieval |
| LLM Fine-tuning | Dataset prep, training, evaluation |

---

## File Statistics

| Metric | Count |
|--------|-------|
| Total Skills | 14 |
| Total Files | 40+ |
| SQL Files | 24 |
| XLSX Files | 14 |

---

## How to Use

1. Navigate to the relevant skill category
2. Read the main `SKILL.md` for overview and trigger conditions
3. Check `examples.md` for production-ready code
4. Use sub-files for detailed reference

## Contributing

To add a new skill:
1. Create a folder under the appropriate category
2. Add `SKILL.md` with trigger conditions and instructions
3. Add `examples.md` with practical examples
4. Update this sitemap
