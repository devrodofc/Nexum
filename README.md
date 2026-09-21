# NEXUM

> Um jogo 2D Pixel Art sobre medicina, ciência e a luta contra uma doença desconhecida.

Projeto desenvolvido para o programa **Próxima Fase! — Vortex**, na temática **Saúde**.

## Sobre o projeto

O ano era 2186.

Os avanços da tecnologia, biologia e medicina permitiram à humanidade alcançar algo antes considerado impossível: uma cura definitiva para todas as doenças conhecidas.

Com a erradicação das doenças, a expectativa de vida aumentou drasticamente e, ao longo das décadas seguintes, a medicina perdeu grande parte de sua importância. Cada vez menos pessoas decidiram seguir a profissão.

Até que tudo mudou.

Em **1º de julho de 2220**, uma nova doença altamente contagiosa surgiu. Embora sua mortalidade pudesse ser controlada em determinadas circunstâncias, sua capacidade de transmissão tornou sua contenção extremamente difícil.

A doença passou a ser conhecida como **NEX-20**, ou simplesmente **Nexum**.

Em **2226**, seis anos após o início da pandemia, o jogador assume o papel de um dos poucos médicos e cientistas ainda em atividade, trabalhando em um hospital e centro de pesquisa brasileiro.

Sua missão é atender os pacientes afetados pela Nexum enquanto coleta evidências e contribui para compreender uma doença sobre a qual a humanidade ainda sabe muito pouco.

## Conceito

**NEXUM** combina atendimento médico, tomada de decisões e investigação científica.

O jogador deverá observar pacientes, conversar com eles, identificar sintomas, solicitar exames, formular hipóteses diagnósticas, decidir tratamentos e fornecer orientações preventivas.

As informações obtidas durante os atendimentos também poderão contribuir para o estudo da Nexum.

O objetivo é criar uma relação entre duas funções do protagonista:

**Médico → cuidar das pessoas.**

**Cientista → compreender a doença.**

O conhecimento adquirido ao longo do jogo poderá modificar as possibilidades disponíveis nos atendimentos seguintes.

## Core Loop

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
RESULTADO
   ↓
DADOS / AMOSTRAS
   ↓
PESQUISA
   ↓
NOVOS CONHECIMENTOS
   ↓
NOVOS ATENDIMENTOS
```

O primeiro protótipo será construído em torno de um atendimento completo antes da expansão para novos pacientes e sistemas.

## Saúde

O projeto busca integrar diferentes aspectos da área de Saúde diretamente às decisões do jogador.

Os principais pilares são:

* **Prevenção:** orientar pacientes e reduzir possíveis riscos de transmissão;
* **Diagnóstico:** coletar e interpretar evidências para formular hipóteses;
* **Tratamento:** selecionar condutas e acompanhar suas consequências;
* **Pesquisa:** utilizar informações clínicas para compreender a Nexum;
* **Reabilitação:** acompanhar a recuperação dos pacientes, planejada para etapas posteriores do projeto.

A intenção é fazer com que Saúde faça parte das próprias mecânicas do jogo, e não apenas de sua ambientação.

## Escopo inicial

O Proof of Concept será pequeno e concentrado na validação do core loop.

O primeiro objetivo jogável será:

```text
INÍCIO
  ↓
PACIENTE ENTRA
  ↓
INVESTIGAÇÃO CLÍNICA
  ↓
DIAGNÓSTICO
  ↓
TRATAMENTO
  ↓
ORIENTAÇÃO
  ↓
CONSEQUÊNCIA
  ↓
FIM DO ATENDIMENTO
```

Sistemas maiores serão adicionados somente após a validação desse ciclo.

## Tecnologia

* **Engine:** Godot
* **Linguagem:** GDScript
* **Estilo:** 2D Pixel Art
* **Versionamento:** Git + GitHub
* **Gerenciamento:** GitHub Projects / Issues

## Equipe

### Rodrigo

Programação, Game Design e UI.

### Daniel

Programação, Pixel Art, Game Design e Áudio.

### Gustavo

Programação, UI e Game Design.

## Desenvolvimento

O projeto será desenvolvido durante o programa **Próxima Fase! — Vortex**, entre **01/10 e 28/10**, com apresentação prevista para **29/10 e 30/10**.

O desenvolvimento seguirá quatro etapas principais:

**Semana 1 — O jogo existe.**

Construção do projeto, controles, sistemas fundamentais e primeiro graybox jogável.

**Semana 2 — O jogo funciona.**

Integração do core loop, consequências, conteúdo principal e primeiros playtests.

**Semana 3 — O jogo parece um jogo.**

Pixel Art, interface, áudio, feedback visual e balanceamento.

**Semana 4 — O jogo está apresentável.**

Correção de bugs, polish, builds, playtests finais, documentação e preparação da apresentação.

## Status

🚧 **Em pré-produção.**

Atualmente estamos definindo o escopo, documentando as decisões de design e preparando o primeiro vertical slice.

---

Desenvolvido para o **Próxima Fase! — Vortex 2026**.
