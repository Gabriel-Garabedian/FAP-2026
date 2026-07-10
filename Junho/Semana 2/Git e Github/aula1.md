# Introdução ao Git e GitHub

## Objetivo da Aula

Aprender os conceitos fundamentais de Git e GitHub, entendendo como funcionam o controle de versão, o armazenamento de projetos e o fluxo básico utilizado por desenvolvedores para registrar e compartilhar código.

---

## O que é Git?

O **Git** é um sistema de controle de versão distribuído que permite:

* Registrar alterações em arquivos.
* Recuperar versões anteriores de um projeto.
* Trabalhar em equipe sem sobrescrever o trabalho de outras pessoas.
* Manter um histórico completo das modificações realizadas.

---

## O que é GitHub?

O **GitHub** é uma plataforma online que utiliza o Git para armazenar repositórios na nuvem.

Com ele é possível:

* Hospedar projetos.
* Compartilhar código.
* Colaborar com outros desenvolvedores.
* Criar portfólios profissionais.
* Documentar projetos através do README.

---

## Configuração Inicial do Git

Após instalar o Git, é necessário configurar a identidade do usuário:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@email.com"
```

Verificar as configurações:

```bash
git config --global --list
```

---

## Token de Acesso

O GitHub utiliza tokens para autenticação em vez de senhas.

O token funciona como uma chave de acesso segura para:

* Fazer push.
* Fazer pull.
* Clonar repositórios privados.
* Automatizar processos.

 Nunca compartilhe seu token.

---

## Repositórios

Um repositório é o local onde ficam armazenados:

* Arquivos do projeto.
* Histórico de versões.
* Documentação.
* Configurações.

Boas práticas:

* Utilizar nomes claros.
* Adicionar README.md desde a criação.
* Manter documentação atualizada.

---

## Fluxo Básico do Git

### Clonar um repositório

```bash
git clone URL_DO_REPOSITORIO
```

### Entrar na pasta do projeto

```bash
cd nome-do-repositorio
```

### Verificar alterações

```bash
git status
```

### Adicionar arquivos

```bash
git add arquivo.txt
```

ou

```bash
git add .
```

### Criar um commit

```bash
git commit -m "Descrição da alteração"
```

### Enviar para o GitHub

```bash
git push
```

---

## Conceitos Importantes

### Commit

Um commit é uma "fotografia" do projeto em um determinado momento.

Cada commit possui:

* Autor.
* Data.
* Mensagem descritiva.
* Histórico permanente.

Exemplo:

```bash
git commit -m "Adiciona documentação inicial"
```

---

### README.md

O README é o cartão de visitas do projeto.

Pode conter:

* Descrição.
* Tecnologias utilizadas.
* Instruções de instalação.
* Imagens.
* Exemplos de uso.

Projetos com README bem elaborado demonstram profissionalismo.

---

### GitHub como Portfólio

Além de armazenar código, o GitHub permite:

* Mostrar projetos para recrutadores.
* Demonstrar evolução técnica.
* Organizar estudos.
* Hospedar sites com GitHub Pages.

---

## Próximos Conceitos Apresentados

A professora também citou tópicos que serão aprofundados posteriormente:

* Branches
* Merge
* Pull Requests
* Resolução de conflitos
* Code Review
* Colaboração em equipe

Essas práticas fazem parte do fluxo utilizado por empresas de tecnologia.

---

## Conclusão

Git e GitHub são ferramentas essenciais para qualquer desenvolvedor. Elas permitem versionar projetos, colaborar com equipes, manter documentação organizada e construir um portfólio profissional. Dominar o fluxo básico de clone, add, commit e push é o primeiro passo para trabalhar com desenvolvimento de software em ambientes reais. 🚀

---

### Principais comandos da aula

```bash
git config --global user.name "Seu Nome"
git config --global user.email "Seu Email"

git clone URL do repositorio
cd projeto

git status
git add .
git commit -m "Mensagem"
git push
```

