# HE/Cloud Security Architecture Diagram

This diagram shows a privacy-preserving architecture for cloud-based healthcare databases using homomorphic encryption, cloud security controls, key management, observability, and compliance governance.

```mermaid
flowchart TB
    U[Healthcare Users<br/>Clinicians, Analysts, Researchers] --> A[Secure Web / API Layer]
    A --> AUTH[Identity and Access Management<br/>SSO, MFA, RBAC, ABAC]
    AUTH --> API[Application Services<br/>Kubernetes / Containers]
    API --> ENC[Encryption Control Layer<br/>TLS, AES/RSA, Hybrid Encryption]
    ENC --> HE[Homomorphic Encryption Layer<br/>Data-in-Use Protection]
    HE --> DB[(Cloud Healthcare Database<br/>EHR / Clinical / Claims Data)]

    KMS[Cloud KMS / HSM<br/>Key Rotation, Segregation, Audit] --> ENC
    KMS --> HE

    API --> OBS[Observability and Security Monitoring<br/>Logs, Metrics, Traces, SIEM]
    DB --> AUDIT[Audit and Compliance Evidence<br/>HIPAA, GDPR, HITECH, NIST, CSA]
    OBS --> AUDIT
    KMS --> AUDIT

    GOV[Governance and Risk Controls<br/>Policies, Risk Assessment, Access Reviews] --> AUTH
    GOV --> AUDIT

    AI[AI / Analytics Workloads<br/>Privacy-Preserving Querying] --> HE
    AI --> RESULTS[Encrypted / De-identified Results]
```

## Architecture Summary

The architecture protects healthcare data across three major states:

| Data State | Primary Controls | Research Relevance |
|---|---|---|
| Data in transit | TLS, API security, identity controls | Prevents interception and unauthorized access |
| Data at rest | AES, cloud database encryption, KMS/HSM | Protects stored healthcare records |
| Data in use | Homomorphic encryption / privacy-preserving computation | Reduces exposure during query and analytics processing |

## Research Contribution

This architecture supports the research argument that healthcare cloud security should not rely only on traditional encryption at rest and in transit. For sensitive healthcare analytics and AI workloads, data-in-use protection is a critical layer for privacy-preserving computation and compliance-aware system design.
