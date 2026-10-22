# {{PROJECT_NAME}} — Applications

This directory contains the applications for **{{PROJECT_NAME}}**.

## Structure

Each subdirectory represents a standalone Python application with its own
dependencies managed as a uv workspace member:

```text
apps/
├── {{APP_NAME}}/
│   ├── README.md          # Application-specific documentation
│   ├── pyproject.toml     # uv project configuration
│   ├── src/
│   │   └── {{APP_NAME}}/ # Application source code
│   ├── tests/             # Application tests
│   └── Dockerfile         # Container definition (if applicable)
└── ...
```

## Conventions

* Each application lives in its own subdirectory with an independent
  `pyproject.toml`
* Every application must have a `README.md` explaining its purpose, setup,
  and usage
* Use [uv](../meta/adr/ADR-015-use_uv.md) for dependency management
* Use [Ruff](../meta/adr/ADR-005-use_ruff.md) for linting and formatting
* Use [pytest](../meta/adr/ADR-004-use_pytest.md) for testing
* Follow the [Development Philosophy](../meta/DEVELOPMENT_PHILOSOPHY.md) for
  code quality standards
* Include tests alongside the application code in a `tests/` directory
