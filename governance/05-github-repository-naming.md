# GitHub Repository Naming Conventions

## Version Information
| Version | Date | Description |
|---------|------|-------------|
| 1.0 | 2023-05-20 | Initial documentation |
| 1.1 | 2023-05-20 | Added links to role definitions and standardized terminology |

## Overview

Consistent repository naming is essential for discoverability, organization, and governance. This document outlines the standard naming conventions for repositories in our GitHub organization.

## Naming Structure

All repositories should follow this naming pattern:

```plaintext
[product-area]-[component]-[division]
```

This naming convention aligns with our [team naming conventions](./01-github-governance-roles.md#team-types) and repository access model defined in [04-github-repository-governance.md](./04-github-repository-governance.md).

Where:
- **product-area**: The functional product or service area
- **component**: The specific component or module
- **division**: The organizational [division](./01-github-governance-roles.md#division-team) (optional for organization-wide repositories)

## Examples by Category

### Shared Services

Repositories for shared services used across the organization:

```
infrastructure-monitoring
design-system-components
api-platform-core
authentication-service
analytics-dashboard
```

### Division-Specific Products

Repositories for products managed by specific [divisions](./01-github-governance-roles.md#division-team):

```
volunteer-portal-oslo
website-frontend-hordaland
event-management-oslo
donor-management-hk
training-platform-hordaland
```

### National Products

Repositories for national-level products:

```
crm-donor-management
finance-reporting
national-website-frontend
emergency-response-system
membership-management
```

## Component Naming Guidelines

These guidelines help ensure consistency across repositories and align with our [governance model](./04-github-repository-governance.md).

### Common Component Names

Use these standard component names when applicable to ensure consistent naming across projects:

| Component Name | Description |
|----------------|-------------|
| `api` | API implementation |
| `client` | Client library for accessing a service |
| `service` | Backend service |
| `frontend` | User interface implementation |
| `admin` | Administration interface |
| `docs` | Documentation |
| `core` | Core shared library |
| `utils` | Utility functions |
| `config` | Configuration files/templates |
| `infra` | Infrastructure as code |
| `cli` | Command-line interface tool |
| `sdk` | Software Development Kit |
| `mobile` | Mobile application |
| `worker` | Background worker service |
| `analytics` | Analytics component |
| `cms` | Content Management System |
| `gateway` | API Gateway or service gateway |
| `db` | Database schema, migrations, or tools |
| `monitoring` | Monitoring and alerting components |
| `auth` | Authentication/authorization components |

### Examples with Components

```
volunteer-portal-api-oslo
volunteer-portal-frontend-oslo
website-frontend-hordaland
website-cms-hordaland
api-platform-core
api-platform-client
```

## When to Skip Division Identifier

Omit the division identifier when:

1. The repository is used across the entire organization
2. The repository is part of the core infrastructure
3. The component is managed centrally, not by a specific division

Examples:
```
design-system-components
api-platform-core
infrastructure-monitoring
```

## Abbreviations and Naming Rules

1. **Use lowercase**: All repository names should be lowercase
2. **Use hyphens**: Separate words with hyphens, not underscores or camelCase
3. **Be descriptive but concise**: Keep names short but clear
4. **Avoid person names**: Don't name repositories after team members
5. **Avoid version numbers**: Don't include version numbers in repository names
6. **Align with team names**: Repository names should align with relevant [Project Team](./01-github-governance-roles.md#project-team) names
7. **Standard abbreviations**: Some acceptable abbreviations for common terms:

| Full Term | Abbreviation |
|-----------|--------------|
| Administration | admin |
| Application | app |
| Authentication | auth |
| Configuration | config |
| Documentation | docs |
| Infrastructure | infra |
| Management | mgmt |
| Statistics | stats |
| Utilities | utils |

## Repository Prefixes for Special Types

Some repositories serve special purposes and should use these prefixes:

| Prefix | Purpose | Example |
|--------|---------|---------|
| `template-` | Repository templates | `template-nodejs-api` |
| `poc-` | Proof of concept | `poc-blockchain-donations` |
| `archive-` | Archived projects | `archive-legacy-website` |

## Process for New Repository Names

1. **[Project Owner](./01-github-governance-roles.md#project-owner) proposes name**: Following the conventions in this document
2. **[Repository Admin](./01-github-governance-roles.md#repository-admin) reviews**: Ensures alignment with naming standards
3. **Repository is created**: Using the approved name

## Handling Legacy Repositories

For repositories created before these naming conventions:

1. Repositories will maintain their current names to avoid breaking existing references
2. New features should be created in new repositories with proper naming
3. Consider renaming critical repositories after careful planning

## Examples of Good vs. Bad Names

| ✅ Good Names | ❌ Bad Names | Why |
|--------------|-------------|-----|
| `volunteer-portal-api-oslo` | `oslo_volunteers_system` | Uses correct format with hyphens |
| `website-frontend-hordaland` | `HordalandWeb` | Lowercase with hyphens, not camelCase |
| `donor-management-hk` | `johns-donor-project` | No person names in repository names |
| `event-management-oslo` | `oslo-events-v2` | No version numbers in names |
| `api-platform-core` | `API_platform` | Consistent casing, hyphens not underscores |

## Additional Guidelines for Monorepos

For monorepo structures (multiple projects in a single repository):

1. Use the most general product area name
2. Add `-monorepo` suffix
3. Use internal directory structure to organize components

Example:
```
digital-services-monorepo
```

With internal structure:
```
/services/volunteer-portal
/services/event-management
/packages/shared-components
```

## Related Documents

For more information on related topics, please refer to:

- [01-github-governance-roles.md](./01-github-governance-roles.md) - Detailed information on GitHub roles and team types
- [04-github-repository-governance.md](./04-github-repository-governance.md) - Repository governance model and access control
- [03-github-provisioning.md](./03-github-provisioning.md) - User provisioning and team structure