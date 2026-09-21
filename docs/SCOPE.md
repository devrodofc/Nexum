# NEXUM — Scope

**Versão:** 0.1
**Status:** Pré-produção
**Projeto:** Próxima Fase! — Vortex 2026

---

# 1. Objetivo deste documento

Este documento define o escopo de desenvolvimento de **NEXUM** durante o programa Próxima Fase! — Vortex.

Seu objetivo é separar claramente:

* o que é necessário para demonstrar o jogo;
* o que melhora a experiência;
* o que representa expansão futura;
* o que não será desenvolvido durante o programa.

A prioridade é entregar um **Proof of Concept pequeno, funcional, estável e apresentável**.

---

# 2. Restrição principal

O projeto será desenvolvido por:

* Rodrigo;
* Daniel;
* Gustavo.

Disponibilidade aproximada:

**7 horas semanais por integrante.**

Durante quatro semanas:

```text
3 integrantes
×
7 horas
×
4 semanas

≈ 84 horas totais
```

Esse tempo inclui:

* programação;
* arte;
* áudio;
* testes;
* integração;
* reuniões;
* documentação;
* correção de bugs;
* preparação da apresentação.

Portanto, as 84 horas não devem ser tratadas como 84 horas exclusivamente de implementação.

---

# 3. Objetivo do PoC

O PoC deve provar que o conceito central de NEXUM funciona.

Ao final do programa, deve ser possível demonstrar:

```text
PACIENTE CHEGA
↓
JOGADOR INVESTIGA
↓
OBTÉM EVIDÊNCIAS
↓
FORMULA UMA HIPÓTESE
↓
DECIDE UMA CONDUTA
↓
FORNECE UMA ORIENTAÇÃO PREVENTIVA
↓
RECEBE UMA CONSEQUÊNCIA
↓
OBTÉM INFORMAÇÃO ÚTIL SOBRE A NEXUM
```

O avaliador deve compreender a proposta mesmo sem uma versão completa do jogo.

---

# 4. Regra de prioridade

Toda funcionalidade será classificada como:

## P0 — Necessária

Sem ela, a ideia central não pode ser demonstrada adequadamente.

## P1 — Importante

Melhora significativamente a experiência, clareza ou apresentação.

Não é necessária para provar o conceito.

## P2 — Futuro

Expande o jogo, mas não deve comprometer a entrega do PoC.

---

# 5. Tamanho das tarefas

Toda funcionalidade deverá também receber uma estimativa de complexidade.

## S — Pequena

Pode ser concluída em algumas horas.

## M — Média

Pode consumir aproximadamente um dia de trabalho.

## L — Grande

Pode exigir vários dias ou integração significativa.

## XL — Muito grande ou incerta

Possui risco elevado de consumir tempo imprevisível.

---

# 6. Regra de risco

Uma tarefa classificada como:

**P0 + XL**

deve ser imediatamente revisada.

Ela deverá ser:

* simplificada;
* dividida;
* substituída;
* ou removida do P0.

O PoC não deve depender de uma única funcionalidade de alto risco.

---

# 7. P0 — Escopo obrigatório

## 7.1 Estrutura básica do jogo

O projeto deverá possuir:

* projeto Godot funcional;
* cena principal;
* transição para o atendimento;
* interface mínima;
* fluxo completo até o encerramento do atendimento.

**Prioridade:** P0

---

## 7.2 Paciente

O jogo deverá possuir pelo menos um paciente completamente funcional.

O paciente precisa conter:

* identificação;
* idade;
* queixa principal;
* respostas da anamnese;
* evidências;
* resultados de exames;
* possibilidades diagnósticas;
* possibilidades de tratamento;
* consequência.

**Prioridade:** P0

---

## 7.3 Sistema de diálogo

O jogador deverá conseguir conversar com o paciente.

Para o primeiro graybox:

* aproximadamente 3 perguntas;
* respostas pré-definidas;
* perguntas relacionadas ao estado do paciente;
* informações relevantes registradas.

Não será necessário criar um sistema narrativo complexo.

**Prioridade:** P0

---

## 7.4 Anamnese

As perguntas deverão permitir descobrir informações relacionadas a:

* sintomas;
* histórico;
* exposição;
* prevenção.

As respostas precisam possuir alguma utilidade para a decisão do jogador.

**Prioridade:** P0

---

## 7.5 Prontuário

O jogador deverá possuir uma forma de consultar as informações encontradas.

O prontuário deve registrar pelo menos:

* sintomas;
* histórico relevante;
* resultados clínicos;
* exame complementar.

**Prioridade:** P0

---

## 7.6 Evidências

As informações obtidas deverão ser registradas de forma estruturada.

O sistema deverá distinguir conceitualmente informações como:

* sintoma;
* resultado;
* histórico;
* exposição;
* amostra ou dado científico.

Esse sistema deverá ser desenvolvido pensando na futura investigação científica.

**Prioridade:** P0

---

## 7.7 Exame clínico

O primeiro atendimento deverá possuir aproximadamente:

* 2 verificações clínicas.

Exemplo:

* temperatura;
* saturação.

Não será necessário desenvolver minigames específicos para cada exame.

Fluxo suficiente:

```text
ESCOLHER
↓
EXECUTAR
↓
RECEBER RESULTADO
↓
REGISTRAR
```

**Prioridade:** P0

---

## 7.8 Exame complementar

O primeiro atendimento deverá possuir:

* pelo menos 1 exame complementar.

Ele deverá revelar uma informação relevante para o diagnóstico.

**Prioridade:** P0

---

## 7.9 Diagnóstico

O jogador deverá selecionar uma hipótese após analisar as evidências.

No primeiro graybox:

* aproximadamente 2 possibilidades diagnósticas.

O diagnóstico deverá influenciar a próxima etapa.

**Prioridade:** P0

---

## 7.10 Tratamento

Depois do diagnóstico, o jogador deverá decidir uma conduta.

No primeiro graybox:

* aproximadamente 2 opções.

A escolha deverá influenciar o resultado do atendimento.

**Prioridade:** P0

---

## 7.11 Prevenção

O jogador deverá tomar pelo menos uma decisão relacionada à prevenção.

Exemplo:

* orientação fornecida ao paciente;
* recomendação relacionada ao contato com outras pessoas;
* ação preventiva relacionada ao comportamento da Nexum.

A decisão deverá possuir alguma consequência perceptível.

**Prioridade:** P0

---

## 7.12 Consequência

O atendimento deverá terminar com uma consequência baseada nas decisões realizadas.

Ela pode ser apresentada através de:

* diálogo;
* mensagem;
* alteração no estado do paciente;
* resumo do atendimento.

O jogador precisa perceber que suas decisões tiveram impacto.

**Prioridade:** P0

---

## 7.13 Conexão com pesquisa

O primeiro PoC não precisa possuir a gameplay completa do laboratório.

Porém, o atendimento deverá gerar pelo menos uma informação que possa ser apresentada como:

* evidência científica;
* dado;
* observação;
* amostra.

O jogo deverá comunicar que esse material poderá contribuir para a investigação da Nexum.

**Prioridade:** P0

---

## 7.14 Início e fim claros

O jogador deverá compreender:

* quando o atendimento começa;
* o que precisa fazer;
* quando tomou sua decisão;
* quando o atendimento terminou.

**Prioridade:** P0

---

# 8. P1 — Melhorias importantes

Funcionalidades P1 serão desenvolvidas apenas se o P0 estiver estável.

---

## 8.1 Mais pacientes

Adicionar aproximadamente:

* 2 a 4 novos pacientes.

Cada paciente deverá apresentar alguma variação relevante.

Não adicionar pacientes apenas para aumentar quantidade de conteúdo.

**Prioridade:** P1

---

## 8.2 Retorno de paciente

Um paciente atendido anteriormente poderá reaparecer posteriormente.

O retorno poderá mostrar:

* evolução;
* recuperação;
* complicação;
* consequência de uma orientação anterior.

Isso permite introduzir acompanhamento e reabilitação.

**Prioridade:** P1

---

## 8.3 Reabilitação narrativa

Adicionar decisões simples relacionadas à recuperação.

Não será necessário desenvolver um sistema completo.

Exemplo:

```text
PACIENTE RETORNA
↓
RELATA LIMITAÇÃO
↓
JOGADOR ANALISA
↓
ORIENTAÇÃO DE RECUPERAÇÃO
```

**Prioridade:** P1

---

## 8.4 Primeira descoberta científica

Uma evidência obtida durante atendimentos poderá gerar uma pequena descoberta.

Exemplo:

```text
EVIDÊNCIA
↓
DESCOBERTA
↓
NOVA INFORMAÇÃO
```

Essa descoberta poderá desbloquear:

* pergunta;
* exame;
* informação;
* tratamento.

**Prioridade:** P1

---

## 8.5 Recursos limitados

Algumas decisões poderão exigir escolher entre diferentes recursos.

Exemplos:

* exames limitados;
* tempo;
* disponibilidade.

Somente será implementado se melhorar claramente as decisões.

**Prioridade:** P1

---

## 8.6 Arte final básica

Após o graybox funcionar:

* personagem;
* pacientes;
* cenário principal;
* objetos essenciais;
* elementos principais da interface.

**Prioridade:** P1

---

## 8.7 Animações básicas

Somente animações necessárias para melhorar leitura e apresentação.

Exemplos:

* idle;
* entrada do paciente;
* pequenos feedbacks.

**Prioridade:** P1

---

## 8.8 Áudio

Adicionar:

* feedback de interface;
* ambiente;
* efeitos principais;
* música, caso haja tempo.

**Prioridade:** P1

---

## 8.9 Feedback visual

Adicionar feedback para:

* nova evidência;
* resultado de exame;
* decisão;
* consequência;
* descoberta.

**Prioridade:** P1

---

# 9. P2 — Visão futura

As seguintes funcionalidades fazem parte da visão de NEXUM, mas não são necessárias para o PoC.

---

## 9.1 Investigação científica completa

Gameplay específica de laboratório envolvendo:

* comparação de evidências;
* identificação de padrões;
* formulação de hipóteses;
* experimentos;
* validação;
* descobertas.

**Prioridade:** P2

---

## 9.2 Sistema completo de reabilitação

Possibilidades futuras:

* acompanhamento de longo prazo;
* recuperação gradual;
* sequelas;
* exercícios;
* retorno às atividades;
* evolução clínica.

**Prioridade:** P2

---

## 9.3 Políticas de saúde pública

Possibilidades futuras:

* campanhas;
* isolamento;
* distribuição de recursos;
* protocolos;
* decisões populacionais.

**Prioridade:** P2

---

## 9.4 Evolução dinâmica da pandemia

Sistema que simule:

* contaminação;
* transmissão;
* regiões;
* crescimento de casos.

**Prioridade:** P2

---

## 9.5 Exploração do hospital

Movimentação livre entre setores.

Possíveis locais:

* atendimento;
* laboratório;
* internação;
* administração.

**Prioridade:** P2

---

## 9.6 Sistema avançado de recursos

Possibilidades:

* medicamentos;
* equipamentos;
* orçamento;
* vagas;
* profissionais;
* materiais.

**Prioridade:** P2

---

## 9.7 Narrativa expandida

Possibilidades:

* personagens recorrentes;
* relações;
* eventos;
* escolhas narrativas;
* múltiplos finais.

**Prioridade:** P2

---

## 9.8 Progressão extensa

Não faz parte do PoC:

* grandes árvores de habilidade;
* níveis;
* dezenas de desbloqueios;
* sistemas extensos de progressão.

**Prioridade:** P2

---

# 10. Fora do escopo do programa

As funcionalidades abaixo **não deverão ser desenvolvidas durante os 28 dias**, salvo mudança formal de escopo.

* multiplayer;
* modo cooperativo;
* backend online;
* contas de usuários;
* ranking online;
* mundo aberto;
* grande exploração;
* combate;
* procedural complexo;
* geração procedural de pacientes;
* dezenas de doenças;
* simulação médica realista completa;
* inteligência artificial avançada;
* inventário complexo;
* crafting;
* árvore extensa de habilidades;
* dezenas de tratamentos;
* dezenas de exames;
* dezenas de pacientes;
* sistema econômico completo;
* save complexo;
* múltiplas campanhas;
* múltiplos finais complexos;
* física avançada;
* integração com banco de dados externo.

---

# 11. Escopo de conteúdo do primeiro graybox

A primeira versão jogável deverá possuir exatamente o necessário para validar a mecânica.

Meta inicial:

```text
1 paciente

3 perguntas

2 verificações clínicas

1 exame complementar

2 hipóteses diagnósticas

2 opções de tratamento

1 decisão preventiva

1 consequência

1 evidência científica
```

Nenhum conteúdo adicional deverá ser necessário para realizar o primeiro playtest.

---

# 12. Gate do graybox

Antes de adicionar novos pacientes, arte extensa ou investigação científica, o jogo deverá permitir:

```text
INICIAR
↓
RECEBER PACIENTE
↓
CONVERSAR
↓
COLETAR INFORMAÇÕES
↓
REALIZAR EXAMES
↓
CONSULTAR PRONTUÁRIO
↓
DIAGNOSTICAR
↓
ESCOLHER TRATAMENTO
↓
ORIENTAR PREVENÇÃO
↓
RECEBER CONSEQUÊNCIA
↓
FINALIZAR ATENDIMENTO
```

Se esse ciclo ainda não funcionar, a prioridade continua sendo o graybox.

---

# 13. Gate para adicionar P1

Uma funcionalidade P1 só deverá entrar em produção quando:

* o core loop estiver completo;
* o build estiver funcionando;
* não houver bug bloqueante;
* o primeiro playtest tiver sido realizado;
* a equipe considerar o P0 tecnicamente seguro.

---

# 14. Regra para novas ideias

Toda nova ideia deverá responder:

## Pergunta 1

**Isso melhora a demonstração da ideia central?**

## Pergunta 2

**Precisamos disso para o avaliador compreender NEXUM?**

## Pergunta 3

**Qual problema atual essa funcionalidade resolve?**

## Pergunta 4

**Qual é sua prioridade?**

P0, P1 ou P2?

## Pergunta 5

**Qual é o tamanho?**

S, M, L ou XL?

Se não houver uma resposta clara, a funcionalidade permanece no backlog futuro.

---

# 15. Controle de mudanças

Mudanças significativas deverão ser registradas.

São consideradas significativas alterações em:

* core loop;
* gênero;
* prioridade;
* sistemas P0;
* número de pacientes;
* estrutura do atendimento;
* prazo;
* tecnologia principal.

Uma mudança de escopo deverá responder:

```text
O que mudou?

Por que mudou?

O que entra?

O que sai?

Qual impacto no prazo?

Qual risco?
```

Não adicionar funcionalidades apenas porque surgiu tempo aparente em uma etapa.

---

# 16. Ordem de corte

Caso o projeto atrase, a ordem de corte será:

```text
1. P2
↓
2. P1
↓
3. quantidade de conteúdo
↓
4. complexidade visual
↓
5. simplificação de sistemas P0
```

O core loop deverá ser preservado.

---

# 17. Semana 4 protegida

A quarta semana será destinada principalmente a:

* correção de bugs;
* integração;
* testes;
* builds;
* polish;
* balanceamento;
* documentação;
* apresentação;
* ensaio.

Não deverão ser iniciados sistemas críticos novos nessa semana.

Qualquer funcionalidade incompleta no início da Semana 4 deverá ser avaliada para:

* simplificação;
* adiamento;
* remoção.

---

# 18. Definition of Done

Uma funcionalidade só será considerada concluída quando:

* funcionar conforme o esperado;
* atender aos critérios de aceite;
* tiver sido testada;
* não quebrar o build;
* estiver integrada ao projeto;
* estiver enviada ao GitHub.

> “Funciona no computador de quem desenvolveu” não representa conclusão.

---

# 19. Critério de sucesso do PoC

NEXUM será considerado um PoC bem-sucedido se, ao final do programa, for possível demonstrar de forma clara:

## Ideia

O avaliador entende rapidamente quem é o jogador e qual é seu objetivo.

## Loop

Existe um atendimento completo e jogável.

## Saúde

Prevenção, diagnóstico e tratamento influenciam diretamente as decisões.

## Ciência

O jogo demonstra a conexão entre pacientes, evidências e investigação da Nexum.

## Consequência

As decisões produzem resultados perceptíveis.

## Estabilidade

A demonstração pode ser executada sem depender de improvisos ou correções durante a apresentação.

## Expansão

A equipe consegue explicar como investigação científica, acompanhamento, reabilitação e saúde pública poderiam expandir o sistema no futuro.

---

# 20. Princípio final

Durante o programa:

> **É melhor demonstrar perfeitamente um pequeno ciclo de atendimento do que apresentar vários sistemas incompletos.**

NEXUM deve provar sua ideia antes de tentar provar seu tamanho.
