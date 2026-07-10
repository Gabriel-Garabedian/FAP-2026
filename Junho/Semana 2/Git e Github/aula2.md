# 📚 GitHub, Branches e Pull Requests

## 🎯 Objetivo

Aprender a clonar repositórios, criar branches, registrar alterações e enviar contribuições para um repositório compartilhado.

---

## 🧠 Conceitos Aprendidos

### Repositório Central

Repositório principal utilizado pela equipe ou turma para armazenar e organizar os projetos.

### Branch

Linha paralela de desenvolvimento utilizada para trabalhar sem afetar a branch principal.

### Pull Request (PR)

Solicitação para que alterações de uma branch sejam analisadas e integradas ao projeto principal.

---

## 💻 Comandos Utilizados

### Clonar um repositório

```bash
git clone URL_DO_REPOSITORIO
```

Baixa uma cópia completa do projeto para o computador.

### Entrar na pasta do projeto

```bash
cd nome-do-projeto
```

### Criar e trocar para uma nova branch

```bash
git checkout -b atividade-semana-1
```

> Atualmente também pode ser usado:

```bash
git switch -c atividade-semana-1
```

### Adicionar arquivos

```bash
git add .
```

### Criar commit

```bash
git commit -m "Adiciona instruções da semana 1"
```

### Enviar alterações

```bash
git push
```

---

## 🔄 Fluxo da Aula

```text
Criar Repositório
↓
Git Clone
↓
Criar Branch
↓
Adicionar Arquivos
↓
Git Add
↓
Git Commit
↓
Git Push
↓
Pull Request
↓
Code Review
↓
Merge
```

---

## 🏢 Como Empresas Utilizam

- Existe um repositório central.
- Cada desenvolvedor cria sua própria branch.
- As alterações são enviadas através de Pull Requests.
- O código é revisado antes de chegar à branch principal.
- Todo o histórico fica registrado no GitHub.

---

## 📝 Resumo

- Aprendemos a clonar repositórios.
- Aprendemos a criar branches.
- Utilizamos `git add`, `git commit` e `git push`.
- Entendemos o conceito de Pull Request.
- Vimos como ocorre o processo de revisão e merge em equipes.