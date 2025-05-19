# GitHub Repository Naming Conventions

## Overview

Consistent repository naming is essential for discoverability, organization, and governance. This document outlines the standard naming conventions for repositories in our GitHub organization.

## Naming Structure

All repositories should follow this naming pattern:

```
[product-area]-[component]-[division]
```

Where:
- **product-area**: The functional product or service area
- **component**: The specific component or module
- **division**: The organizational division (optional for organization-wide repositories)

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

Repositories for products managed by specific divisions:

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

### Common Component Names

Use these standard component names when applicable:

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
6. **Standard abbreviations**: Some acceptable abbreviations for common terms:

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

1. **Project Lead proposes name**: Following the conventions in this document
2. **Repository Admin reviews**: Ensures alignment with naming standards
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