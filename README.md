# Provisionamento de VM no Azure via Azure DevOps com Terraform

## Estrutura
Este projeto automatiza a criação de uma máquina virtual Windows no Azure usando Terraform executado via pipeline do Azure DevOps.

## Requisitos
- Azure Subscription com permissões para criar recursos.
- Azure DevOps project configurado com Service Connection.
- Terraform instalado no pipeline (`UseTerraform@0`).

## Pipeline
O pipeline `azure-pipelines.yml` executa os seguintes passos:
1. `terraform init`
2. `terraform plan`
3. `terraform apply`

## Segurança
- Mantenha `admin_password` seguro usando Azure KeyVault ou pipelines secrets.