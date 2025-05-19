# Revised GitHub Structure for Norwegian Red Cross

## Aligning with GitHub Best Practices

Based on industry best practices for GitHub in large organizations, we're revising our approach to focus more on product ownership and collaboration while still maintaining logical separation between divisions.

## Organization Structure

We will maintain a single GitHub organization for Norwegian Red Cross with these structural elements:

```mermaid
graph TD
    A[Norwegian Red Cross GitHub Organization] --> B[Shared Services]
    A --> C[Regional Products]
    A --> D[National Products]
    
    B --> B1[Infrastructure]
    B --> B2[Design System]
    B --> B3[API Platform]
    
    C --> C1[Volunteer Management]
    C --> C2[Local Websites]
    C --> C3[Event Management]
    
    D --> D1[National Websites]
    D --> D2[Finance Systems]
    D --> D3[CRM & Fundraising]
```

**Figure 1:** Product-Based Organization Structure

## Repository Naming Conventions

Repositories will follow a product/service-focused naming convention while still indicating divisional ownership:

```
[product-area]-[component]-[division]
```

### Examples:

#### Shared Services:
- `infrastructure-monitoring`
- `design-system-components`
- `api-platform-core`

#### Regional Products with Division Indicators:
- `volunteer-portal-oslo`
- `website-frontend-hordaland`
- `event-management-oslo`

#### National Products:
- `crm-donor-management`
- `finance-reporting`
- `national-website-frontend`

This approach maintains divisional context where needed while emphasizing the product or service function first.

## Team Structure

The team structure will focus on product responsibilities while using nested teams to manage access for organizational units:

```mermaid
graph TD
    classDef productTeam fill:#e6f7ff,stroke:#1890ff
    classDef divisionTeam fill:#fff7e6,stroke:#fa8c16
    classDef accessTeam fill:#f6ffed,stroke:#52c41a

    NRC[Norwegian Red Cross Organization]
    
    PT1[Infrastructure Team]
    PT2[API Platform Team]
    PT3[Volunteer Systems Team]
    PT4[Website Team]
    PT5[Finance Systems Team]
    
    DT1[Hovedkontor]
    DT2[Oslo]
    DT3[Hordaland]
    
    AT1[Repository Managers]
    AT2[Security Review]
    
    NRC --> PT1
    NRC --> PT2
    NRC --> PT3
    NRC --> PT4
    NRC --> PT5
    
    NRC --> DT1
    NRC --> DT2
    NRC --> DT3
    
    NRC --> AT1
    NRC --> AT2
    
    class PT1,PT2,PT3,PT4,PT5 productTeam
    class DT1,DT2,DT3 divisionTeam
    class AT1,AT2 accessTeam
```

**Figure 2:** Product-Focused Team Structure

### Key Teams and Roles

1. **Product Teams**
   - Purpose: Teams organized around specific products or services
   - Members: Cross-functional team members with expertise in that product/service
   - Permissions: Primary maintainers of related repositories
   - Example: "API Platform Team" manages all API-related repositories

2. **Division Teams**
   - Purpose: Teams representing organizational divisions (Hovedkontor, Oslo, etc.)
   - Members: All users who belong to that division
   - Permissions: Read access to repositories relevant to their division
   - Example: "Oslo" team includes all Oslo Red Cross staff

3. **Access Management Teams**
   - Purpose: Teams with special access management responsibilities
   - Members: Trusted administrators and security personnel
   - Permissions: Repository creation, security review, etc.
   - Example: "Repository Managers" team has repository creation permissions

4. **Project Teams**
   - Purpose: Temporary teams formed for specific projects
   - Members: Contributors from various divisions working on a specific initiative
   - Permissions: Write access to project-specific repositories
   - Example: "Website Redesign Team" for a time-limited project

## Permission Model

The permission model will now balance product ownership with divisional context:

### Permission Levels Matrix

| Team Type | Repository Type | Permission Level | Purpose |
|-----------|----------------|------------------|---------|
| Product Teams | Related product repos | Admin/Write | Primary maintainers |
| Division Teams | Division-specific repos | Read | Division-wide visibility |
| Repository Managers | All repos | Admin (creation only) | Governance and standards |
| Project Teams | Project-specific repos | Write | Temporary collaboration |

### Cross-Functional Collaboration

To foster innersourcing and collaboration:

1. **Default Visibility**
   - Most repositories should be visible to all organization members
   - Encourage cross-team contributions through pull requests

2. **Contribution Process**
   - Anyone can propose changes via fork and pull request model
   - Product teams review and approve contributions

3. **Shared Resources**
   - Common components should be in dedicated repositories
   - Encourage reuse across division boundaries

## Implementation Plan

To transition to this product-focused structure while maintaining divisional context:

1. **Create Product Teams**
   - Identify key product areas and services
   - Create corresponding teams with clear ownership

2. **Map Current Teams**
   - Map existing staff to both product and division teams
   - Many staff will belong to multiple teams

3. **Adjust Repository Structure**
   - Begin with new repositories following product-first naming
   - Gradually migrate existing repositories as appropriate

4. **Documentation**
   - Create clear documentation explaining the product-focused model
   - Provide guidelines for cross-team collaboration

## Best Practices Alignment

This revised approach better aligns with GitHub best practices by:

- Focusing on product ownership rather than organizational structure
- Enabling cross-divisional collaboration and innersourcing
- Maintaining divisional context where needed
- Simplifying permission management
- Encouraging code reuse and shared responsibility