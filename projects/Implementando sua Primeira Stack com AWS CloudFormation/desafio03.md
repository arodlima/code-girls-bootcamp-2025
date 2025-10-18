# Implementando sua Primeira Stack com AWS CloudFormation

## O que é?

O **AWS CloudFormation** é um serviço que permite criar, configurar e gerenciar recursos da AWS de forma automatizada, utilizando **templates em formato YAML ou JSON**. Ele aplica o conceito de Infraestrutura como Código (IaC), permitindo que toda a infraestrutura seja versionada, replicada e atualizada com segurança.

## Principais características

- **Automação**: provisiona e configura recursos automaticamente.
- **Reprodutibilidade**: permite recriar ambientes idênticos com base em um template.
- **Gerenciamento simplificado**: possibilita criar, atualizar e excluir grupos de recursos de uma só vez.
- **Integração com outros serviços AWS**: funciona bem com Lambda, EC2, S3, IAM, entre outros.
- **Controle de versões**: os templates podem ser versionados junto com o código do projeto.
- **Rollback automático**: reverte mudanças caso ocorra falha na criação da Stack.

## Conceito de Stack

Uma **Stack (pilha)** é um conjunto de recursos AWS (como instâncias EC2, buckets S3, funções Lambda, etc.) criados e gerenciados juntos a partir de um template CloudFormation.

- Cada Stack é baseada em um template que descreve a infraestrutura desejada.
- É possível **atualizar** ou **deletar** todos os recursos de uma Stack em uma única ação.
- Exemplo: uma Stack pode conter os recursos necessários para um ambiente de aplicação completo (rede, servidor, banco de dados e permissões).

## Fluxo para criar uma Stack pelo Console

1. Acesse o Console AWS e abra o serviço CloudFormation.
2. Clique em Create stack → With new resources (standard).
3. Escolha o método de criação:
   - Template pronto da AWS,
   - Upload de um arquivo YAML/JSON,
   - ou Especificar URL do template armazenado no S3.
4. Defina o nome da Stack e parametrizações (valores variáveis do template).
5. Revise as configurações, marque a opção de confirmação de criação de recursos IAM (se houver) e clique em Create stack.
6. Acompanhe o progresso na aba Events até o status CREATE_COMPLETE.
7. Consulte os recursos criados na aba Resources.

## Fontes

- [AWS CloudFormation - Documentação Oficial](https://docs.aws.amazon.com/pt_br/AWSCloudFormation/latest/UserGuide/Welcome.html)
- [AWS CloudFormation - Conceitos Básicos](https://aws.amazon.com/pt/cloudformation/faqs)
