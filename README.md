# CI/CD and SRE Pipeline Lab

An educational Python project that demonstrates a production-style CI/CD workflow with GitHub Actions. The pipeline includes code quality checks, tests, security scanning, simulated image publishing and deployment, smoke and performance checks, SLO evaluation, and rollback handling.

## Pipeline overview

The workflow in `.github/workflows/ci-cd.yml` runs on pushes to `main` and `develop`, and on pull requests targeting `main`. Its stages cover:

1. Formatting, linting, and unit tests.
2. Dependency and static security checks.
3. A simulated container build and deployment flow.
4. Smoke, performance, and SLO checks.
5. Rollback handling after a failed deployment.

Deployment and image-publishing steps are simulations. This repository does not configure a real registry or production cluster.

## Repository layout

- `app/`: Python application, requirements, and unit tests.
- `scripts/`: security evaluation, smoke and performance checks, SLO checks, and rollback example.
- `.github/workflows/ci-cd.yml`: CI/CD pipeline definition.

The workflow uses Python 3.11. Review the workflow before adapting it to real infrastructure, and configure credentials through GitHub Actions secrets rather than committing them.
