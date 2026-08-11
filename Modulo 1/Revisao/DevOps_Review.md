# Convite Para Revisão: Questões de DevOps

Este documento resume as 9 questões que você respondeu ao longo da sessão, detalhando cada *conceito* e a lógica por trás da escolha da resposta correta. O intuito é servir como material de estudo para a prova e para reforçar a compreensão dos principais pilares de DevOps.

---

## Questão 1 – Estratégia de Ramificação
**Pergunta resumida**: Qual ramificação promoverá múltiplos deployments diários e evitará *merge hell*?

### Resposta
**D – Trunk‑Based Development**

### Por que?
- **Integrações frequentes**: Desenvolvedores fazem commits diretamente no *trunk* (ou em branches de curta duração), evitando divergência.
- **Menos conflitos**: Como não há longos ramos de feature, conflitos são mínimos e resolvidos rapidamente.
- **Melhora da entrega**: A frequência de commits facilita a entrega diária.
- **Oposto ao GitFlow/Release Branch**: Essas abordagens mantêm ramos longos, exacerbando problemas de merge.

---

## Questão 2 – Gerenciamento de Configuração em Máquinas Dinâmicas
**Pergunta resumida**: Qual modelo evita tráfego de rede excessivo e mantém credenciais seguras em VMs efêmeras?

### Resposta
**E – Modelo pull‑based (agente‑baseado)**

### Por que?
- O **agente** na VM executa **pull** de sua configuração, buscando apenas o que precisa.
- Reduz o **overhead de rede**: o servidor central não precisa push‑ar a cada janela de operação.
- **Credenciais locais**: o agente pode usar credenciais gerenciadas pela nuvem (IAM, Secrets Manager) sem expô‑las no servidor.
- Compatível com **stateful** e **stateless** VMs, pois a criação de um novo nó implica apenas iniciar o agente.

---

## Questão 3 – Idempotência da IaC
**Pergunta resumida**: Por que a execução de IaC não duplica recursos já criados, enquanto o Bash faz?

### Resposta
**C – Idempotência**

### Por que?
- **IaC declarativa** descreve *estado esperado*, não *procedimentos*. O provedor consulta o estado real e ajusta‑se.
- **Terraform & outros** mantêm um arquivo de *state*, comparando antes e depois da aplicação.
- **Bash** descreve uma sequência; se falha no meio, a reexecução tenta **recriar** tudo.
- Idempotência garante que a mesma execução múltiplas vezes converte todo o ambiente no mesmo estado final.

---

## Questão 4 – Lead Time, Process Time e Eficiência do Ciclo
**Pergunta resumida**: Calcular Lead Time, Process Time e ECE.

### Resposta
- **Lead Time** = 33 dias
- **Process Time** = 18 dias
- **ECE** = 54.55 %

### Por que?
| Item | Cálculo | Resultado |
|---|---|---|
| Process Time | 2 + 10 + 5 + 1 | 18 |
| Waiting Time | 1 + 3 + 4 + 7 | 15 |
| Lead Time | PT + WT | 33 |
| ECE | PT / LT × 100 | 54.55 % |

---

## Questão 5 – Benefício do SAST no Build
**Pergunta resumida**: Qual vantagem se o SAST roda na fase de *build*?

### Resposta
**D – Detecção precoce**

### Por que?
- Shift‑left: identifica bugs de segurança _antes_ de gerar artefatos.
- **Custo**: correções próximas à origem (código) custam menos.
- Evita que falhas se propagem para produção.
- Diferencia de *Runtime* (DAST, IAST) que vêm mais tarde.

---

## Questão 6 – Rastreabilidade na Auditoria PCI‑DSS
**Pergunta resumida**: O que garante rastreabilidade total?

### Resposta
**E – Automação e orquestração de ferramentas que pertençam a um grafo de dependências auditável**

### Por que?
- Conecta *commit → PR → build → artifact → deploy* de forma **imutável**.
- Ferramentas como *git*, *GitHub Actions*, *JFrog Artifactory*, *Kubernetes*, *OPA*, *HashiCorp Sentinel* podem registrar eventos.
- Sem essa ligação automática, rastrear a origem de um componente tornou‑se impraticável.

---

## Questão 7 – Manual Gate de Aprovação
**Pergunta resumida**: O que a existência de um gate manual indica?

### Resposta
**D – Entrega Contínua (Continuous Delivery)**

### Por que?
- Software pode ser **built & tested** automaticamente.
- A decisão final de **deploy** requer **ritual humano** → CD.
- Se o deploy fosse automático, teríamos **Continuous Deployment**.

---

## Questão 8 – GitHub Actions Workflow
**Pergunta resumida**: Como *jobs*, *steps* e artefatos se relacionam?

```yaml
name: CI/CD Pipeline de Testes Paralelos
on:
  push:
    branches:
      - main
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v3

      - name: Setup Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '16'

      - name: Install dependencies and build
        run: |
          npm install
          npm run build

      - name: Upload build artifact
        uses: actions/upload-artifact@v3
        with:
          name: build-output
          path: dist/

  test:
    needs: build
    runs-on: ${{ matrix.os }}
    strategy:
      matrix:
        os:
          - ubuntu-latest
          - windows-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v3

      - name: Download build artifact
        uses: actions/download-artifact@v3
        with:
          name: build-output
          path: dist/

      - name: Setup Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '16'

      - name: Install dependencies
        run: npm install

      - name: Run tests
        run: npm test
```

### Resposta
**C – Build antes de Test, instâncias paralelas no test**

### Por que?
- `needs: build` força *build* a terminar.
- Ação de upload/download de artefato garante persistência entre jobs.
- `matrix` replica `test` em runners distintos (Linux/Windows) em paralelo.
- Steps dentro de cada job são **sequenciais**.

---

## Questão 9 – Completar o Texto CALMS
**Pergunta resumida**: Qual sequência preenche corretamente?

### Resposta
**A – Mensuração – dados – monitoramento – observabilidade – confiáveis**

### Por que?
- **Mensuração** é o pilar do CALMS.
- *dados* são coletados continuamente.
- *monitoramento* garante observação dos sistemas.
- *observabilidade* agrega logs, métricas e traces.
- Métricas precisam ser *confiáveis* e acessíveis.

---

## Resumo das Respostas
1. **D** Trunk‑Based Development
2. **E** Pull‑based (agente‑baseado)
3. **C** Idempotência
4. Lead Time = 33 d; Process = 18 d; ECE ≈ 54.55 %
5. **D** Detecção precoce
6. **E** Automação e orquestração
7. **D** Entrega Contínua
8. **C** Build precede Test, parallel test jobs
9. **A** Mensuração – dados – monitoramento – observabilidade – confiáveis

---

> Este documento deve ser usado como apoio de revisão. Recomenda‑se revisitar cada tópico e verificar exemplos práticos em projetos de código‑aberto ou nas ferramentas que a sua organização utiliza.

