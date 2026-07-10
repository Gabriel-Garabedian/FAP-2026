# 📚 - Branches, Merge e Conflitos

## 🎯 Objetivo

Aprender a desenvolver funcionalidades isoladas sem afetar a versão principal do sistema.

---

## 🧠 O que é uma Branch?

Uma branch é uma linha paralela de desenvolvimento.

Permite criar funcionalidades sem modificar diretamente a `main`.

---

## 🏢 Por que empresas usam Branches?

- Organização
- Segurança
- Trabalho em equipe
- Desenvolvimento paralelo

---

## 💻 Comandos

### Criar e trocar para uma branch

```bash
git switch -c feature-login
```

### Trocar de branch

```bash
git switch main
```
### Para ver TODAS as branches (as locais e as remotas juntas)

```bash
git branch -a
```

### Fazer merge

```bash
git merge feature-login
```
Une as alterações da branch na branch atual.

### Se for a primeira vez enviando essa branch para o GitHub, geralmente use:
```bash
git push -u origin feature-login
```
cria o vínculo entre a branch local e a remota.
---

## 🌳 Padrão de Nomes

✅ Bom:

```text
feature-login
feature-pagamento
feature-recuperacao-senha
```

❌ Ruim:

```text
teste
coisas
branch-nova
```

---

## ⚠️ Conflitos

Acontecem quando duas branches modificam a mesma linha de formas diferentes.

Exemplo:

```java
<<<<<<< HEAD
String emailUsuario;
=======
String emailPrincipal;
>>>>>>> main
```

---

## 🔧 Como Resolver

1. Analisar o código.
2. Escolher a melhor solução.
3. Remover as marcações do Git.
4. Salvar o arquivo.
5. Fazer commit.

---

## ⚠️ Erros Comuns

- Trabalhar direto na `main`.
- Fazer merge sem atualizar a branch.
- Resolver conflitos sem entender o código.

---

## 📝 Resumo

- Branches isolam funcionalidades.
- Merge une alterações.
- Nem todo merge gera conflito.
- O Git nunca escolhe sozinho quando existe conflito.