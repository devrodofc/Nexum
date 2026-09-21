# NEXUM — Game Design Document

**Versão:** 0.1
**Status:** Pré-produção
**Projeto:** Próxima Fase! — Vortex 2026
**Engine:** Godot
**Categoria:** 2D Pixel Art
**Tema:** Saúde

---

# 1. Visão do jogo

**NEXUM** é um jogo 2D Pixel Art de narrativa, medicina e investigação científica ambientado no Brasil em 2226.

O jogador assume o papel de um dos poucos médicos e cientistas ainda em atividade após décadas em que as doenças foram consideradas um problema solucionado pela humanidade.

Com o surgimento da doença NEX-20, conhecida como **Nexum**, o protagonista precisa voltar a enfrentar problemas que a sociedade acreditava terem desaparecido.

Durante o jogo, o jogador atende pacientes, coleta evidências, formula hipóteses diagnósticas, toma decisões de tratamento e fornece orientações preventivas.

As informações obtidas nos atendimentos também contribuem para a investigação científica da Nexum.

A proposta central é fazer o jogador experimentar duas responsabilidades conectadas:

**cuidar das pessoas que estão sofrendo agora**

e

**compreender a doença para melhorar os próximos atendimentos.**

---

# 2. Pitch

> Em 2226, décadas após a humanidade acreditar ter erradicado todas as doenças, uma pandemia desconhecida obriga um dos últimos médicos-cientistas do mundo a tratar pacientes enquanto investiga a doença que ameaça uma sociedade despreparada para enfrentá-la.

---

# 3. Fantasia do jogador

O jogador deve sentir que é:

> **um médico-cientista tentando compreender uma doença desconhecida enquanto vidas dependem das decisões tomadas com informações incompletas.**

O jogador não começa dominando a Nexum.

O conhecimento sobre a doença deve crescer junto com sua experiência.

A progressão não acontece apenas através de números ou equipamentos.

**Conhecimento também é progressão.**

---

# 4. Contexto narrativo

## 4.1 2186 — A cura

Em 2186, avanços extraordinários em tecnologia, biologia e medicina permitiram o desenvolvimento de uma solução capaz de eliminar as doenças conhecidas.

Com o passar das décadas, doenças deixaram de representar uma preocupação significativa para a humanidade.

A expectativa de vida aumentou e a necessidade de profissionais especializados em medicina diminuiu drasticamente.

A medicina passou gradualmente a ser uma área pouco procurada.

---

## 4.2 2220 — NEX-20

Em **1º de julho de 2220**, uma nova doença surgiu.

Ela apresentou uma capacidade de transmissão extremamente elevada e rapidamente se espalhou pela população.

A doença recebeu a identificação **NEX-20** e passou a ser conhecida popularmente como **Nexum**.

A humanidade, acostumada a décadas sem grandes ameaças epidemiológicas, não estava preparada.

Medidas severas de isolamento foram adotadas enquanto cientistas e os poucos profissionais de saúde restantes tentavam compreender a nova ameaça.

---

## 4.3 2226 — O jogador

Seis anos depois, a Nexum continua sendo um grande desafio.

O jogador trabalha em um hospital e centro científico brasileiro.

Ele é simultaneamente:

* médico;
* pesquisador;
* cientista.

Sua rotina é dividida entre cuidar das pessoas afetadas e estudar as evidências produzidas pela própria doença.

---

# 5. Pilares de design

## 5.1 Medicina

O atendimento de pacientes constitui a principal atividade do jogador.

O jogador deverá:

* conversar;
* observar;
* investigar;
* solicitar exames;
* interpretar evidências;
* formular hipóteses;
* decidir uma conduta;
* acompanhar consequências.

---

## 5.2 Ciência

O conhecimento disponível sobre a Nexum é incompleto.

Os atendimentos produzem:

* dados;
* evidências;
* observações;
* amostras.

Essas informações poderão alimentar a investigação científica.

Descobertas realizadas através da pesquisa poderão modificar atendimentos posteriores.

---

## 5.3 Decisão

O jogador não deve apenas avançar diálogos.

Sempre que possível, uma interação importante deve produzir uma decisão.

A estrutura desejada é:

**INFORMAÇÃO → INTERPRETAÇÃO → DECISÃO → CONSEQUÊNCIA**

---

## 5.4 Saúde

Saúde deve influenciar diretamente as mecânicas.

Os principais eixos trabalhados serão:

* prevenção;
* diagnóstico;
* tratamento;
* acompanhamento;
* pesquisa;
* futuramente, reabilitação.

Se o tema Saúde fosse removido, o core loop do jogo deixaria de funcionar.

---

# 6. Core Loop

O ciclo completo planejado para NEXUM é:

```text
ATENDIMENTO
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
PRÓXIMO ATENDIMENTO
```

O PoC não precisa implementar imediatamente toda a profundidade desse ciclo.

O primeiro objetivo será validar:

```text
PACIENTE
↓
INVESTIGAÇÃO CLÍNICA
↓
DECISÃO
↓
CONSEQUÊNCIA
↓
FIM
```

---

# 7. Estrutura de um atendimento

Um atendimento deve durar aproximadamente **2 a 4 minutos** no PoC.

O atendimento possui as seguintes etapas.

---

## 7.1 Entrada do paciente

O paciente entra no ambiente de atendimento.

O jogador recebe informações iniciais, como:

* identificação;
* idade;
* queixa principal.

Exemplo:

> Paciente 003 — Marina, 31 anos
> “Estou com dificuldade para respirar desde ontem.”

O jogador ainda não possui todas as informações necessárias.

---

# 8. Anamnese

A conversa é uma ferramenta de investigação.

O jogador escolhe perguntas para obter informações sobre o paciente.

As perguntas podem abordar:

### Sintomas

* início;
* intensidade;
* duração;
* evolução.

### Histórico

* condições anteriores;
* tratamentos;
* informações clínicas relevantes.

### Exposição

* contato com infectados;
* ambientes frequentados;
* possíveis situações de transmissão.

### Prevenção

* medidas preventivas utilizadas;
* comportamento recente;
* contato com outras pessoas.

As respostas alimentam o prontuário.

---

# 9. Prontuário

O prontuário funciona como o principal registro de informações do paciente.

Pode conter:

```text
PACIENTE

Queixa principal

Sintomas descobertos

Histórico

Possível exposição

Exames realizados

Resultados

Hipótese diagnóstica

Tratamento

Orientação preventiva

Resultado
```

O prontuário também será importante futuramente para o sistema de investigação científica.

---

# 10. Exame clínico

O jogador pode realizar verificações clínicas simples.

Exemplos possíveis:

* temperatura;
* saturação;
* frequência cardíaca.

No PoC, essas ações não precisam possuir minigames próprios.

A interação pode seguir:

```text
SELECIONAR EXAME
↓
FEEDBACK
↓
RESULTADO
↓
REGISTRO NO PRONTUÁRIO
```

---

# 11. Exames complementares

Dependendo das evidências encontradas, o jogador poderá solicitar exames.

Exemplos conceituais:

* análise sanguínea;
* teste relacionado à Nexum;
* exame de imagem.

O conjunto definitivo será determinado durante a produção.

Exames devem existir para fornecer **informação útil para uma decisão**, e não apenas aumentar a quantidade de interações.

Futuramente poderão existir limitações relacionadas a:

* tempo;
* disponibilidade;
* recursos;
* conhecimento científico.

---

# 12. Evidências

Toda informação relevante descoberta durante um atendimento será tratada conceitualmente como uma **evidência**.

Exemplos:

```text
Sintoma

Histórico

Contato

Resultado clínico

Resultado laboratorial

Resposta ao tratamento

Amostra
```

As evidências possuem duas funções:

### Clínica

Ajudar o jogador a tomar decisões sobre aquele paciente.

### Científica

Fornecer dados para compreender a Nexum.

Essa estrutura deve permitir que o sistema de investigação científica seja desenvolvido posteriormente sem reconstruir todo o sistema de pacientes.

---

# 13. Diagnóstico

Depois de reunir informações, o jogador deverá formular uma hipótese.

O PoC trabalhará com poucas possibilidades.

Exemplo conceitual:

```text
Nexum — quadro leve

Nexum — quadro grave

Inconclusivo
```

O objetivo não é reproduzir toda a complexidade da medicina real.

O diagnóstico deve funcionar como um problema de interpretação:

> **Com as evidências disponíveis, qual hipótese parece mais adequada?**

---

# 14. Tratamento

Depois da hipótese diagnóstica, o jogador decide uma conduta.

As opções disponíveis podem variar de acordo com o conhecimento científico adquirido.

Inicialmente, tratamentos podem ser limitados.

Exemplo conceitual:

```text
CONDUTA A

CONDUTA B

SUPORTE CLÍNICO
```

Algumas possibilidades futuras poderão aparecer bloqueadas:

```text
???

Conhecimento insuficiente.
```

Isso ajuda a comunicar que a compreensão da Nexum ainda está evoluindo.

---

# 15. Prevenção

Prevenção deverá aparecer durante os atendimentos e nas consequências das decisões.

O jogador poderá fornecer orientações ao paciente ou às pessoas próximas dele.

Exemplo:

```text
Qual orientação será fornecida?

[A]

[B]

[C]
```

A escolha poderá influenciar acontecimentos posteriores.

Exemplo:

```text
ATENDIMENTO
↓
ORIENTAÇÃO
↓
TEMPO
↓
CONSEQUÊNCIA
```

Uma orientação adequada poderá reduzir determinados riscos.

Uma orientação inadequada poderá produzir consequências narrativas ou mecânicas.

O objetivo é fazer prevenção possuir impacto, e não funcionar apenas como texto educativo.

---

# 16. Consequências

As decisões tomadas durante um atendimento devem produzir algum tipo de resposta.

Uma consequência pode ser:

* clínica;
* narrativa;
* científica;
* preventiva.

O jogador poderá descobrir consequências imediatamente ou posteriormente.

Exemplo:

> Um paciente atendido anteriormente retorna ao hospital.

Ou:

> Pessoas que tiveram contato com determinado paciente começaram a apresentar sintomas.

O sistema deverá evitar transformar toda decisão em simplesmente:

**CERTO / ERRADO.**

Sempre que possível, o jogador deverá compreender **por que** determinada consequência ocorreu.

---

# 17. Investigação científica

A investigação científica é uma parte planejada do jogo e deverá utilizar as evidências produzidas durante os atendimentos.

O ciclo futuro será:

```text
EVIDÊNCIAS
↓
OBSERVAÇÃO
↓
HIPÓTESE
↓
INVESTIGAÇÃO / EXPERIMENTO
↓
RESULTADO
↓
DESCOBERTA
```

Exemplo conceitual:

```text
Paciente A → característica X

Paciente B → característica X

Paciente C → característica X

          ↓

Possível padrão identificado

          ↓

Hipótese

          ↓

Investigação

          ↓

Descoberta
```

Uma descoberta pode desbloquear:

* novas informações;
* novas perguntas;
* novos exames;
* novas opções de tratamento;
* novas medidas preventivas.

Portanto:

**atendimentos alimentam a pesquisa**

e

**pesquisa melhora os atendimentos.**

A gameplay completa de investigação não faz parte do primeiro graybox.

---

# 18. Reabilitação e acompanhamento

Reabilitação faz parte da visão futura do projeto.

Inicialmente, ela poderá ser representada através do retorno de pacientes e diálogos.

Exemplo:

> Um paciente anteriormente tratado retorna apresentando dificuldades durante sua recuperação.

Isso permite abordar:

* recuperação;
* acompanhamento;
* sequelas;
* adaptação;
* qualidade de vida.

Uma gameplay específica de reabilitação poderá ser explorada futuramente.

---

# 19. Progressão

A principal progressão conceitual de NEXUM será:

> **conhecimento.**

No começo, tanto o jogador quanto o protagonista sabem pouco sobre a doença.

Conforme evidências são encontradas:

```text
DESCONHECIDO
↓
OBSERVADO
↓
HIPÓTESE
↓
INVESTIGADO
↓
COMPREENDIDO
```

Novos conhecimentos poderão alterar as possibilidades disponíveis.

Exemplos:

```text
Nova pergunta

Novo exame

Nova interpretação

Novo tratamento

Nova prevenção
```

---

# 20. Vitória e derrota

NEXUM não precisa utilizar uma estrutura tradicional de vitória baseada em combate.

No PoC, o objetivo será completar uma pequena sequência de atendimentos e demonstrar evolução do conhecimento sobre a Nexum.

As decisões podem produzir resultados melhores ou piores.

O jogador poderá:

* estabilizar pacientes;
* cometer erros;
* obter informações incompletas;
* descobrir novas evidências;
* produzir consequências futuras.

Condições definitivas de vitória e derrota para uma versão maior ainda serão definidas.

---

# 21. Estrutura do PoC

O primeiro graybox utilizará apenas **um paciente**.

### Conteúdo inicial

* 1 paciente;
* 1 queixa principal;
* 3 perguntas;
* 2 verificações clínicas;
* 1 exame complementar;
* 2 hipóteses diagnósticas;
* 2 possibilidades de conduta;
* 1 decisão preventiva;
* consequências simples;
* registro das evidências.

O objetivo é validar o atendimento completo antes de adicionar conteúdo.

---

# 22. Experiência desejada

Durante um atendimento, queremos que o jogador pense:

> “Preciso entender o que está acontecendo.”

Depois:

> “Tenho informações suficientes para tomar essa decisão?”

E posteriormente:

> “Agora sei algo sobre a Nexum que antes não sabia.”

Essa sequência representa a experiência central desejada.

---

# 23. Direção visual

O jogo utilizará **Pixel Art 2D**.

A direção visual deverá priorizar:

* leitura clara;
* poucos ambientes;
* personagens reconhecíveis;
* interfaces legíveis;
* animações pequenas;
* produção compatível com o tamanho da equipe.

O hospital e laboratório devem comunicar uma sociedade tecnologicamente avançada, mas pressionada pela crise da Nexum.

A direção artística definitiva será estabelecida após a validação do graybox.

---

# 24. Áudio

O áudio deverá reforçar:

* ambiente hospitalar;
* tensão;
* investigação;
* consequências das decisões.

O PoC não exige uma grande quantidade de músicas ou efeitos.

Prioridade:

```text
feedback funcional
>
ambientação
>
variedade
```

---

# 25. Princípios de produção

Durante o desenvolvimento, toda nova ideia deverá responder:

> **Isso melhora a demonstração da ideia central?**

Caso contrário, não deverá entrar automaticamente no PoC.

A prioridade será:

1. core loop;
2. clareza;
3. estabilidade;
4. feedback;
5. apresentação;
6. expansão.

---

# 26. Visão futura

Após a validação do PoC, NEXUM poderá explorar sistemas como:

* investigação científica interativa;
* laboratório;
* novos pacientes;
* diferentes manifestações da Nexum;
* acompanhamento de pacientes;
* reabilitação;
* recursos hospitalares limitados;
* evolução da pandemia;
* decisões de saúde pública;
* novos exames;
* novos tratamentos;
* diferentes medidas preventivas;
* relações entre pacientes;
* consequências de longo prazo;
* exploração de setores do hospital;
* narrativa expandida.

Esses elementos representam possibilidades de expansão.

**Eles não constituem compromisso com o PoC atual.**

---

# 27. Regra de escopo

O jogo implementado é a fonte final de verdade.

Este documento deverá evoluir conforme o projeto for testado.

Se uma mecânica descrita aqui não contribuir para a experiência central ou se mostrar inviável dentro do período disponível, ela poderá ser simplificada, adiada ou removida.

O objetivo do programa não é implementar tudo que NEXUM poderia se tornar.

O objetivo é demonstrar com qualidade **por que NEXUM pode se tornar um jogo interessante.**
