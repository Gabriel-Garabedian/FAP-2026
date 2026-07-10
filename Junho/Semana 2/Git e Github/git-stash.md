# 📚 Módulo 6 - Git Stash

## 🎯 Objetivo

Aprender a guardar alterações temporariamente sem criar commits.

---

## 🧠 O que é Git Stash?

Git Stash funciona como uma gaveta temporária.

Permite guardar alterações e recuperá-las depois.

---

## 💻 Comandos

### Guardar alterações

```bash
git stash
```

### Listar stashes

```bash
git stash list
```

### Recuperar alterações

```bash
git stash pop
```

---

## 🏢 Exemplo Real

Você está trabalhando em:

```text
feature-pagamento
```

Surge um bug urgente.

Fluxo:

```text
git stash
↓
Troca de branch
↓
Corrige bug
↓
Volta para feature
↓
git stash pop
```

---

## ⚠️ Erros Comuns

- Esquecer que existe um stash salvo.
- Confundir stash com commit.
- Usar stash para guardar código por vários dias.

---

## 📝 Resumo

- Stash guarda alterações temporariamente.
- Não cria commit.
- Muito útil para interrupções inesperadas.