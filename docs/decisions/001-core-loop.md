# ADR 001 — Core Loop: Médico + Cientista

**Status:** Aprovado
**Data:** 21/09/2026
**Projeto:** NEXUM
**Tipo:** Decisão de Game Design

---

# 1. Contexto

NEXUM é um jogo 2D Pixel Art desenvolvido para o programa Próxima Fase! — Vortex, dentro da temática Saúde.

A proposta narrativa coloca o jogador no papel de um profissional que atua simultaneamente como:

* médico;
* cientista;
* pesquisador.

O mundo do jogo passou décadas acreditando que as doenças haviam sido eliminadas.

Com o surgimento da NEX-20, conhecida como Nexum, poucos profissionais ainda possuem conhecimento suficiente para atuar na área médica.

Era necessário definir qual dessas funções deveria formar o núcleo da gameplay.

---

# 2. Alternativas consideradas

## Alternativa A — Foco em atendimento médico

O jogo seria concentrado em:

* conversar com pacientes;
* identificar sintomas;
* realizar exames;
* diagnosticar;
* tratar;
* acompanhar consequências.

### Vantagens

* escopo menor;
* fácil compreensão;
* forte relação com Saúde;
* menor risco técnico.

### Desvantagens

* utiliza apenas parte da fantasia do protagonista;
* ciência teria papel predominantemente narrativo;
* menor diferenciação entre atendimentos ao longo do jogo.

---

## Alternativa B — Foco em investigação científica

O jogo seria concentrado em:

* analisar amostras;
* comparar dados;
* identificar padrões;
* formular hipóteses;
* realizar experimentos;
* compreender a Nexum.

### Vantagens

* forte identidade científica;
* boas possibilidades de puzzle;
* permite progressão através de conhecimento.

### Desvantagens

* menor contato com pacientes;
* prevenção, diagnóstico e tratamento ficam menos presentes;
* maior dificuldade para demonstrar diferentes áreas da Saúde.

---

## Alternativa C — Médico + Cientista

O jogador alterna entre:

**cuidar dos pacientes**

e

**usar as informações desses atendimentos para compreender a Nexum.**

Os dois sistemas devem se alimentar.

---

# 3. Decisão

A equipe decidiu seguir a:

> **Alternativa C — Médico + Cientista**

O core loop completo planejado para NEXUM será:

```text
PACIENTE
↓
ANAMNESE
↓
EXAMES
↓
EVIDÊNCIAS
↓
DIAGNÓSTICO
↓
TRATAMENTO
↓
PREVENÇÃO
↓
CONSEQUÊNCIA
↓
DADOS / AMOSTRAS
↓
INVESTIGAÇÃO CIENTÍFICA
↓
DESCOBERTA
↓
NOVO CONHECIMENTO
↓
NOVO ATENDIMENTO
```

---

# 4. Princípio central

Os dois lados do jogo não devem funcionar como sistemas independentes.

A regra será:

> **Os atendimentos alimentam a pesquisa, e a pesquisa modifica os próximos atendimentos.**

Exemplo:

```text
Paciente
↓
Evidência encontrada
↓
Pesquisa
↓
Descoberta
↓
Novo exame disponível
↓
Próximo paciente
```

Uma descoberta científica também poderá futuramente liberar:

* novas perguntas;
* novas interpretações;
* novos exames;
* novas formas de tratamento;
* novas medidas preventivas.

---

# 5. Experiência desejada

O jogador deve perceber que não conhece todas as respostas desde o início.

Durante o jogo, a experiência desejada é:

```text
NÃO SEI
↓
OBSERVO
↓
INVESTIGO
↓
FORMULO UMA HIPÓTESE
↓
TOMO UMA DECISÃO
↓
VEJO A CONSEQUÊNCIA
↓
APRENDO
```

O conhecimento adquirido passa a fazer parte da progressão do jogador.

---

# 6. Papel da Saúde

A decisão Médico + Cientista permite trabalhar diretamente com diferentes áreas da temática Saúde.

## Prevenção

O jogador poderá orientar pacientes e utilizar descobertas científicas para reduzir riscos.

## Diagnóstico

O jogador deverá reunir e interpretar evidências.

## Tratamento

O jogador deverá escolher condutas com base nas informações disponíveis.

## Acompanhamento

Pacientes poderão retornar e demonstrar consequências de decisões anteriores.

## Reabilitação

Planejada para expansão futura.

## Pesquisa

Os dados dos atendimentos contribuirão para compreender a Nexum.

---

# 7. Escopo do PoC

A decisão pelo modelo Médico + Cientista **não significa que todos os sistemas serão implementados imediatamente**.

O primeiro graybox deverá validar principalmente:

```text
PACIENTE
↓
INVESTIGAÇÃO CLÍNICA
↓
DIAGNÓSTICO
↓
TRATAMENTO
↓
PREVENÇÃO
↓
CONSEQUÊNCIA
↓
EVIDÊNCIA CIENTÍFICA
```

A gameplay completa de investigação científica será desenvolvida apenas após a validação do atendimento.

---

# 8. Investigação científica no primeiro PoC

No primeiro momento, a pesquisa poderá ser representada apenas através de:

* coleta de evidências;
* registro de dados;
* obtenção de amostras;
* descoberta simples;
* mensagem de progressão científica.

Exemplo:

```text
ATENDIMENTO CONCLUÍDO

Nova evidência obtida:
Padrão X observado na Nexum.
```

Isso já demonstra a relação entre medicina e ciência sem exigir um laboratório completo.

---

# 9. Preparação técnica

Mesmo sem implementar a investigação completa imediatamente, os dados do atendimento devem ser estruturados de forma reutilizável.

Elementos importantes:

* paciente;
* evidência;
* sintoma;
* exame;
* resultado;
* diagnóstico;
* tratamento;
* consequência.

Essas informações deverão poder ser consumidas futuramente pelo sistema de investigação científica.

---

# 10. Consequências da decisão

Ao escolher o modelo Médico + Cientista:

### Devemos

* conectar atendimento e pesquisa;
* tratar conhecimento como progressão;
* registrar evidências de forma estruturada;
* fazer descobertas alterarem possibilidades futuras;
* manter Saúde como parte central da gameplay.

### Não devemos

* criar dois jogos independentes dentro do mesmo projeto;
* transformar o laboratório em sistema complexo antes do atendimento funcionar;
* desenvolver dezenas de mecânicas científicas no PoC;
* adicionar conteúdo que não contribua para o ciclo principal.

---

# 11. Riscos

## Risco 1 — Escopo excessivo

Médico + Cientista pode facilmente se transformar em dois sistemas grandes.

### Mitigação

Validar primeiro o atendimento e representar a investigação de forma simples.

---

## Risco 2 — Sistemas desconectados

O jogador pode sentir que atendimento e pesquisa são atividades sem relação.

### Mitigação

Toda descoberta científica importante deverá produzir alguma consequência futura no atendimento.

---

## Risco 3 — Excesso de texto

O jogo pode depender demais de diálogos e interfaces.

### Mitigação

Utilizar:

* decisões frequentes;
* feedback visual;
* exames;
* prontuário;
* consequências;
* progressão perceptível.

---

# 12. Critério de validação

Esta decisão será considerada validada quando o jogador conseguir compreender, durante a demonstração, que:

1. atende pacientes;
2. obtém informações;
3. utiliza essas informações para tomar decisões;
4. aprende algo sobre a Nexum;
5. esse conhecimento pode melhorar atendimentos futuros.

Se essa relação não estiver clara, o core loop deverá ser revisado.

---

# 13. Regra final

> **O jogador não pesquisa a Nexum apenas para preencher uma barra de progresso.**

A pesquisa deve existir porque o conhecimento adquirido modifica a forma como o jogador consegue cuidar dos próximos pacientes.

