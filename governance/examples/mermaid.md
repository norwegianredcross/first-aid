# Mermaid Examples

This document provides examples of well-formatted Mermaid diagrams for Norwegian Red Cross GitHub documentation.

## Governance Document Relationships


```mermaid
flowchart TD
    classDef roles fill:#8a2be2,stroke:#4b0082,stroke-width:2px,color:#ffffff
    classDef users fill:#1e90ff,stroke:#0000cd,stroke-width:2px,color:#ffffff
    classDef repo fill:#2e8b57,stroke:#006400,stroke-width:2px,color:#ffffff
    classDef process fill:#ff8c00,stroke:#d2691e,stroke-width:2px,color:#ffffff
    classDef platform fill:#d81b60,stroke:#c2185b,stroke-width:2px,color:#ffffff
    classDef security fill:#d32f2f,stroke:#b71c1c,stroke-width:2px,color:#ffffff
    
    R[01-github-governance-roles.md]
    U1[02-github-internal-external.md]
    U2[03-github-provisioning.md]
    RG[04-github-repository-governance.md]
    RN[05-github-repository-naming.md]
    S[06-github-servicenow.md]
    P[07-platform-selection-guidelines.md]
    SEC[08-github-security-standards.md]
    
    R --> U1
    R --> RG
    
    U1 --> U2
    
    RG --> RN
    RG --> S
    
    U2 --> S
    
    S -.-> P
    RG -.-> P
    
    SEC --> R
    SEC --> RG
    SEC --> U1
    
    class R roles
    class U1,U2 users
    class RG,RN repo
    class S process
    class P platform
    class SEC security
```

**Figure 1: Relationships between governance documents**

## Documentation Structure Example

```mermaid
flowchart TD
    classDef root fill:#8a2be2,stroke:#4b0082,stroke-width:2px,color:#ffffff
    classDef required fill:#2e8b57,stroke:#006400,stroke-width:2px,color:#ffffff
    classDef optional fill:#ff8c00,stroke:#d2691e,stroke-width:2px,color:#ffffff
    classDef process fill:#1e90ff,stroke:#0000cd,stroke-width:2px,color:#ffffff
    classDef security fill:#d32f2f,stroke:#b71c1c,stroke-width:2px,color:#ffffff
    classDef support fill:#d81b60,stroke:#c2185b,stroke-width:2px,color:#ffffff
    classDef dark fill:#000000,stroke:#ffffff,stroke-width:2px,color:#ffffff
    classDef light fill:#ffffff,stroke:#000000,stroke-width:2px,color:#000000
    classDef template fill:#4b0082,stroke:#000000,stroke-width:1px,color:#ffffff
    
    A[Repository Documentation] --> B[Required Documents]
    A --> C[Optional Documents]
    
    B --> D[README.md]
    B --> E[CONTRIBUTING.md]
    B --> F[CODEOWNERS]
    B --> G[LICENSE]
    
    C --> H[SECURITY.md]
    C --> I[SUPPORT.md]
    C --> J[CHANGELOG.md]
    
    H --> H1[SECURITY.md template]
    
    D --> D1[README.md template]
    E --> E1[CONTRIBUTING.md template]
    F --> F1[CODEOWNERS template]
    G --> G1[LICENSE templates]
    G1 --> G2[LICENSE-opensource.md]
    G1 --> G3[LICENSE-internal.md]
    
    class A root
    class B,D,E,F,G required
    class C optional
    class E process
    class H security
    class I support
    class J optional
    class D dark
    class G light
    class D1,E1,F1,G1,G2,G3,H1 template
```

**Figure 2: Repository documentation structure example**

## Sequence Diagram Example

```mermaid
sequenceDiagram
    actor Dev as Developer
    participant RA as Repository Admin
    participant GH as GitHub
    
    Dev->>RA: Request repository creation
    RA->>GH: Create repository
    RA->>GH: Configure branch protection
    RA->>GH: Set up required files
    
    GH-->>RA: Repository created
    RA-->>Dev: Repository access granted
    
    Dev->>GH: Clone repository
    Dev->>GH: Make changes
    Dev->>GH: Create pull request
    
    GH->>RA: Notify of PR
    RA->>GH: Review PR
    RA->>GH: Approve and merge
```

**Figure 3: Repository creation sequence diagram example**
