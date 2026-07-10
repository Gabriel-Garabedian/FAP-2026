# 📚 Conventional Commits

## 🎯 Objetivo

Padronizar mensagens de commit para que qualquer pessoa da equipe consiga entender rapidamente o que foi alterado.

---

## ✨ feat

Usado para adicionar uma nova funcionalidade.

### Exemplos

```bash
git commit -m "feat: adiciona recuperação de senha"
git commit -m "feat: implementa autenticação JWT"
git commit -m "feat: adiciona cadastro de alunos"
```

---

## 🐛 fix

Usado para corrigir bugs.

### Exemplos

```bash
git commit -m "fix: corrige erro no login"
git commit -m "fix: corrige validação de CPF"
git commit -m "fix: corrige cálculo de IMC"
```

---

## ♻️ refactor

Usado quando o código é reorganizado sem alterar o comportamento da aplicação.

### Exemplos

```bash
git commit -m "refactor: reorganiza LoginService"
git commit -m "refactor: simplifica validação de usuário"
git commit -m "refactor: separa regras de negócio em serviços"
```

---

## 📖 docs

Usado para alterações na documentação.

### Exemplos

```bash
git commit -m "docs: atualiza README"
git commit -m "docs: adiciona guia de instalação"
git commit -m "docs: documenta endpoints da API"
```

---

## 🧪 test

Usado para criação ou manutenção de testes.

### Exemplos

```bash
git commit -m "test: adiciona testes para LoginService"
git commit -m "test: corrige testes de autenticação"
```

---

## 🎨 style

Usado para ajustes de formatação e estilo do código.

### Exemplos

```bash
git commit -m "style: ajusta indentação"
git commit -m "style: organiza imports"
```

---

## ⚡ perf

Usado para melhorias de performance.

### Exemplos

```bash
git commit -m "perf: otimiza consulta de usuários"
git commit -m "perf: reduz consumo de memória"
```

---

## 🔧 chore

Usado para tarefas de manutenção e configuração do projeto.

### Exemplos

```bash
git commit -m "chore: atualiza dependências"
git commit -m "chore: configura pipeline CI"
git commit -m "chore: ajusta configuração do Docker"
```

---

## 📌 Boas Práticas

✅ Seja específico.

```bash
git commit -m "feat: adiciona recuperação de senha"
```

✅ Descreva o que foi feito.

```bash
git commit -m "fix: corrige erro de autenticação"
```

✅ Use verbos de ação.

```bash
git commit -m "docs: atualiza README"
```

---

## ❌ Evite

```bash
git commit -m "mudancas"
git commit -m "teste"
git commit -m "ajustes"
git commit -m "update"
```

Essas mensagens não explicam o que foi alterado.

---

## 📝 Resumo

| Prefixo | Uso |
|----------|----------|
| feat | Nova funcionalidade |
| fix | Correção de bug |
| refactor | Reorganização do código |
| docs | Documentação |
| test | Testes |
| style | Formatação |
| perf | Performance |
| chore | Manutenção e configuração |

Seguir esse padrão torna o histórico do projeto mais profissional, organizado e fácil de entender.
