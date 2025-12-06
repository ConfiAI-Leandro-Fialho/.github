# 🧬 Arquitetura Técnica da ConfiAI — Visão Big Tech

Este documento descreve a **arquitetura técnica oficial** da plataforma ConfiAI,
no formato “Big Tech style”, organizada em camadas.

```text
+--------------------------------------------------------------+
|                    ConfiAI GitHub Organization               |
|              (Repositórios, UBK, Governança Global)          |
+--------------------------------------------------------------+
                              |
                              v
+--------------------------------------------------------------+
|                Core Cognitive Layer (Tronco Central)         |
+--------------------------------------------------------------+
|  confiai-ubk-spec  |  confiai-kb-core  |  confiai-cae-engine |
| (Regras & SPECS)   | (KB Declarativa)  | (Jobs & Actions)    |
+--------------------+-------------------+---------------------+
                             |
                             v
+--------------------------------------------------------------+
|                    Orchestration & Agent Layer               |
+--------------------------------------------------------------+
|                  confiai-joe-agent (Agente Operacional)      |
|   - API interna ConfiAI                                      |
|   - Ponte entre UBK / KB / CAE / n8n / Odoo / Chatwoot       |
+--------------------------------------------------------------+
                             |
                             v
+--------------------------------------------------------------+
|                Support & Platform Layer (Anel de Suporte)    |
+--------------------------------------------------------------+
|  confiai-infra   | confiai-devops | confiai-governance       |
| (Redes,          | (CI/CD,        | (Políticas, Auditoria,    |
|  containers,     |  deploy,       |  GitOps, Segurança)       |
|  borda Traefik)  |  observabilidade)                         |
+------------------+----------------+--------------------------+
|       confiai-n8n-workflows        |   confiai-data-core     |
|  (Fluxos de automação, pipelines)  | (Data lake, ETL/ELT,    |
|                                    |  datasets bronze/silver/|
|                                    |  gold para IA/BI/CAE)   |
+--------------------------------------------------------------+
                             |
                             v
+--------------------------------------------------------------+
|                Integration & Application Layer               |
+--------------------------------------------------------------+
|  Odoo / ERP   |  WordPress  |  Chatwoot / WhatsApp / Web    |
|  (CRM,        |  (Conteúdo, |  (Atendimento omnichannel)    |
|   Financeiro, |   Marketing)|                              |
|   Projetos)   |             |  Outras APIs externas         |
+--------------------------------------------------------------+
                             |
                             v
+--------------------------------------------------------------+
|             Usuários Finais, Clientes, Parceiros, LFA        |
+--------------------------------------------------------------+

               (Canal histórico / migração controlada)
+--------------------------------------------------------------+
|      confiai-knowledge-core (Legacy Knowledge Core)          |
|  - Somente leitura                                            |
|  - Fonte histórica para migração para o confiai-kb-core       |
+--------------------------------------------------------------+
Esta visão é usada para:

documentação técnica;

governança e GitOps;

seeds da CAE;

integração com DevOps, Infra e Data Core;

alinhamento com parceiros tecnológicos.

Para uma visão mais conceitual e inspiradora (Árvore da Prosperidade),
consulte a visão arquitetural complementar quando publicada.
