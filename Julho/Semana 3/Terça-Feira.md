# 📅 Diário de Aprendizado - FAP

> 📅 **Aulas:** Terças e Quintas  

---

## Semana x (14/07/2026 - 16/07/2026)

### Terça-feira (14/07/2026) - 🎓 Aula 1
**Status:** ✅ Concluído  
**Tempo:** 3 horas (aula presencial)
**Conteúdo:** 

## O que aprendi:

 ### Kanban vs Scrum                                                                                    
  | Aspecto | Kanban | Scrum |
  |--------|--------|-------|
  | Iterações | Contínuo, sem sprints fixos | Sprints fixas (2-4 semanas) |
  | Papéis | Nenhum obrigatório | PO, Scrum Master, Dev Team |
  | Planejamento | Sob demanda | Planejamento de sprint |
  | Limite de WIP | Sim | Não por padrão |
  | Mudanças | A qualquer momento | Congeladas na sprint |
  | Reuniões | Mínimas | Daily, review, retro, planning |

  - **Kanban:** fluxo contínuo/imprevisível, foco em reduzir tempo de ciclo e gargalos.
  - **Scrum:** entregas previsíveis por sprint, estrutura e ritmo definidos.

  ### Scrumban (Scrum + Kanban)

  - Sprints/ritmo do Scrum + limite de WIP e pull do Kanban.
  - Tarefas entram por pull quando há capacidade; ajustes aceitos no meio.
  - Bom para manutenção (bugs urgentes surgem no meio do caminho).

  ## Ferramentas

  - Jira, Trello, Azure DevOps, Linear, ClickUp/Asana.
  - Scrumban = como organizar, não um produto específico.

--- 

## SOA vs Microservices

  | Ponto | SOA | Microservices |
  |-------|-----|---------------|
  | Granularidade | Grossa | Fina |
  | Comunicação | ESB pesado | API leve / mensageria |
  | Dados | Compartilhados | Por serviço |
  | Deploy | Coordenado | Independente |

  - **SOA:** serviços reutilizáveis via ESB, foco em integração corporativa.
  - **Microservices:** serviços pequenos/independentes, cada um com seu banco.
  - Microservices = evolução da SOA, eliminando o ESB como ponto central de falha.
  - Trade-off: microservices traz complexidade distribuída (rede, consistência).

---

 ### IaC (Infrastructure as Code)                                                                        - Infra declarada em código (não manual). Versionável e reproduzível.
  - **Terraform** (multi-cloud, declarativo), **CloudFormation** (AWS), **Pulumi** (código real:
  Python/TS), **Ansible** (configuração/SSH).

  ### Containers
  - Empacotam app + dependências; isolamento leve via kernel do host.
  - **Docker** (padrão), **containerd**, **Podman** (sem daemon).
  - Orquestração: **Kubernetes** (padrão), **Docker Swarm**, **Nomad**.

  ### CI/CD (Continuous Integration / Continuous Delivery)
  - **CI:** builds e testes automáticos a cada commit.
  - **CD:** deploy automático (staging/prod) após aprovação.
  - **GitHub Actions**, **GitLab CI**, **Jenkins** (self-host), **CircleCI**, **ArgoCD** (GitOps para
  K8s).

  ### Integração no fluxo
  - IaC provisiona infra → Containers empacotam o app → CI/CD faz build/test/deploy.
  - Pipeline típico: `git push` → CI roda testes → builda imagem Docker → CD faz deploy em cluster K8s
  provisionado por Terraform.

  Copie e cole no mesmo README. Se quiser, posso também fechar o bloco anterior unindo tudo num único
  arquivo.


- Desafios em Redes, Segurança e Observabilidade
- Decisão: SOA versus Microsserviços

**O que teve Hioje**

-Apresentação do trabalho de Planejamento de Sprint

**Dificuldades:**
- Extrema dificultade em apresentar, sei o asusnto mas não consigo aprentar, travo na hora e nao consigo fazer uma apresentção digina 

---
