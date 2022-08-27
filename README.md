# Setup Azure Workspace

A composite action refer the [docs](https://docs.github.com/en/actions/creating-actions/creating-a-composite-action) including these actions:

1. [Azure Login](https://github.com/marketplace/actions/azure-login)
2. [Azure Container Registry Login](https://github.com/marketplace/actions/azure-container-registry-login)
3. [Azure Kubernetes set context](https://github.com/marketplace/actions/azure-kubernetes-set-context)

## Inputs

| Action inputs      | Description                                                                   |
|--------------------|-------------------------------------------------------------------------------|
| client-id          | associated Azure service principal with an OIDC Federated Identity Credential |
| tenant-id          | associated Azure service principal with an OIDC Federated Identity Credential |
| subscription-id    | associated Azure service principal with an OIDC Federated Identity Credential |
| acr-login-server   | Azure ACR registry                                                            |
| acr-username       | registry username                                                             |
| acr-password       | registry password                                                             |
| aks-resource-group | Resource group containing the AKS cluster                                     |
| aks-cluster-name   | Name of the AKS cluster                                                       |

>  In your GitHub workflow, Set `permissions:` with `id-token: write` at workflow level or job level based on whether the OIDC token needs to be auto-generated for all Jobs or a specific Job.

[Azure Login](https://github.com/marketplace/actions/azure-login#github-action-for-azure-login) require this.

## Outputs

None

## Troubleshooting

TBD
