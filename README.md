# CI/CD Pipeline with GitHub Actions

[![Testing](https://github.com/nikola20145/VU-SEP-Assignment2/actions/workflows/testing.yml/badge.svg)](https://github.com/nikola20145/VU-SEP-Assignment2/actions/workflows/testing.yml)
[![PMD Static Analysis](https://github.com/nikola20145/VU-SEP-Assignment2/actions/workflows/static-analysis-1.yml/badge.svg)](https://github.com/nikola20145/VU-SEP-Assignment2/actions/workflows/static-analysis-1.yml)

A group assignment for the **Software Engineering Process (SEP)** course at Vrije Universiteit Amsterdam. We built a full CI/CD pipeline in **GitHub Actions** for a small Java project built with **Maven**. Every push is compiled and tested, the code is checked with two static analysis tools, and releases are created automatically.

The application is deliberately simple (a `Calculator.divide` method with JUnit 5 tests). The focus of the project is the automation around it and the team workflow: feature branches, issues, pull requests and code reviews.

## The pipeline

| Workflow | File | Trigger | What it does |
|---|---|---|---|
| **Testing** | [`testing.yml`](.github/workflows/testing.yml) | Push to any branch | Sets up JDK 11, builds with `mvn package` and runs the JUnit tests |
| **Static analysis 1 – PMD** | [`static-analysis-1.yml`](.github/workflows/static-analysis-1.yml) | Push to any branch | Runs PMD (`mvn pmd:pmd`) with the basic ruleset to catch code-quality issues early |
| **Static analysis 2 – Checkstyle** | [`static-analysis-2.yml`](.github/workflows/static-analysis-2.yml) | Pull request to any branch | Runs `mvn checkstyle:check` to enforce code style before merging |
| **Release** | [`release.yml`](.github/workflows/release.yml) | Push to `main` whose commit message contains `release` | Tags the commit `v<run number>` and pushes the tag, so GitHub publishes a release with source `.zip`/`.tar.gz` archives |

## My contribution

I designed and implemented the **PMD static analysis workflow** (`static-analysis-1.yml`). I chose PMD because it integrates directly with Maven, and I configured the pipeline to run it on every push. I also:

- Set up the README/report template and the team's GitHub conventions for commits, issues and pull requests
- Opened issues and pull requests for my workflow and reviewed my teammates' testing, Checkstyle and release workflows
- Helped coordinate the team and kept everyone on track with their tasks

The full assignment report, with each member's contributions, is in [`REPORT.md`](REPORT.md).

## Tech stack

Java 11 · Maven · JUnit 5 · GitHub Actions · PMD · Checkstyle

## Project structure

```
.github/workflows/   CI/CD workflow definitions
src/                 Calculator.java
tests/               CalculatorTest.java (JUnit 5)
workflow-tests/      Dummy files each member committed to trigger and test the workflows
pom.xml              Maven build with Surefire and PMD plugins
```

## Running locally

```bash
mvn test           # compile and run the tests
mvn pmd:pmd        # PMD static analysis
mvn checkstyle:check
```

## Team

[@nikola20145](https://github.com/nikola20145) (Nikola), [@YBushi](https://github.com/YBushi) (Tomáš), [@jayran-d](https://github.com/jayran-d) (Jayran), [@QS832](https://github.com/QS832) (Luis)
