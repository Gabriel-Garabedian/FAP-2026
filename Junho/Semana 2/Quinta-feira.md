# 📅 Diário de Aprendizado - FAP

> 📅 **Aulas:** Terças e Quintas  

---

## Semana x (16/06/2026 - 18/06/2026)

### Quinta-feira (18/06/2026) - 🎓 Aula 2
**Status:** ✅ Concluído  
**Tempo:** 3 horas (aula presencial)  
**Conteúdo:** 

**O que aprendi:**
```text
Hoje aprendi o fluxo básico de contribuição em projetos colaborativos utilizando Git e GitHub.

Durante a atividade, realizei um Fork de um repositório para minha conta do GitHub, criei uma nova branch para desenvolver minhas alterações de forma isolada, adicionei um arquivo NOME.json na pasta alunos e registrei as mudanças utilizando Git.

Após concluir as modificações, enviei as alterações para meu repositório remoto e abri um Pull Request (PR) solicitando a integração das mudanças ao repositório original. O próximo passo é aguardar a revisão e o Merge por parte do professor.
```
---
**Dificuldades:**
```text
Ao tentar enviar as alterações para o repositório remoto utilizando git push, ocorreu um erro informando que a branch atual não possuía uma branch remota configurada (upstream).

Solução: Foi necessário executar o comando abaixo para definir a branch remota de acompanhamento:
```

```bash
git push -u origin nome-da-branch
```
```text
Após a configuração inicial do upstream, os próximos envios puderam ser realizados normalmente utilizando apenas:
```
```bash
git push
```
---
