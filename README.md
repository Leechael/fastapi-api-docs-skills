# FastAPI API Docs Skills

Agent skills for analyzing FastAPI routes and completing API documentation.

## Installation

```bash
npx skills add leechael/fastapi-api-docs-skills
```

## Skills

### api-docs

Analyze FastAPI route files and complete API documentation metadata. Follows the complete call stack including `Depends`, traces all possible errors, and generates comprehensive OpenAPI documentation elements.

**Usage:**

```
/api-docs @path/to/routes/file.py
```

**Batch mode:**

```
/api-docs @project/api/routes/           # All files in directory
/api-docs @file1.py @file2.py @file3.py  # Multiple specific files
```

**What it does:**

1. Discovers all route handlers (`@router.get`, `@router.post`, etc.)
2. Traces dependencies (`Depends(...)`) for auth requirements and errors
3. Analyzes handler body for database operations, external calls, and error propagation
4. Generates docstrings, OpenAPI metadata, and parameter documentation

## Writing Style

Documentation follows the [anti-slop](api-docs/references/anti-slop.md) guidelines:

- Summaries: 6 words max, imperative verb
- Descriptions: direct statements, no filler
- No "serves as", "in order to", or hedging language

## License

MIT
