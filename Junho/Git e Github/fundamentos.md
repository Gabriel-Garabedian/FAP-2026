# 📚- Fundamentos do Git

## 🎯 Objetivo

Entender o que é Git, GitHub e os primeiros comandos utilizados no controle de versão.

---

## 🧠 O que é Git?

Git é um sistema de controle de versão que registra alterações em arquivos ao longo do tempo.

Com ele é possível:

- Recuperar versões antigas.
- Trabalhar em equipe.
- Rastrear alterações.
- Evitar perda de código.

---

## 🌐 O que é GitHub?

GitHub é uma plataforma que hospeda repositórios Git na nuvem.

Permite:

- Compartilhar projetos.
- Trabalhar em equipe.
- Armazenar código online.

---

## ⚖️ Git x GitHub

| Git | GitHub |
|------|------|
| Ferramenta local | Plataforma online |
| Controla versões | Hospeda repositórios |
| Funciona sem internet | Depende da internet |

---

## 💻 Comandos

### Inicializar repositório

```bash
git init
```

Cria a pasta oculta `.git`, responsável por armazenar o histórico do projeto.

### Verificar status

```bash
git status
```

Mostra:

- Arquivos modificados
- Arquivos preparados para commit
- Arquivos não rastreados

### Adicionar arquivos

```bash
git add .
```

Prepara arquivos para o próximo commit.

### Criar commit

```bash
git commit -m "Cria classe Usuario"
```

Registra as alterações no histórico do Git.

---

## ⚠️ Erros Comuns

- Pensar que `git add` envia código para o GitHub.
- Pensar que `git commit` envia código para o GitHub.
- Usar mensagens de commit genéricas.

❌ Ruim:

```bash
git commit -m "mudancas"
```

✅ Bom:

```bash
git commit -m "Adiciona autenticação por email"
```

---

## 📝 Resumo

- Git controla versões.
- GitHub hospeda projetos.
- `git init` cria um repositório.
- `git status` mostra o estado do projeto.
- `git add` prepara arquivos.
- `git commit` salva alterações localmente.