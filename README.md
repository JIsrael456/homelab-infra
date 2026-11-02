# Homelab Infra — JI Tech Solutions

Laboratório pessoal de infraestrutura de TI, construído para simular o ambiente corporativo de uma empresa fictícia — a **JI Tech Solutions** — e desenvolver, na prática, competências de Infraestrutura, Cloud, Automação e Dados.

## Progresso do projeto

**Situação documentada:** as fases 01 e 02 têm suas implementações principais registradas, mas ainda possuem itens pendentes; a fase 03 foi realizada anteriormente e precisa ser revalidada após a reinstalação da estação. Portanto, o histórico de **3/11 (27%)** não deve ser interpretado como 3 fases integralmente concluídas no estado atual.

> O indicador anterior de 27% era manual. A partir desta revisão, a conclusão integral de uma fase exige checklist atualizado, validações e evidências. Não há percentual de conclusão integral auditado até a revisão das pendências.

| Fase | Tema | Situação documentada |
|---|---|---|
| [01](./fase-01-rede) | Infraestrutura de Rede | 🟡 Implementação principal registrada; DHCP pendente |
| [02](./fase-02-windows-server) | Windows Server | 🟡 AD DS/DNS/OUs/GPOs documentados; DHCP e compartilhamentos pendentes |
| [03](./fase-03-windows-client) | Windows Cliente | 🔄 Revalidação após reinstalação pendente |
| [04](./fase-04-linux) | Linux | ⏳ Planejada |
| [05](./fase-05-docker) | Docker | ⏳ Planejada |
| [06](./fase-06-banco-de-dados) | Banco de Dados | ⏳ Planejada |
| [07](./fase-07-powershell) | PowerShell | ⏳ Planejada |
| [08](./fase-08-shell) | Shell Script | ⏳ Planejada |
| [09](./fase-09-google-cloud) | Google Cloud | ⏳ Planejada |
| [10](./fase-10-powerbi) | Power BI | ⏳ Planejada |
| [11](./fase-11-monitoramento) | Monitoramento | ⏳ Planejada |

Confira o checklist técnico e os registros históricos em [progresso](./progresso).

## Por que este projeto existe

Depois de atuar como Assistente de TI (Google Workspace, gestão de acessos/IAM, infraestrutura e suporte), decidi ir além de cursos e certificados: montar um ambiente integrado onde cada tecnologia estudada é aplicada de verdade, documentada e conectada às demais — como aconteceria numa empresa real.

Em vez de vários projetos isolados, todas as fases fazem parte de uma única infraestrutura corporativa simulada.

## Objetivos

- Consolidar conhecimentos em Infraestrutura de TI
- Aprender Cloud Computing na prática
- Desenvolver habilidades em automação (PowerShell e Shell Script)
- Aprofundar Banco de Dados e Power BI
- Produzir documentação técnica no padrão usado em empresas
- Construir um portfólio técnico público no GitHub

## A empresa fictícia: JI Tech Solutions

A JI Tech Solutions possui 50 colaboradores distribuídos entre RH, Financeiro, Comercial, Diretoria e TI. No cenário-alvo, a autenticação é centralizada no Active Directory; Linux, PostgreSQL, backups no Google Cloud Storage e dashboards em Power BI fazem parte das etapas planejadas, ainda não declaradas como implantadas.

Mais detalhes em [`Empresa.md`](./Empresa.md).

## Estrutura do projeto

| Fase | Tema | Objetivo | Resultado esperado |
|------|------|----------|---------------------|
| [01](./fase-01-rede) | Infraestrutura de Rede | Planejar IPs, DNS, gateway e comunicação entre servidores | Toda a infraestrutura consegue se comunicar |
| [02](./fase-02-windows-server) | Windows Server | Active Directory, DNS, DHCP, GPO, usuários, grupos, compartilhamentos | Autenticação centralizada da empresa |
| [03](./fase-03-windows-client) | Windows Cliente | Entrada no domínio, login, validação de GPO, acesso a compartilhamentos | Simulação de um computador corporativo |
| [04](./fase-04-linux) | Linux | SSH, Apache/Nginx, firewall, usuários e permissões | Servidor responsável pelos serviços internos |
| [05](./fase-05-docker) | Docker | Containerização de PostgreSQL, Grafana, Portainer, Nginx | Serviços executando em containers |
| [06](./fase-06-banco-de-dados) | Banco de Dados | Modelagem, SQL, tabelas, consultas | Banco utilizado pelos sistemas e dashboards |
| [07](./fase-07-powershell) | PowerShell | Criação de usuários, desativação de contas, inventário, relatórios | Administração automatizada do ambiente Windows |
| [08](./fase-08-shell) | Shell Script | Atualizações, backups, monitoramento, limpeza de logs | Administração automatizada do ambiente Linux |
| [09](./fase-09-google-cloud) | Google Cloud | Cloud Storage, IAM, Compute Engine, backup | Ambiente híbrido entre infraestrutura local e nuvem |
| [10](./fase-10-powerbi) | Power BI | Dashboards de inventário, chamados e usuários | Painéis gerenciais para tomada de decisão |
| [11](./fase-11-monitoramento) | Monitoramento | Grafana, Prometheus, alertas, dashboards técnicos | Monitoramento centralizado de servidores e serviços |

As pastas organizam a documentação por fase; o nível de implementação e a disponibilidade de evidências variam entre as fases.

## Tecnologias implementadas e planejadas

**Documentadas na implementação principal:** VirtualBox, IPv4, Windows Server 2025, Active Directory, DNS, OUs, grupos e GPOs. O ingresso do cliente Windows ocorreu anteriormente, mas requer revalidação após reinstalação.

**Planejadas ou com pendências:** DHCP, compartilhamentos, Linux, Docker, PostgreSQL, SQL, PowerShell, Shell Script, Google Cloud, Power BI, Grafana e Prometheus.

## Tecnologias do escopo geral

`Active Directory` · `Windows Server` · `Windows 11` · `Linux` · `Docker` · `PostgreSQL` · `SQL` · `PowerShell` · `Shell Script` · `Google Cloud Platform` · `Power BI` · `Grafana` · `Prometheus`

## Documentação

Documentação complementar (arquitetura, diagrama de rede, inventário e plano de backup) fica em [`docs/`](./docs) e no [`Projeto_Homelab.md`](./Projeto_Homelab.md).

## Objetivo final

Ao concluir todas as fases, este repositório vai representar uma infraestrutura corporativa completa, documentada e funcional — reunindo Infraestrutura, Windows Server, Linux, Redes, Active Directory, Docker, Banco de Dados, SQL, PowerShell, Shell Script, Google Cloud, Power BI e Monitoramento.

Mais do que um conjunto de cursos, é a evidência prática da capacidade de planejar, implantar, integrar e documentar uma infraestrutura de TI semelhante à de uma empresa real — servindo como portfólio técnico para oportunidades em Infraestrutura, Cloud, Administração de Sistemas e Engenharia de Dados.

## Autor

**Jacó Israel**
[LinkedIn](https://linkedin.com/in/jaco-israel)
