# GitHub Documentation Standards

## Version Information
| Version | Date | Description |
|---------|------|-------------|
| 1.0 | 2025-05-20 | Initial documentation |
| 1.1 | 2025-05-20 | Added links to role definitions and standardized terminology |
| 1.2 | 2025-05-20 | Extracted markdown and mermaid standards to example files |

## Overview

This document outlines the documentation standards for all repositories in the Norwegian Red Cross GitHub organization, managed by [Repository Admins](./01-github-governance-roles.md#repository-admin) with support from [Project Owners](./01-github-governance-roles.md#project-owner) and [Team Maintainers](./01-github-governance-roles.md#team-maintainer). Consistent documentation ensures code maintainability, promotes collaboration, and facilitates onboarding of new team members.

## Required Documentation Files

Every repository in the Norwegian Red Cross GitHub organization must contain the following documentation files:

### README.md

All repositories must have a README.md file in the root directory that includes:

- **Project Name and Description**
  - Clear description of the repository's purpose
  - Business context and relationship to other systems
  - Status indicator (active, maintenance, deprecated)

- **Getting Started Guide**
  - Prerequisites and dependencies
  - Installation instructions
  - Basic usage examples
  - Environment setup details

- **Architecture Overview**
  - High-level architecture diagram (if applicable)
  - Key components and interactions
  - External system dependencies

- **Contributing Information**
  - Link to CONTRIBUTING.md
  - Quick reference for development workflow

- **License Information**
  - Clear statement of licensing terms
  - Copyright notice

- **Contact Information**
  - Team/Department responsible
  - How to report issues or request features

Use the [README.md template](./templates/README.md) to create your README.md file.

### CONTRIBUTING.md

All repositories must have a CONTRIBUTING.md file that includes:

- **Contribution Process**
  - How to report bugs
  - How to suggest enhancements
  - How to submit changes

- **Development Environment Setup**
  - Step-by-step setup instructions
  - Required tools and versions
  - Local testing procedures

- **Coding Standards**
  - Code style and formatting rules
  - Language-specific conventions
  - Documentation requirements for code

- **Testing Requirements**
  - Test coverage expectations
  - Types of tests required
  - How to run tests locally

- **Pull Request Process**
  - Branch naming conventions
  - Commit message standards
  - PR template usage instructions

- **Review Process**
  - What reviewers look for
  - Expected response times
  - How feedback should be addressed

Use the [CONTRIBUTING.md template](./templates/CONTRIBUTING.md) to create your CONTRIBUTING.md file.

### CODEOWNERS

All repositories must have a CODEOWNERS file that:

- Designates owners for specific directories or file types
- Includes at least one [Repository Admin](./01-github-governance-roles.md#repository-admin) or [Team Maintainer](./01-github-governance-roles.md#team-maintainer)
- Maps to the actual project team structure

Use the [CODEOWNERS template](./templates/CODEOWNERS) to create your CODEOWNERS file.

### LICENSE

All repositories must have an appropriate LICENSE file:

- Internal repositories: Proprietary license template
- Public repositories: Approved open source license (MIT recommended)

Use the [LICENSE-opensource.md template](./templates/LICENSE-opensource.md) for open source repositories.
Use the [LICENSE-internal.md template](./templates/LICENSE-internal.md) for internal repositories.

## Repository Setup Documentation Checklist

[Repository Admins](./01-github-governance-roles.md#repository-admin) should verify the following documentation items during repository creation:

| Documentation Item | Required | Included | Notes |
|-------------------|----------|----------|-------|
| README.md | ✅ | | Use [README.md template](./templates/README.md) |
| CONTRIBUTING.md | ✅ | | Use [CONTRIBUTING.md template](./templates/CONTRIBUTING.md) |
| CODEOWNERS | ✅ | | Use [CODEOWNERS template](./templates/CODEOWNERS) |
| LICENSE | ✅ | | Use [LICENSE-opensource.md](./templates/LICENSE-opensource.md) or [LICENSE-internal.md](./templates/LICENSE-internal.md) |
| Issue templates | Recommended | | Use [ISSUE_TEMPLATE](./templates/ISSUE_TEMPLATE) |
| Pull request template | Recommended | | Use [PULL_REQUEST_TEMPLATE](./templates/PULL_REQUEST_TEMPLATE) |
| SECURITY.md | Recommended | | Use [SECURITY.md template](./templates/SECURITY.md) |

## Documentation Standards Resources

We have created dedicated example files to demonstrate the recommended documentation standards:

- [Markdown Standards and Examples](./examples/markdown.md) - Comprehensive guide to Markdown formatting
- [Mermaid Diagram Examples](./examples/mermaid.md) - Examples of well-formatted diagrams

Refer to these examples when creating documentation for your repositories.

## Documentation Roles and Responsibilities

The responsibility for maintaining documentation is shared across different roles:

1. **[Repository Admins](./01-github-governance-roles.md#repository-admin)**:
   - Set up initial required documentation during repository creation
   - Verify documentation compliance with these standards
   - Enforce documentation requirements through branch protection rules
   - Conduct periodic audits of documentation quality

2. **[Project Owners](./01-github-governance-roles.md#project-owner)**:
   - Responsible for the overall quality and accuracy of documentation
   - Ensure documentation is kept up-to-date with project changes
   - Review and approve significant documentation updates
   - Ensure README.md accurately reflects the project's current status

3. **[Team Maintainers](./01-github-governance-roles.md#team-maintainer)**:
   - Manage CODEOWNERS file and ensure it reflects team structure
   - Review documentation contributions from team members
   - Ensure code changes include appropriate documentation updates
   - Help onboard new contributors to documentation practices

4. **[Team Members](./01-github-governance-roles.md#team-member)**:
   - Update documentation when making code changes
   - Follow the established documentation standards
   - Report outdated or incorrect documentation
   - Contribute to documentation improvements

## Documentation Maintenance

- README.md should be updated with any significant changes by [Project Owners](./01-github-governance-roles.md#project-owner)
- CODEOWNERS should be reviewed quarterly by [Project Owners](./01-github-governance-roles.md#project-owner) and [Team Maintainers](./01-github-governance-roles.md#team-maintainer)
- All documentation should be reviewed annually by the responsible [Project Owner](./01-github-governance-roles.md#project-owner)
- Outdated documentation should be updated or clearly marked as deprecated
- [Repository Admins](./01-github-governance-roles.md#repository-admin) should verify documentation compliance during periodic repository audits

## Related Documents

For more information on related topics, please refer to:

- [01-github-governance-roles.md](./01-github-governance-roles.md) - Roles and responsibilities definitions
- [04-github-repository-governance.md](./04-github-repository-governance.md) - Repository governance structure
- [05-github-repository-naming.md](./05-github-repository-naming.md) - Repository naming conventions
- [08-github-security-standards.md](./08-github-security-standards.md) - Security documentation requirements
- [Examples](./examples/) - Documentation examples including Markdown and Mermaid
- [Templates](./templates/) - Repository templates including README.md and CONTRIBUTING.md