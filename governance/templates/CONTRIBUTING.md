# Contributing to [Repository Name]

Thank you for your interest in contributing to this project! This document provides guidelines and instructions for contributing.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Development Process](#development-process)
- [Reporting Issues](#reporting-issues)
- [Pull Requests](#pull-requests)
- [Coding Standards](#coding-standards)
- [Testing](#testing)
- [Documentation](#documentation)
- [Review Process](#review-process)

## Code of Conduct

This project follows the Norwegian Red Cross code of conduct. By participating, you are expected to uphold this code.

## Getting Started

### Development Environment Setup

1. Fork the repository
2. Clone your fork: `git clone https://github.com/YOUR-USERNAME/[repository-name].git`
3. Add the original repository as upstream: `git remote add upstream https://github.com/norwegianredcross/[repository-name].git`
4. Set up your development environment:

```bash
# Install dependencies
npm install  # Or appropriate command for this project

# Set up environment variables
cp .env.example .env
# Edit .env as needed
```

## Development Process

### Branching Strategy

We follow a standard Git flow process:

- `main` - Production-ready code
- `develop` - Development branch for integration
- Feature branches - For new features or changes

### Branch Naming Convention

```
[type]/[short-description]
```

Where `[type]` is one of:
- `feature` - New feature
- `bugfix` - Bug fix
- `hotfix` - Critical fix for production
- `improvement` - Enhancement to existing feature
- `refactor` - Code restructuring
- `docs` - Documentation changes

Example: `feature/user-authentication`

## Reporting Issues

Please use GitHub Issues to report bugs or suggest improvements:

1. Check if the issue already exists
2. Use the provided issue template
3. Include:
   - Clear description of the problem
   - Steps to reproduce
   - Expected vs. actual behavior
   - Screenshots if applicable
   - Environment details (browser, OS, versions)

## Pull Requests

1. Create a new branch from `develop` with the appropriate naming convention
2. Make your changes in small, logical commits
3. Follow the [coding standards](#coding-standards)
4. Add or update tests as necessary
5. Update documentation if needed
6. Submit your PR against the `develop` branch
7. Fill out the PR template completely

### Commit Message Guidelines

We follow conventional commits:

```
[type]: [subject]

[optional body]

[optional footer]
```

Where `[type]` is one of:
- `feat` - New feature
- `fix` - Bug fix
- `docs` - Documentation changes
- `style` - Formatting, missing semicolons, etc.
- `refactor` - Code changes that neither fix bugs nor add features
- `perf` - Performance improvements
- `test` - Adding or fixing tests
- `chore` - Build process or tooling changes

Example: `feat: add user authentication system`

## Coding Standards

This project follows [specific coding standards]. Some key points:

- [Indentation style]
- [Naming conventions]
- [File structure]
- [Code organization]

We use linters to enforce these standards. To check your code:

```bash
npm run lint
```

To automatically fix issues when possible:

```bash
npm run lint:fix
```

## Testing

All pull requests should maintain or increase test coverage. To run tests:

```bash
npm test
```

### Types of Tests

- **Unit Tests**: Test individual components in isolation
- **Integration Tests**: Test interactions between components
- **End-to-End Tests**: Test the complete application flow

## Documentation

- Update README.md if you add or change features
- Keep code comments up-to-date
- Document public APIs with JSDoc or similar
- Update any relevant documentation in the `/docs` directory

## Review Process

1. All PRs require at least one review from a maintainer
2. Automated checks must pass:
   - Unit tests
   - Linting
   - Status checks
3. Address all feedback from reviewers
4. PRs will be merged by maintainers once approved

Thank you for contributing!