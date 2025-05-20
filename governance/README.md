# GitHub Governance Framework

## Introduction

This repository contains the official governance documentation for the Norwegian Red Cross GitHub organization. These documents establish a comprehensive framework that defines how GitHub is managed, secured, and used within our organization.

The goal of this governance framework is to:

- Provide clear roles and responsibilities for GitHub management
- Establish consistent naming and organization standards
- Define secure workflows and approval processes
- Enable effective collaboration across teams and with external partners
- Ensure proper documentation of all repositories

## How to Use This Documentation

### For Different Audiences

#### GitHub Administrators
Start with the roles document (01) to understand your responsibilities, then review all documents with special attention to repository governance (04), security standards (08), and ServiceNow integration (06).

#### Project Owners
Focus on repository governance (04), repository naming (05), security standards (08), documentation standards (09), and platform selection (07) to understand your responsibilities and requirements.

#### Team Maintainers
Review roles (01), user provisioning (03), and repository governance (04) to understand how to manage teams and access effectively.

#### Developers
Familiarize yourself with documentation standards (09), security standards (08), and repository naming (05) to ensure your contributions follow organizational practices.

### Documents by Topic

#### Organization and Roles
- [01-github-governance-roles.md](./01-github-governance-roles.md) - All roles and responsibilities
- [02-github-internal-external.md](./02-github-internal-external.md) - Internal vs external user management

#### Access and Provisioning
- [03-github-provisioning.md](./03-github-provisioning.md) - How users get access to GitHub
- [06-github-servicenow.md](./06-github-servicenow.md) - Request and approval workflows

#### Repository Management
- [04-github-repository-governance.md](./04-github-repository-governance.md) - Repository administration and permissions
- [05-github-repository-naming.md](./05-github-repository-naming.md) - Naming convention requirements

#### Security and Standards
- [07-platform-selection-guidelines.md](./07-platform-selection-guidelines.md) - GitHub vs Azure DevOps decisions
- [08-github-security-standards.md](./08-github-security-standards.md) - Security requirements
- [09-github-documentation-standards.md](./09-github-documentation-standards.md) - Documentation requirements
- [10-github-best-practices.md](./10-github-best-practices.md) - Analysis of industry best practices alignment

### Quick Reference Diagrams

For visual learners, each document contains diagrams that illustrate key concepts. You can find all diagram examples in the [examples/mermaid.md](./examples/mermaid.md) file.

## Key Concepts

### Team Structure

The Norwegian Red Cross uses a hierarchical team structure in GitHub:

1. **[Division Teams](./01-github-governance-roles.md#division-team)** (Level 1) - Provide read access across divisions
2. **[Department Teams](./01-github-governance-roles.md#department-team)** (Level 2) - Provide read access to department members
3. **[Role-based Teams](./01-github-governance-roles.md#role-based-team)** - Provide read access based on job functions
4. **[Project Teams](./01-github-governance-roles.md#project-team)** - Provide write access for active contributors

### Governance Roles

The governance structure relies on clearly defined roles:

- **[Organization Owners](./01-github-governance-roles.md#organization-owner)** - Highest level of permissions
- **[Repository Admins](./01-github-governance-roles.md#repository-admin)** - Manage repository creation and settings
- **[Team Admins](./01-github-governance-roles.md#team-admin)** - Manage team structures
- **[Project Owners](./01-github-governance-roles.md#project-owner)** - Responsible for specific repositories
- **[Team Maintainers](./01-github-governance-roles.md#team-maintainer)** - Manage team memberships

### Request Workflows

All GitHub requests go through ServiceNow with standardized workflows:

1. Repository creation requests
2. GitHub access requests
3. Repository conversion requests

## Document Summaries

### [01-github-governance-roles.md](./01-github-governance-roles.md)
**Title:** GitHub Governance Roles

Defines all roles involved in GitHub governance, with clear responsibilities and permission levels for each role. Includes role relationship diagrams, assignment matrices, and team types with their purposes and membership criteria.

### [02-github-internal-external.md](./02-github-internal-external.md)
**Title:** Internal and External Users in GitHub

Explains the differences between internal employees/consultants and external collaborators, including access models, authentication methods, and best practices for collaboration with external partners.

### [03-github-provisioning.md](./03-github-provisioning.md)
**Title:** GitHub User Provisioning

Details the automated user provisioning flow from HR systems through Okta to GitHub, including team assignment based on organizational structure, lifecycle management, and special case handling.

### [04-github-repository-governance.md](./04-github-repository-governance.md)
**Title:** Repository Governance in GitHub

Establishes the repository administration model, access control based on organizational structure, and approval flows for repository creation and management.

### [05-github-repository-naming.md](./05-github-repository-naming.md)
**Title:** GitHub Repository Naming Conventions

Provides standardized naming patterns for repositories with examples, component naming guidelines, and special cases for different repository types.

### [06-github-servicenow.md](./06-github-servicenow.md)
**Title:** GitHub ServiceNow Integration

Documents how ServiceNow serves as the self-service portal for all GitHub-related requests, with detailed workflows for repository creation, access requests, and repository conversions.

### [07-platform-selection-guidelines.md](./07-platform-selection-guidelines.md)
**Title:** Platform Selection Guidelines

Guides decision-making between GitHub and Azure DevOps, with criteria for when to use each platform and requirements for making repositories public.

### [08-github-security-standards.md](./08-github-security-standards.md)
**Title:** GitHub Security Standards

Establishes security requirements for all repositories, including branch protection, secret scanning, dependency management, and security incident response procedures.

### [09-github-documentation-standards.md](./09-github-documentation-standards.md)
**Title:** GitHub Documentation Standards

Sets requirements for repository documentation, including README.md, CONTRIBUTING.md, and CODEOWNERS files, with templates and formatting standards.

### [10-github-best-practices.md](./10-github-best-practices.md)
**Title:** GitHub Best Practices Analysis

Analyzes how our governance framework aligns with industry best practices, highlighting areas of excellence and potential enhancements to our GitHub management approach.

## Supporting Resources

### Templates

The [templates/](./templates/) directory contains standardized templates for:
- [README.md](./templates/README.md) - Repository readme file
- [CONTRIBUTING.md](./templates/CONTRIBUTING.md) - Contribution guidelines
- [CODEOWNERS](./templates/CODEOWNERS) - Code ownership definition
- [LICENSE files](./templates/LICENSE-internal.md) - Internal and open source license options
- [SECURITY.md](./templates/SECURITY.md) - Security policy and vulnerability reporting
- Issue and pull request templates

### Examples

The [examples/](./examples/) directory contains:
- [Markdown formatting guidelines](./examples/markdown.md) - How to write consistent documentation
- [Mermaid diagram examples](./examples/mermaid.md) - How to create clear diagrams

## Governance Maintenance

This governance framework is maintained by the [Repository Admin](./01-github-governance-roles.md#repository-admin) team with oversight from [Organization Owners](./01-github-governance-roles.md#organization-owner). For questions, suggestions, or to report issues with the governance documentation, please contact them directly.

## Version History

| Version | Date | Description |
|---------|------|-------------|
| 1.0 | 2023-05-20 | Initial documentation |
| 2.0 | 2023-05-20 | Restructured for better organization and consistency |
| 2.1 | 2023-05-20 | Added platform selection guidelines document |
| 2.2 | 2023-05-20 | Added security standards document |
| 2.3 | 2023-05-20 | Added documentation standards and section-specific role links |
| 2.4 | 2023-05-20 | Consolidated External User into Outside Collaborator for clarity |
| 2.5 | 2023-05-20 | Added team types definitions with direct links to all roles |
| 3.0 | 2023-05-20 | Restructured README with clearer guidance and audience-specific sections |
| 3.1 | 2023-05-20 | Added GitHub Best Practices Analysis document |