# Internal and External Users in GitHub

## Overview

Norwegian Red Cross's GitHub organization accommodates two distinct user types to balance security and collaboration:

1. **Internal Users**: Employees and consultants with redcross.no accounts
2. **External Users**: Pro-bono contributors, volunteers, and partners

This document outlines how these user types access repositories and collaborate within our GitHub organization.

```mermaid
flowchart TD
    classDef internal fill:#e6f7ff,stroke:#1890ff,stroke-width:1px
    classDef external fill:#fff7e6,stroke:#fa8c16,stroke-width:1px
    
    A[Norwegian Red Cross<br>GitHub Organization]
    
    B[Internal Users]
    C[External Users]
    
    D[Organization Members<br>via SSO]
    E[Outside Collaborators]
    
    A --- B
    A --- C
    
    B --- D
    C --- E
    
    D --- A
    E --- A
    
    class B,D internal
    class C,E external
```

**Figure 1: User Types in GitHub**

## Access Model Overview

Our access model follows these principles:

1. **Organizational Structure Teams**: Provide Read-only access for visibility
   - Based on our 2-level hierarchy (divisions and departments)
   - Automatically maintained through HR/Okta synchronization
   - Ensures everyone can see relevant repositories

2. **Project Teams**: Provide Write/Maintain access for contributors
   - Created for specific repositories or projects
   - Managed by Repository Admins and Team Maintainers
   - Include people actively working on the project

## 2-Level Organizational Hierarchy

Our organizational structure in GitHub mirrors our 2-level hierarchy:

```mermaid
flowchart TD
    classDef division fill:#d4380d,stroke:#ff4d4f,stroke-width:2px,color:#ffffff
    classDef department fill:#389e0d,stroke:#52c41a,stroke-width:2px,color:#ffffff
    
    D1[Hovedkontor]
    D1 --> DEPT1[HK IT Department]
    D1 --> DEPT2[HK Inntekt Department]
    
    D2[Oslo Røde Kors]
    D2 --> DEPT3[Oslo IT Department]
    
    D3[Hordaland Røde Kors]
    D3 --> DEPT4[Hordaland IT Department]
    
    class D1,D2,D3 division
    class DEPT1,DEPT2,DEPT3,DEPT4 department
```

**Figure 2: Organizational Hierarchy Structure**

## Internal Users

### Characteristics

Internal users are:
- Employees and consultants of Norwegian Red Cross
- Have redcross.no email accounts
- Authenticate through Single Sign-On (SSO) with Okta
- Full members of the GitHub organization

### Access Model

Internal users access GitHub through:
- Single Sign-On (SSO) integration with Okta
- Authentication using their redcross.no credentials
- Automatic team assignments based on organizational structure
- Read access to repositories within their division or department
- Write/Maintain access only through project team membership

### Team Structure for Internal Users

Internal users are assigned to teams following our 2-level hierarchy:

1. **Division Level (Level 1)**
   - Users are assigned to their division team
   - Examples: "Hovedkontor Team", "Oslo Røde Kors Team"
   - Provides Read access to division-wide repositories

2. **Department Level (Level 2)**
   - Users are assigned to their department team
   - Examples: "HK IT Department Team", "Oslo IT Department Team" 
   - Provides Read access to department-specific repositories

3. **Project Teams (for contribution access)**
   - Users are manually assigned to project teams
   - Provides Write/Maintain access to specific repositories
   - Can include members from any division or department

### Participation in Development

Internal users can:
- View repositories in their division or department (Read access)
- Contribute to repositories by joining specific project teams (Write/Maintain access)
- Create repositories (if they are Repository Admins)
- Manage projects and repositories according to their assigned roles
- Participate in all aspects of the development lifecycle

### Benefits

The internal user approach provides:
- Centralized identity management
- Automated basic access (Read) based on organizational structure
- Clear separation between viewing and contribution rights
- Seamless integration with other organizational tools

## External Users

### Characteristics

External users are:
- Pro-bono contributors
- Volunteers
- Partners
- Contractors not requiring redcross.no accounts
- Use their personal GitHub accounts

### Access Model

External users access GitHub as:
- Outside Collaborators (GitHub's term for external contributors)
- They authenticate with their personal GitHub accounts
- They are granted access to specific repositories only
- They do not need to authenticate through Okta SSO
- They are added to project teams for specific repositories

### Participation in Development

External users can:
- Access only the specific repositories they're invited to
- Join project teams with Write/Maintain permissions
- Create issues and pull requests
- Participate in code reviews
- Collaborate on development tasks

### Benefits

The external user approach provides:
- Low barrier to entry for contributors
- No need for additional accounts
- No consumption of paid GitHub seats
- Straightforward onboarding process
- Repository-specific access control

## Collaboration Models

The two user types enable different collaboration models within the same repositories:

### Internal Team Collaboration

Internal teams rely on a two-tier access model with our 2-level hierarchy:
- Division and Department teams provide Read access (visibility)
- Project teams provide Write/Maintain access (contribution)

```mermaid
flowchart TD
    classDef divTeam fill:#fff7e6,stroke:#fa8c16,stroke-width:1px
    classDef deptTeam fill:#f6ffed,stroke:#52c41a,stroke-width:1px
    classDef projTeam fill:#e6f7ff,stroke:#1890ff,stroke-width:1px
    
    DT[Division Team<br>Read Access] --> DEPT[Department Team<br>Read Access]
    DEPT --> User1[Internal User]
    PT[Project Team<br>Write/Maintain Access] --> User1
    
    DT -.->|View Only| Repo[Repository]
    DEPT -.->|View Only| Repo
    PT -->|Can Contribute| Repo
    
    class DT divTeam
    class DEPT deptTeam
    class PT projTeam
```

**Figure 3: Internal User Access Model with 2-Level Hierarchy**

### External Contributor Collaboration

External collaboration is focused on project teams and specific repositories:

```mermaid
flowchart LR
    classDef projTeam fill:#e6f7ff,stroke:#1890ff,stroke-width:1px
    classDef user fill:#fff7e6,stroke:#fa8c16,stroke-width:1px
    
    EU[External User<br>Outside Collaborator] --- PT[Project Team<br>Write/Maintain Access]
    PT --- Repo[Repository]
    
    class EU user
    class PT projTeam
```

**Figure 4: External User Access Model**

## Security and Governance

The dual-access model maintains security through:

1. **Clear separation of access levels**:
   - Read access based on 2-level organizational structure (internal)
   - Write/Maintain access based on project participation (internal and external)
   - Repository-specific permissions for external contributors

2. **Role-based permissions**:
   - Repository Admins control repository creation and team assignments
   - Team Maintainers manage team membership
   - Branch protection rules enforce code quality for all contributors

3. **Access review processes**:
   - Regular audits of external collaborator access
   - Automatic updates to organizational team membership
   - Periodic review of project team composition

## Best Practices for Mixed Teams

When internal and external users collaborate:

1. **Repository settings**:
   - Branch protection rules apply to all contributors equally
   - Required reviews ensure code quality
   - Status checks enforce testing and CI requirements

2. **Communication**:
   - Use repository discussions for project communication
   - Ensure external contributors are included in relevant conversations
   - Document decisions and requirements clearly

3. **Contribution workflow**:
   - Establish consistent contribution guidelines
   - Document development processes for all contributors
   - Provide clear onboarding for both user types

This dual approach allows Norwegian Red Cross to maintain security and governance while benefiting from the skills and contributions of the broader community.