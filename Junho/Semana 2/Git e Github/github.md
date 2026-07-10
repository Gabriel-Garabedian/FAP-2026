# 📚 - Git e GitHub

## 🎯 Objetivo

Aprender a conectar o Git local ao GitHub e sincronizar alterações entre o computador e o repositório remoto.

---

## 🧠 Conceitos

### Repositório Local

É o projeto armazenado no seu computador.

### Repositório Remoto

É o projeto hospedado no GitHub.

---

## 💻 Comandos

### Clonar um repositório

```bash
git clone URL_DO_REPOSITORIO
```

Baixa uma cópia completa do projeto para o computador.

### Atualizar projeto

```bash
git pull
```

Baixa as alterações mais recentes do GitHub.

### Enviar alterações

```bash
git push
```

Envia commits locais para o GitHub.

---

## 🔄 Fluxo Básico

```text
Alterar código
↓
git add .
↓
git commit -m "Descrição"
↓
git push
```

---

## ⚠️ Erros Comuns

- Achar que commit envia código para o GitHub.
- Esquecer de fazer pull antes de começar a programar.
- Fazer push sem revisar as alterações.

---

## 🏢 Como Empresas Utilizam

Fluxo comum:

```text
git pull
↓
Desenvolvimento
↓
git add
↓
git commit
↓
git push
```

Sempre atualize seu projeto antes de começar uma tarefa.

---

## 📝 Resumo

- `git clone` baixa projetos.
- `git pull` atualiza o projeto local.
- `git push` envia alterações para o GitHub.
- Commit não envia código para a nuvem.