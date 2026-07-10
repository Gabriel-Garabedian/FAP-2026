# 📚 - Git Rebase

## 🎯 Objetivo

Aprender a atualizar uma branch com as alterações mais recentes da `main` sem criar commits extras de merge, mantendo o histórico mais limpo e organizado.

---

## 🧠 O que é Git Rebase?

Git Rebase é um comando que reaplica os commits da sua branch sobre outra branch, normalmente a `main`.

Ele permite atualizar sua branch com as mudanças mais recentes do projeto.

---

## ⚖️ Rebase x Merge

### Merge

```text
main
├─ A
├─ B
├─ E
├─ F
│
└─ Merge Commit
   │
feature-login
├─ C
├─ D
```

- Cria um commit extra de merge.
- Mantém o histórico original.

### Rebase

```text
main
├─ A
├─ B
├─ E
├─ F
│
└─ C'
   └─ D'
```

- Não cria commit de merge.
- Reorganiza os commits para um histórico linear.

---

## 🏢 Quando Empresas Utilizam?

O Rebase é muito utilizado:

- Antes de abrir um Pull Request.
- Para atualizar uma feature branch.
- Para manter o histórico limpo.
- Em equipes que seguem boas práticas de Git.

---

## 💻 Comandos

### Atualizar a Main

```bash
git switch main
git pull
```

Atualiza a branch principal com as alterações mais recentes do GitHub.

---

### Voltar para sua Branch

```bash
git switch feature-login
```

---

### Executar o Rebase

```bash
git rebase main
```

Reaplica os commits da sua branch sobre a versão mais recente da `main`.

---

## ⚠️ Conflitos Durante o Rebase

Assim como no Merge, conflitos podem acontecer.

Exemplo:

```java
main:
String emailPrincipal;
```

```java
feature-login:
String emailUsuario;
```

O Git não sabe qual versão manter e solicita intervenção do desenvolvedor.

---

## 🔧 Resolver Conflitos

Após corrigir os arquivos:

```bash
git add .
```

```bash
git rebase --continue
```

O Git continua o processo de rebase.

---

## 🧠 Analogia Simples

Imagine que você escreveu uma redação.

Enquanto isso, outras pessoas adicionaram novos parágrafos antes do seu texto.

### Merge

Você adiciona uma página explicando onde os textos foram unidos.

### Rebase

Você reescreve sua redação como se tivesse começado depois das alterações dos outros.

O resultado fica mais organizado.

---

## ⚠️ Boas Práticas

✅ Fazer rebase em branches pessoais.

✅ Fazer rebase antes de abrir Pull Requests.

✅ Atualizar a `main` antes de iniciar o rebase.

❌ Fazer rebase em branches compartilhadas por várias pessoas.

❌ Fazer rebase sem entender os conflitos.

---

## 🔄 Fluxo Profissional

```text
git switch main
↓
git pull
↓
git switch feature-login
↓
git rebase main
↓
Resolver conflitos (se necessário)
↓
git push
↓
Pull Request
```

---

## 📝 Resumo

- Rebase atualiza uma branch usando outra branch como base.
- Mantém o histórico mais limpo que o Merge.
- Pode gerar conflitos.
- É muito utilizado antes de Pull Requests.
- Não substitui Merge, mas complementa o fluxo de trabalho.