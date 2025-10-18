# Implementando Infraestrutura Automatizada com AWS CloudFormation

## O que é?

O AWS CloudFormation é um serviço que permite criar, configurar e gerenciar recursos da AWS de forma automatizada. Ele utiliza templates em YAML ou JSON para descrever toda a infraestrutura — como instâncias EC2, bancos de dados RDS, VPCs, entre outros — promovendo padronização e reprodutibilidade.

## Principais Benefícios

- Automação: Cria e gerencia recursos automaticamente, reduzindo erros manuais.
- Infraestrutura como Código (IaC): Permite versionar e auditar a infraestrutura.
- Reutilização: Templates podem ser replicados em diferentes ambientes (dev, test, prod).
- Integração nativa: Compatível com diversos serviços AWS sem necessidade de plug-ins externos.
- Rollback automático: Em caso de falhas, reverte a criação da Stack para o estado anterior.

## Estrutura Básica de um Template

Um template CloudFormation é composto por seções principais:

1. AWSTemplateFormatVersion: Define a versão do formato do template.
2. Description: Breve explicação da Stack.
3. Parameters: Variáveis que permitem customização na criação.
4. Resources: Elemento essencial — define todos os recursos a serem criados.
5. Outputs: Exibe valores gerados, como IDs ou URLs, após a criação.
6. Mappings / Conditions / Metadata: Adicionam lógica e organização ao template.

## Anotação do Fluxo Prático de Uso

1. Criação do Template: Descreva a infraestrutura em YAML/JSON.
2. Upload no CloudFormation Console ou CLI.
3. Definição de parâmetros e nome da Stack.
4. Implantação: CloudFormation provisiona os recursos automaticamente.
5. Monitoramento: Acompanhe o status da Stack (CREATE_IN_PROGRESS, COMPLETE etc.).
6. Gerenciamento: Atualize ou exclua a Stack conforme necessário.

## CloudFormation x Terraform

| Critério                | AWS CloudFormation         | Terraform                              |
| ----------------------- | -------------------------- | -------------------------------------- |
| Provedor                | Exclusivo da AWS           | Multi-cloud (AWS, Azure, GCP, etc.)    |
| Linguagem               | YAML/JSON                  | HCL (HashiCorp Configuration Language) |
| Rollback                | Automático em caso de erro | Necessita configuração manual          |
| Gerenciamento de estado | Interno (na AWS)           | Arquivo de estado (.tfstate)           |
| Integração com AWS      | Nativa                     | Boa, mas via API                       |
| Curva de aprendizado    | Menor para quem usa AWS    | Maior, porém mais flexível             |

## Fontes

- [Documentação Oficial AWS CloudFormation](https://docs.aws.amazon.com/cloudformation)
- [AWS CloudFormation Developer Guide](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/Welcome.html)
