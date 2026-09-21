# NEXUM — Roadmap

**Versão:** 0.1
**Projeto:** Próxima Fase! — Vortex 2026
**Período de desenvolvimento:** 01/10/2026 a 28/10/2026
**Apresentação:** 29/10/2026 e 30/10/2026

---

# 1. Objetivo do roadmap

Este documento organiza o desenvolvimento de **NEXUM** ao longo dos 28 dias do programa.

A prioridade é garantir que:

1. o jogo exista cedo;
2. o core loop funcione cedo;
3. o conteúdo seja validado antes do polish;
4. a última semana seja protegida;
5. a apresentação dependa de uma build estável.

O roadmap não representa uma lista fixa de funcionalidades.

Ele representa uma sequência de **metas de produção**.

---

# 2. Resumo das quatro semanas

## Semana 1 — O jogo existe

**01/10 a 07/10**

Meta:

> Construir o primeiro atendimento jogável em graybox.

---

## Semana 2 — O jogo funciona

**08/10 a 14/10**

Meta:

> Completar e validar o core loop do PoC.

---

## Semana 3 — O jogo parece um jogo

**15/10 a 21/10**

Meta:

> Transformar o protótipo funcional em uma experiência apresentável.

---

## Semana 4 — O jogo está apresentável

**22/10 a 28/10**

Meta:

> Estabilizar, testar, polir e preparar a apresentação.

---

# 3. Semana 1 — O jogo existe

**Período:** 01/10 a 07/10

## Objetivo

Construir uma versão feia, simples e jogável do atendimento.

Ao final da semana, deve ser possível iniciar o jogo e concluir um atendimento básico.

Arte final não é prioridade.

---

## Entregas principais

### Projeto

* criar o projeto Godot;
* configurar estrutura de pastas;
* configurar Git e GitHub;
* definir branch principal de desenvolvimento;
* configurar GitHub Projects;
* criar primeiras Issues.

---

### Estrutura de dados

Criar uma estrutura inicial para representar:

* paciente;
* perguntas;
* respostas;
* evidências;
* exames;
* diagnósticos;
* tratamentos;
* consequências.

A estrutura deve permitir expansão futura para investigação científica.

---

### Atendimento graybox

Implementar o fluxo mínimo:

```text
INÍCIO
↓
PACIENTE
↓
DIÁLOGO
↓
EXAME
↓
PRONTUÁRIO
↓
DIAGNÓSTICO
↓
TRATAMENTO
↓
PREVENÇÃO
↓
CONSEQUÊNCIA
↓
FIM
```

---

## Conteúdo da primeira versão

Utilizar apenas:

* 1 paciente;
* 3 perguntas;
* 2 verificações clínicas;
* 1 exame complementar;
* 2 diagnósticos;
* 2 tratamentos;
* 1 decisão preventiva;
* 1 consequência;
* 1 evidência científica.

---

## O que não fazer nesta semana

Evitar:

* arte final extensa;
* investigação científica completa;
* laboratório completo;
* múltiplos pacientes;
* animações complexas;
* sistema de recursos;
* reabilitação;
* exploração do hospital.

---

## Gate da Semana 1

A semana será considerada concluída quando alguém que não programou o sistema conseguir:

1. iniciar o jogo;
2. atender o paciente;
3. realizar escolhas;
4. chegar ao fim do atendimento.

---

# 4. Semana 2 — O jogo funciona

**Período:** 08/10 a 14/10

## Objetivo

Validar o core loop.

A prioridade muda de:

> “conseguimos implementar?”

para:

> “isso funciona como jogo?”

---

## Entregas principais

### Melhorar o atendimento

Revisar:

* clareza dos diálogos;
* fluxo da anamnese;
* apresentação das evidências;
* prontuário;
* exames;
* diagnóstico;
* tratamento;
* prevenção;
* consequência.

---

### Consequências

Garantir que as escolhas tenham algum impacto perceptível.

O jogador deve compreender que suas decisões alteraram o resultado.

---

### Saúde

Verificar se o PoC demonstra claramente:

* prevenção;
* diagnóstico;
* tratamento.

A saúde não pode depender apenas da explicação verbal da equipe.

Ela deve aparecer durante a gameplay.

---

### Pesquisa

Implementar apenas a conexão mínima entre atendimento e ciência.

Exemplo:

```text
ATENDIMENTO
↓
EVIDÊNCIA COLETADA
↓
DADO SOBRE A NEXUM
```

Caso seja simples e seguro, poderá existir uma primeira descoberta P1.

---

### Conteúdo adicional

Somente após o primeiro paciente estar validado, avaliar a inclusão de:

* segundo paciente;
* terceiro paciente;
* pequena variação de caso.

Adicionar conteúdo apenas se ele demonstrar uma nova decisão ou consequência.

---

## Primeiro playtest

Realizar o primeiro playtest com alguém de fora da equipe.

Não explicar inicialmente.

Observar se a pessoa entende:

* quem ela é;
* o objetivo;
* como conversar;
* como consultar informações;
* como diagnosticar;
* como escolher tratamento;
* como terminar o atendimento.

---

## Registro do playtest

Registrar:

```text
PROBLEMA
↓
EVIDÊNCIA
↓
PRIORIDADE
↓
MUDANÇA
```

---

## Gate da Semana 2

Ao final da semana, o jogo deverá possuir:

* core loop completo;
* pelo menos um atendimento funcional;
* consequências claras;
* primeiro playtest realizado;
* principais problemas identificados;
* build funcional.

Nenhum sistema crítico do P0 deverá estar apenas planejado.

---

# 5. Semana 3 — O jogo parece um jogo

**Período:** 15/10 a 21/10

## Objetivo

Melhorar apresentação, leitura e sensação de jogo sem alterar o core loop.

---

## Arte

Substituir placeholders prioritários.

Budget inicial:

### Personagens

* protagonista, se visível;
* pacientes essenciais.

### Animações

Apenas as necessárias.

Exemplos:

* idle;
* entrada;
* pequena reação.

### Ambiente

Priorizar:

* sala de atendimento;
* elementos médicos essenciais;
* identidade visual da Nexum.

Não criar múltiplos ambientes apenas por variedade.

---

## UI

Melhorar:

* diálogo;
* prontuário;
* seleção de exame;
* diagnóstico;
* tratamento;
* orientação;
* resultado.

Priorizar:

**clareza > decoração.**

---

## Áudio

Adicionar feedback mínimo para:

* botões;
* nova evidência;
* resultado;
* consequência.

Depois:

* ambiente;
* música, se houver disponibilidade.

---

## Feedback

O jogador deverá perceber claramente quando:

* descobriu algo;
* realizou um exame;
* adicionou informação ao prontuário;
* tomou uma decisão;
* terminou o atendimento;
* obteve uma evidência sobre a Nexum.

---

## Balanceamento

Revisar:

* quantidade de texto;
* duração dos atendimentos;
* quantidade de perguntas;
* dificuldade;
* excesso de informações;
* clareza das opções.

Meta aproximada:

**2 a 4 minutos por atendimento no PoC.**

---

## Segundo playtest

Realizar um novo teste com a versão visual.

Observar especialmente:

* compreensão do objetivo;
* ritmo;
* leitura;
* excesso de texto;
* decisões pouco claras;
* feedback.

---

## Gate da Semana 3

Ao final da semana:

* o jogo deve parecer intencional;
* a interface deve estar compreensível;
* placeholders principais devem ter sido reduzidos;
* feedback básico deve existir;
* áudio essencial deve funcionar;
* a build deve continuar estável.

---

# 6. Semana 4 — O jogo está apresentável

**Período:** 22/10 a 28/10

## Regra principal

> Não iniciar sistema crítico novo.

---

## Objetivo

Transformar a versão atual em uma build segura para apresentação.

---

## Prioridade 1 — Bugs

Classificar bugs em:

### Bloqueante

Impede concluir o jogo.

Corrigir imediatamente.

### Grave

Prejudica claramente a experiência ou apresentação.

Alta prioridade.

### Médio

Problema perceptível, mas não impede demonstração.

Corrigir se houver tempo.

### Baixo

Detalhe visual ou pequeno inconveniente.

Pode permanecer.

---

## Prioridade 2 — Build

Testar exportações regularmente.

Preparar a versão utilizada na apresentação antes do dia 28.

Testar em máquina diferente sempre que possível.

---

## Prioridade 3 — Polish

Melhorar apenas pontos seguros.

Exemplos:

* transições;
* sons;
* feedback;
* pequenos efeitos;
* ajustes de texto;
* pequenas animações.

Não adicionar mecânica nova apenas para parecer que houve mais produção.

---

## Prioridade 4 — Playtest final

Realizar playtest sem auxílio da equipe.

Validar:

* objetivo;
* controles;
* atendimento;
* diagnóstico;
* tratamento;
* prevenção;
* consequência.

---

## Prioridade 5 — Documentação

Atualizar:

* README;
* GDD;
* SCOPE;
* ROADMAP;
* decisões;
* informações do projeto.

A documentação final deve representar o jogo realmente implementado.

---

## Prioridade 6 — Apresentação

Preparar:

* pitch;
* slides;
* roteiro;
* demonstração;
* respostas para perguntas;
* plano de contingência.

---

## Gate da Semana 4

Antes do encerramento do dia 28:

* build final disponível;
* demonstração testada;
* bugs bloqueantes resolvidos;
* documentação atualizada;
* slides finalizados;
* pitch ensaiado;
* backup da build preparado.

---

# 7. Apresentação — 29/10 e 30/10

Tempo previsto:

**15 minutos.**

Estrutura inicial:

## 1 minuto — Problema e contexto

Apresentar rapidamente:

* mundo;
* Nexum;
* crise;
* papel do jogador.

---

## 2 minutos — Conceito

Explicar:

* médico + cientista;
* proposta;
* saúde como mecânica.

---

## 2 minutos — Design

Apresentar:

```text
INVESTIGAR
↓
DIAGNOSTICAR
↓
TRATAR
↓
PREVENIR
↓
APRENDER
```

---

## 5 minutos — Gameplay

Prioridade máxima.

Demonstrar o jogo funcionando.

---

## 2 minutos — Desenvolvimento

Mostrar:

* Godot;
* Pixel Art;
* organização da equipe;
* processo de validação.

---

## 1 minuto — Resultados

Explicar:

* o que foi validado;
* principais aprendizados;
* feedback de playtests.

---

## 1 minuto — Expansão

Apresentar como visão futura:

* investigação científica;
* reabilitação;
* saúde pública;
* novos pacientes;
* progressão do conhecimento.

---

## 1 minuto — Encerramento

Reforçar a proposta central de NEXUM.

---

# 8. Divisão inicial de responsabilidades

A divisão poderá mudar conforme a produção.

## Rodrigo

Foco principal:

* programação;
* arquitetura;
* core loop;
* Game Design;
* integração;
* revisão técnica.

---

## Daniel

Foco principal:

* programação;
* Pixel Art;
* áudio;
* suporte ao Game Design.

---

## Gustavo

Foco principal:

* programação;
* UI;
* implementação de interfaces;
* suporte ao Game Design.

---

# 9. Capacidade da equipe

Disponibilidade estimada:

```text
Rodrigo: 7h/semana
Daniel: 7h/semana
Gustavo: 7h/semana
```

Capacidade aproximada:

```text
21 horas por semana
```

Porém, essa capacidade inclui:

* reuniões;
* revisão;
* testes;
* integração;
* correções;
* Git;
* documentação.

Não planejar 21 horas de novas funcionalidades por semana.

---

# 10. Daily

A Daily deverá ser curta.

Formato:

```text
Ontem:
Hoje:
Bloqueio:
```

Não transformar a Daily em reunião de solução técnica extensa.

Problemas maiores deverão ser discutidos separadamente.

---

# 11. Sprint Review

Ao final de cada semana, comparar:

```text
PLANEJADO

x

ENTREGUE
```

Perguntas:

* o que foi concluído?
* o que não foi?
* por quê?
* existe bloqueio?
* alguma tarefa foi subestimada?
* precisamos cortar escopo?
* o core loop continua protegido?

---

# 12. Ordem de reação a atrasos

Caso uma semana atrase:

```text
1. remover P2
↓
2. remover P1
↓
3. reduzir conteúdo
↓
4. simplificar P0
↓
5. preservar o core loop
```

Não tentar compensar atraso adicionando trabalho simultaneamente para todos.

---

# 13. Builds

Realizar builds durante o desenvolvimento.

Meta mínima:

### Semana 1

Primeira build funcional.

### Semana 2

Build após validação do core loop.

### Semana 3

Build com apresentação visual.

### Semana 4

Build candidata à apresentação.

Não esperar o dia 28 para testar exportação.

---

# 14. Milestones sugeridos no GitHub

## M0 — Setup

Projeto, repositório e estrutura inicial.

---

## M1 — Graybox

Primeiro atendimento completo.

---

## M2 — Core Loop

Atendimento validado e consequências funcionando.

---

## M3 — Presentation Ready

Arte, UI, áudio e polish.

---

## M4 — Final Build

Correções, testes e versão de apresentação.

---

# 15. Critério final

O roadmap será considerado bem-sucedido se no dia 28 existir uma versão do jogo que a equipe consiga abrir e demonstrar sem precisar explicar falhas da implementação.

A prioridade final não é:

> “quantas funcionalidades conseguimos adicionar?”

A prioridade é:

> **“a ideia de NEXUM está clara, funciona e conseguimos demonstrá-la com confiança?”**
