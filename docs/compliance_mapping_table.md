# Compliance Mapping Table

This table maps privacy-preserving cloud security controls to major healthcare and cloud security compliance frameworks.

| Control Area | Technical Control | HIPAA/HITECH Relevance | GDPR Relevance | NIST SP 800-53 Relevance | CSA Cloud Security Relevance | Research Notes |
|---|---|---|---|---|---|---|
| Data in transit | TLS, secure API gateways | Supports transmission security | Supports integrity and confidentiality | SC-8, SC-13 | Secure communications | Baseline control, not sufficient for analytics privacy |
| Data at rest | AES encryption, database encryption | Supports ePHI protection | Supports confidentiality and storage limitation | SC-28 | Data protection lifecycle | Commonly implemented but does not protect data during processing |
| Data in use | Homomorphic encryption | Supports reduced exposure of sensitive healthcare data | Supports privacy by design and data minimization | SC-13, SC-28, privacy controls | Data-use protection | Central research focus |
| Identity and access | MFA, RBAC, ABAC, least privilege | Access control and auditability | Access limitation and accountability | AC-2, AC-3, IA-2 | IAM controls | Required for implementation maturity |
| Key management | KMS/HSM, rotation, segregation of duties | Safeguards encryption keys | Security of processing | SC-12, SC-17 | Key management lifecycle | Key management maturity may affect HE adoption |
| Monitoring and audit | SIEM, logs, traces, audit records | Audit controls and incident response | Accountability and breach detection | AU family, IR family | Logging and monitoring | Supports compliance evidence |
| Governance | Policies, risk assessments, vendor reviews | Administrative safeguards | Privacy governance and accountability | PM, RA, PL families | Governance, risk, compliance | Connects technical security to organizational readiness |
| Vendor support | Cloud provider services, managed encryption, HE tooling | Business associate / vendor risk | Processor/subprocessor accountability | SA family | Third-party risk | Dissertation finding: vendor support can influence implementation success |
