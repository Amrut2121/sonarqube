# SonarQube on AKS with Azure PostgreSQL + Entra ID

## Setup Summary

1. AKS configured with Azure Workload Identity.
2. Azure PostgreSQL Server uses AAD Authentication.
3. `values.yaml` disables internal PostgreSQL and uses a JDBC URL.
4. Authentication token is fetched via Entra ID and injected via Workload Identity.

## Notes

- Ensure the PostgreSQL Server is configured to accept AAD logins.
- Azure Workload Identity must be correctly bound to the Kubernetes service account.
