# Infra_AWS_CloudFormation
repositório organizado contendo anotações e insights adquiridos durante a prática, servindo como material de apoio para os seus estudos e futuras implementações.

🔹 O que é o CloudFormation?

O AWS CloudFormation é um serviço que permite provisionar e gerenciar recursos da AWS de forma declarativa, usando arquivos de template (JSON ou YAML). Em vez de criar manualmente VPCs, instâncias, bancos de dados, etc., você descreve a infraestrutura como código e a AWS cuida da criação, atualização e exclusão.

🔹 Principais Benefícios

Automação Completa – Reduz erros humanos ao eliminar configurações manuais.

Infraestrutura como Código (IaC) – Versionamento de templates no Git, facilitando auditoria e colaboração.

Reprodutibilidade – Crie ambientes de teste, homologação e produção idênticos.

Integração com CI/CD – Pode ser usado em pipelines (CodePipeline, GitHub Actions, Jenkins).

Gerenciamento de Dependências – CloudFormation entende relações entre recursos (ex.: cria a VPC antes da instância).

🔹 Estrutura de um Template CloudFormation

Parameters: variáveis de entrada (ex.: tipo de instância).

Resources: recursos que serão criados (EC2, S3, RDS, VPC).

Outputs: valores de saída, úteis para referência (ex.: endpoint de banco de dados).

Mappings: tabelas estáticas de valores (ex.: AMIs por região).

Conditions: lógica condicional para criação de recursos.

🔹 Passos para Implementar

Definir o template

Especificar em YAML/JSON todos os recursos necessários.

Usar boas práticas de modularização (Nested Stacks para ambientes grandes).

Validar

Executar aws cloudformation validate-template.

Testar em um ambiente de desenvolvimento antes de produção.

Deploy

Criar a Stack pelo Console, CLI ou pipeline.

Acompanhar eventos em tempo real.

Gerenciar Alterações

Usar Change Sets para visualizar o impacto antes de aplicar updates.

Fazer rollback automático em caso de falhas.

Monitorar e Ajustar

Integrar com CloudWatch e CloudTrail para auditoria.

Revisar custos dos recursos provisionados.

🔹 Insights Estratégicos

Padronização corporativa: CloudFormation pode centralizar a criação de infra, aplicando compliance e segurança por padrão.

Redução de custos: facilita apagar ambientes inteiros (Stacks) quando não são mais necessários.

Governança: combinado com Service Catalog, permite oferecer templates prontos para times internos.

Evolução controlada: cada modificação pode ser rastreada via versionamento Git, mantendo histórico e rollback rápido.

Segurança embutida: use IAM Roles e Policies já definidos no template para garantir menor privilégio.

👉 Em resumo: implementar uma infraestrutura automatizada com AWS CloudFormation significa trazer previsibilidade, consistência e agilidade para a criação e manutenção de ambientes na nuvem, reduzindo riscos e aumentando a eficiência operacional.
