# GitHub Governance Documentation

This directory contains governance documentation for managing the Norwegian Red Cross GitHub organization. The documents here define processes, roles, naming conventions, and access models to ensure secure, consistent, and auditable management of repositories and users.

## Reading Order

For best understanding, please read the documents in the following order:

1. **Roles and Responsibilities** - [01-github-governance-roles.md](./01-github-governance-roles.md)
2. **User Types** - [02-github-internal-external.md](./02-github-internal-external.md)
3. **User Provisioning** - [03-github-provisioning.md](./03-github-provisioning.md)
4. **Repository Governance** - [04-github-repository-governance.md](./04-github-repository-governance.md)
5. **Repository Naming** - [05-github-repository-naming.md](./05-github-repository-naming.md)
6. **ServiceNow Integration** - [06-github-servicenow.md](./06-github-servicenow.md)
7. **Platform Selection** - [07-platform-selection-guidelines.md](./07-platform-selection-guidelines.md)
8. **Security Standards** - [08-github-security-standards.md](./08-github-security-standards.md)
9. **Documentation Standards** - [09-github-documentation-standards.md](./09-github-documentation-standards.md)


## Glossary of Terms

| Term | Definition | Primary Document |
|------|------------|------------------|
| [Organization Owner](./01-github-governance-roles.md#organization-owner) | Individual with highest level of permissions for GitHub organization | [01-github-governance-roles.md](./01-github-governance-roles.md) |
| [Repository Admin](./01-github-governance-roles.md#repository-admin) | Trusted individual responsible for repository governance | [01-github-governance-roles.md](./01-github-governance-roles.md) |
| [Team Admin](./01-github-governance-roles.md#team-admin) | Individual responsible for managing GitHub team structures | [01-github-governance-roles.md](./01-github-governance-roles.md) |
| [Project Owner](./01-github-governance-roles.md#project-owner) | Person who owns and is responsible for a repository or project | [01-github-governance-roles.md](./01-github-governance-roles.md) |
| [Team Maintainer](./01-github-governance-roles.md#team-maintainer) | Person who can manage a team's membership and settings | [01-github-governance-roles.md](./01-github-governance-roles.md) |
| [Team Member](./01-github-governance-roles.md#team-member) | Regular contributor to a repository or project | [01-github-governance-roles.md](./01-github-governance-roles.md) |
| [Outside Collaborator](./01-github-governance-roles.md#outside-collaborator) | External contributor (non-redcross.no) with repository-specific access | [01-github-governance-roles.md](./01-github-governance-roles.md) |
| [Financial Approver](./01-github-governance-roles.md#financial-approver-cost-center-manager) | Manager responsible for approving financial aspects | [01-github-governance-roles.md](./01-github-governance-roles.md) |
| [Internal User](./01-github-governance-roles.md#internal-user) | Employee or consultant with a redcross.no account | [01-github-governance-roles.md](./01-github-governance-roles.md) |
| [Division Team](./01-github-governance-roles.md#division-team) | Level 1 team providing Read access to division members | [01-github-governance-roles.md](./01-github-governance-roles.md) |
| [Department Team](./01-github-governance-roles.md#department-team) | Level 2 team providing Read access to department members | [01-github-governance-roles.md](./01-github-governance-roles.md) |
| [Project Team](./01-github-governance-roles.md#project-team) | Team providing Write/Maintain access to repository contributors | [01-github-governance-roles.md](./01-github-governance-roles.md) |

## Document Summaries

### [01-github-governance-roles.md](./01-github-governance-roles.md)
**Title:** GitHub Governance Roles

Defines all roles involved in GitHub governance, including Organization Owner, Repository Admin, Team Admin, Project Owner, Team Maintainer, Team Member, Outside Collaborator, and Financial Approver. It explains responsibilities, permission levels, and the assignment matrix for each role.

### [02-github-internal-external.md](./02-github-internal-external.md)
**Title:** Internal and External Users in GitHub

Describes the distinction between internal users (employees/consultants) and Outside Collaborators (external contributors), their access models, team structures, and collaboration patterns. Details security, governance, and best practices for mixed teams.

### [03-github-provisioning.md](./03-github-provisioning.md)
**Title:** GitHub User Provisioning

Explains the automated provisioning process for internal users via HR systems and Okta, including team assignment, lifecycle management, and SCIM integration. Also covers manual processes for onboarding Outside Collaborators and handling special cases.

### [04-github-repository-governance.md](./04-github-repository-governance.md)
**Title:** Repository Governance in GitHub

Outlines the structure for repository administration, access assignment based on a 2-level organizational hierarchy, and the process for repository creation and team assignment. Includes best practices for team permissions and cross-divisional collaboration.

### [05-github-repository-naming.md](./05-github-repository-naming.md)
**Title:** GitHub Repository Naming Conventions

Specifies the standard naming conventions for repositories, including required patterns, component names, abbreviations, and special prefixes. Provides examples and guidelines for both new and legacy repositories, as well as monorepo structures.

### [06-github-servicenow.md](./06-github-servicenow.md)
**Title:** GitHub ServiceNow Integration

Describes how ServiceNow is used as the single point of entry for all GitHub repository and access requests. It details the request and approval workflows for both repository creation and user access, including form fields, approval steps, and integration with organizational roles and HR systems.

### [07-platform-selection-guidelines.md](./07-platform-selection-guidelines.md)
**Title:** Platform Selection Guidelines

Provides guidance on when to use GitHub versus Azure DevOps for different project types and defines criteria for making repositories public. Includes decision frameworks, approval processes, and migration considerations to ensure consistent platform selection across the organization.

### [08-github-security-standards.md](./08-github-security-standards.md)
**Title:** GitHub Security Standards

Defines security requirements and best practices for GitHub usage, including branch protection rules, secret management, dependency scanning, and security incident response procedures. Ensures consistent security controls across all repositories and user types.

### [09-github-documentation-standards.md](./09-github-documentation-standards.md)
**Title:** GitHub Documentation Standards

Outlines the required documentation files and standards for all repositories, including README.md, CONTRIBUTING.md, CODEOWNERS, and LICENSE files. Provides templates, formatting guidelines, and best practices for maintaining clear and consistent documentation across the organization.

---

For questions or suggestions regarding governance, please contact the [Repository Admin](./01-github-governance-roles.md#repository-admin) team or [Organization Owners](./01-github-governance-roles.md#organization-owner) as defined in the [GitHub Governance Roles](./01-github-governance-roles.md) document.

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