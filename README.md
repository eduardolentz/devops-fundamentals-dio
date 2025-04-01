
# Infraestrutura como Código com Terraform e Azure DevOps

Este projeto tem como objetivo automatizar o provisionamento de recursos na **Microsoft Azure** utilizando **Terraform** e integrá-lo a um pipeline de **Integração Contínua e Entrega Contínua (CI/CD)** no **Azure DevOps**. O objetivo é criar uma infraestrutura escalável e eficiente, automatizando o processo de criação e gerenciamento de recursos na nuvem.

## Objetivo do Projeto

A solução implementa o conceito de **Infraestrutura como Código (IaC)** para facilitar a criação e gerenciamento de recursos na **Azure**, como **Resource Groups**, **Storage Accounts**, e outros serviços necessários. A automação do pipeline no **Azure DevOps** permite que os recursos sejam provisionados e implantados de forma ágil e consistente.

## Tecnologias Utilizadas

- **Terraform**: Ferramenta de **Infraestrutura como Código** para provisionamento de recursos na Azure.
- **Azure DevOps**: Plataforma de CI/CD para automação de testes, builds e deploys.
- **Microsoft Azure**: Plataforma de nuvem onde os recursos são provisionados.
- **GitHub**: Repositório para versionamento e gerenciamento do código.

## Estrutura do Repositório

- **codigoTerraform/**: Contém os arquivos de configuração do Terraform.
  - `site.tf`: Define os recursos de infraestrutura a serem criados no Azure, como **Resource Groups** e **Storage Accounts**.
  - `variables.tf`: Declara variáveis que tornam as configurações do Terraform reutilizáveis e personalizáveis.

- **azure-pipelines.yml**: Arquivo de configuração do pipeline no Azure DevOps, que inclui as etapas de validação e aplicação do código Terraform e o deploy de recursos no Azure.

- **README.md**: Documentação do projeto.

## Como Usar

### Pré-requisitos

1. **Conta no Azure**: Você precisa de uma conta no **Microsoft Azure**. Se ainda não tiver, crie uma conta gratuita [aqui](https://azure.microsoft.com/en-us/free/).
2. **Conta no Azure DevOps**: Crie uma conta no **Azure DevOps** [aqui](https://dev.azure.com/).
3. **Terraform**: Instale o **Terraform** em sua máquina local ou utilize o [Azure Cloud Shell](https://docs.microsoft.com/pt-br/azure/cloud-shell/overview).
4. **GitHub**: Para versionamento do código.

### Passos para Configuração

1. **Clone o Repositório**:
   ```bash
   git clone <URL_do_repositorio>
   cd <nome_do_repositorio>
   ```

2. **Configuração do Azure DevOps**:
   - Crie um novo projeto no **Azure DevOps**.
   - No seu projeto, crie um **Pipeline** e configure-o para utilizar o arquivo `azure-pipelines.yml`.

3. **Configuração do Azure e Terraform**:
   - Autentique-se no **Azure** utilizando o comando `az login` (para autenticação local) ou configure as credenciais diretamente no **Azure DevOps**.
   - Inicialize o Terraform:
     ```bash
     terraform init
     ```

4. **Execução do Pipeline**:
   - Após o primeiro commit, o pipeline será acionado automaticamente, validando e aplicando as configurações do Terraform para provisionar os recursos na Azure.

### Etapas do Pipeline

1. **Inicialização do Terraform**: `terraform init`
2. **Validação do Código**: `terraform validate`
3. **Plano de Execução**: `terraform plan`
4. **Aplicação do Código**: `terraform apply`

### Acessando os Recursos

Após a execução bem-sucedida do pipeline, os recursos provisionados, como **Resource Group** e **Storage Account**, estarão disponíveis na sua conta **Azure**. Acesse o [portal Azure](https://portal.azure.com/) para visualizar os recursos.

---
### Eduardo O. Lentz
💻 Portfolio | 🔗 LinkedIn | 📂 GitHub | 📝 Medium | 📸 Instagram

