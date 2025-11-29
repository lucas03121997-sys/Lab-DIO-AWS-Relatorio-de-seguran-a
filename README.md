# Lab-DIO-AWS-Relatorio-de-segurança

RELATÓRIO TÉCNICO – Medidas Complementares de Segurança Integradas à AWS

Empresa: [Nome da Empresa]
Responsável: [Nome do Responsável]
Data: [Data Atual]

1. Introdução

Este relatório apresenta três medidas de segurança avançadas que podem ser implementadas em conjunto com os serviços da AWS para aumentar a proteção de ambientes corporativos.
As recomendações abrangem ferramentas, serviços e configurações práticas, alinhadas às melhores práticas de segurança da informação, governança e conformidade.

2. Medidas de Segurança Recomendadas
✅ Medida 1: Hardening do Ambiente com Zero Trust + IAM Reforçado
Objetivo: Reduzir acessos indevidos e limitar o movimento lateral dentro da infraestrutura AWS.
Ações recomendadas:
2.1.1 – Implementar Zero Trust Access

Aplicar o princípio "nunca confie, sempre verifique" por meio de:

MFA obrigatório para todos os usuários e funções críticas.

Bloqueio de credenciais inativas ou temporárias.

Revisão e limitação de permissões usando IAM Access Analyzer.

Substituição de chaves de acesso fixas por IAM Roles.

2.1.2 – Políticas IAM Reforçadas

Utilizar políticas baseadas em least privilege.

Remover permissões wildcard (*).

Implementar session policies para limitar ações mesmo dentro de funções privilegiadas.

Rotacionar automaticamente credenciais com AWS Secrets Manager.

2.1.3 – Ferramentas recomendadas

AWS IAM

AWS IAM Identity Center

AWS Secrets Manager

AWS Access Analyzer

AWS Organizations + SCPs

✅ Medida 2: Camada Adicional de Monitoramento Avançado e Resposta Automatizada
Objetivo: Detectar e responder rapidamente a ameaças, comportamentos anômalos e incidentes internos.
Ações recomendadas:
2.2.1 – Monitoramento contínuo e auditoria

Configurar AWS CloudTrail em todas as contas, com logs centralizados.

Habilitar AWS Config para verificar drift e violação de políticas.

Ativar AWS GuardDuty para detecção inteligente de ameaças.

2.2.2 – Automação de resposta a incidentes

Usar AWS Lambda + CloudWatch Events para respostas automáticas, por exemplo:

Bloquear automaticamente um IP suspeito no AWS WAF.

Desabilitar uma credencial comprometida detectada pelo GuardDuty.

Isolar uma instância EC2 suspeita anexando uma Security Group com política de bloqueio total.

2.2.3 – Ferramentas recomendadas

AWS GuardDuty

AWS Security Hub

AWS Config

AWS CloudTrail

AWS Lambda

Amazon Detective (investigação pós-incidente)

✅ Medida 3: Proteção Avançada de Rede e Dados com Criptografia + WAF + Network Hardening
Objetivo: Impedir invasões externas, mitigar ataques e proteger dados sensíveis.
Ações recomendadas:
2.3.1 – Fortalecimento da infraestrutura de rede

Implementar segmentação de rede usando VPCs, Subnets privadas e NACLs.

Usar AWS Firewall Manager + AWS WAF em todas as aplicações expostas.

Restringir portas de administração usando AWS Systems Manager Session Manager (evitando SSH/RDP).

Implementar inspeção adicional com Amazon GuardDuty Malware Protection.

2.3.2 – Criptografia completa de dados

Criptografia em repouso com KMS CMKs gerenciadas.

Criptografia em trânsito com TLS 1.2+ e certificados do AWS Certificate Manager.

Ativar S3 Block Public Access e políticas de bucket restritas.

2.3.3 – Backup e resiliência

Habilitar AWS Backup com retenção imutável (WORM).

Criar políticas de cross-region backup para recuperação em desastres.

2.3.4 – Ferramentas recomendadas

AWS WAF

AWS Firewall Manager

AWS KMS

AWS Backup

AWS Certificate Manager

AWS Systems Manager Session Manager

Amazon VPC Lattice / Security Groups

3. Conclusão

A adoção combinada dessas três medidas proporciona uma arquitetura de segurança robusta, alinhada aos padrões modernos de proteção corporativa.
Com a integração correta entre políticas IAM, monitoramento avançado, automação e segurança de rede, a empresa reduz significativamente seu risco operacional e melhora sua postura de segurança frente a ameaças internas e externas.

Se desejar, posso complementar com:

✔ matriz RACI
✔ plano de ação em etapas
✔ controles baseados na ISO 27001
✔ inserir timbre, capa e transformar em Word
