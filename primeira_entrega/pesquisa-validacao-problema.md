# Entregável Parcial 01: Pesquisa & Validação de Problema - Synthesis

**Curso:** FIAP MBA • MBI LIVE - Empreendedorismo e Inovação 
**Entrega:** Checkpoint 01
**Data alvo:** 23/08/2026
**Grupo:** 

1. Guilherme Csorgo
2. Karen Martins
3. Ludimila Rocha
4. Thiago Guilherme

**Pergunta a ser respondida:** O problema investigado é real, relevante e merece ser resolvido?

**Frase-síntese (TODO: Completar ao final da investigação):**

> "Estamos investigando [problema], que afeta [público] em [contexto]. Inicialmente levantamos [hipóteses]. A partir de [fontes e pesquisa de campo], encontramos [principais evidências]. Com isso, nosso recorte do problema é [definição final]."

---

## 01. Contexto e a dor identificada

VIvemos em um mundo competitivo onde cada minuto te diferencia do seu concorrente. O relógio do *time to market* não para nunca e parece cada vez mais acelerado a medida que novas tecnologias são criadas. Por vezes, a agilidade separa um produto utilizável de um produto útil, e as empresas tem cada vez menos tempo pra validar suas hipóteses antes de expô-las ao mercado. Um estudo publicado na *Marketing Letters* (2021) analisou 83.719 SKUs em 31 categorias de bens de consumo introduzidos nos EUA ao longo de oito anos (2002–2009). Ao fim do primeiro ano, 25% desses produtos não estavam mais vendendo. Após o segundo ano, o número subiu para 40% (Fonte: [Tremendous](https://www.tremendous.com/blog/why-new-product-launches-fail-how-to-avoid-it/)). Em contraste a isso, consumidores nunca geraram tantos dados sobre si mesmos e suas preferencias do que hoje. Outros estudos estimam que 173,4 zettabytes de dados foram criados em 2025, com projeção de ~240 ZB em 2026. Em base diária, são gerados aproximadamente 402,74 milhões de terabytes de dados por dia (Fontes: [Tech Business News](https://www.techbusinessnews.com.au/blog/402-74-million-terrabytes-of-data-is-created-every-day/) e [Design Rush](https://www.designrush.com/agency/it-services/trends/how-much-data-is-created-every-day)). Se houvesse uma forma de utilizar destes dados para que empresas tomem melhores decisões de produto sem perderem velocidade, consegiriamos elevar a regua de entrega de valor, e de quebra acelerariamos a cadência de entrega de produtos de forma exponencial a partir do conhecimento acumulado que criariamos.

### Qual situação está sendo investigada?

Partimos de duas perguntas fundamentais:

* Conseguimos usar os dados de preferencia e comportamento de usuários para tomarmos melhores decisões de produto?
* Assumindo que sim, há espaço no mercado para ofertarmos essa solução de forma rentável?

As alternativas existentes não endereçam esse problema por completo:

- **Pesquisas de mercado** custam entre R$30.000 e R$150.000 por projeto e levam cerca de 3 a 4 semanas para terem resultados. Elas são inacessíveis para a maioria das empresas de pequeno e médio porte, além de agências;
- **Focus groups** têm custo médio de US$3.000 ~ 8.000 por sessão e amostras pequenas (8-12 pessoas)
- **Testes A/B tradicionais** são o padrão ouro de evidência em produtos digitais hoje em dia, mas dependem do lançamento do produto, quando o erro já custou tempo e dinheiro
- **Entrevistas qualitativas** dependem de disponibilidade e recrutamento do público, o que é lento e caro para públicos de nicho
- **Intuição e experiência** são a alternativa mais usada, e a mais arriscada em cenários com orçamento baixo

### Por que isso é relevante?

A consequência de decidir sem validação de audiência se manifesta de diversas formas: campanhas que não convertem, produtos que não encontram demanda, budget de mídia desperdiçado, e oportunidades perdidas para a concorrência que testou antes e lançou mais rápido. Em adição a isso, vimos a ascenção de um novo nicho nos últimos anos: O(a)s digital influencers, youtubers e streamers. O problema não é novo, mas o contexto mudou. Hoje, há uma bilateralidade de interesses: Empresas não querem vincular suas marcas à pessoas com má reputação, e influencers não querem ser lembrados por produtos que fracassaram ou que estão imersos em polêmicas.

Em tecnologia, o cenário é promissor: o custo de inferência de LLMs caiu **78% entre 2024 e 2025**, criando uma janela técnica e econômica para tornar a validação de audiência acessível a quem nunca teve budget para pesquisa formal, além de acelerar a criação e entrega de um potencial produto no mercado para resolver essa dor.

No Brasil, a startup [Galaxies ](https://www.galaxies.com.br/)já prova que grandes empresas (Nestlé, Boticário, Bradesco, Banco do Brasil) pagam para resolver essa dor com personas sintéticas, mas opera exclusivamente em projetos de R$150.000+, deixando o mercado de PMEs, agências médias e profissionais independentes completamente desatendido.

---

## 02. Hipóteses

### Sobre a dor

Profissionais de marketing, fundadores de empresas de pequeno e médio porte além de profissionais da internet enfrentam regularmente a necessidade de entender como sua audiência vai reagir a uma ideia, campanha ou produto, mas não conseguem fazer isso de forma rápida e acessível com as ferramentas disponíveis hoje.

### Sobre as causas

A principal barreira não é falta de interesse em validar, mas o custo e o tempo criam um gap entre a vontade e a possibilidade.

### Sobre a frequência

Esse problema acontece com frequência alta para profissionais que gerenciam campanhas, lançamentos ou conteúdo de forma recorrente.

### Sobre o impacto

O custo de lançar sem validação é percebido como um problema real e recorrente, não como BAU (business as usual). Profissionais conseguem citar exemplos de decisões que custaram dinheiro, tempo ou reputação por falta de validação prévia.

### Sobre o comportamento do público

A alternativa mais usada hoje é a intuição ou a opinião interna da equipe, e as pessoas sabem que isso é insuficiente, mas não têm alternativa disponivel.

### Sobre o segmento mais afetado

O problema é sentido com mais intensidade em agências de marketing e times de produto de startups, onde as decisões são frequentes e o impacto de errar é diretamente mensurável (verba de mídia, prazo de entrega, produto que não converte).

---

## 03. Público-alvo

### Quem vivencia o problema?

**Segmento primário (hipótese prioritária para investigar):**

| Atributo                           | Descrição                                                                                              |
| ---------------------------------- | -------------------------------------------------------------------------------------------------------- |
| **Perfis**                   | Gerente/coordenador de marketing, dono de agência, consultor independente, fundador de startup          |
| **Tamanho da organização** | 5 a 200 funcionários (PMEs, agências de médio porte, freelancers)                                     |
| **Contexto de trabalho**     | Tomam decisões sobre campanhas, lançamentos ou conteúdo ao menos mensalmente                          |
| **Budget para pesquisa**     | Não têm budget para pesquisa formal (R$30K+); buscam alternativas mais rápidas e baratas              |
| **O que fazem hoje**         | Intuição, opinião interna, A/B test pós-lançamento, Google Trends, redes sociais, feedback informal |

**Segmento secundário (a confirmar):**

| Atributo                  | Descrição                                                                                  |
| ------------------------- | -------------------------------------------------------------------------------------------- |
| **Perfil**          | Criadores de conteúdo (YouTube, Instagram) com audiência profissional estabelecida         |
| **Dor primária**   | Validar thumbnail, título, formato ou tema antes de produzir e publicar                     |
| **Dor secundária** | Engajamento da audiência com campanhas de marketing ou react de produtos                    |
| **Frequência**     | Semanal: cada vídeo ou post relevante envolve decisões criativas com risco de performance |

### Recorte escolhido para a investigação

Este entregável foca no segmento primário: **profissionais de marketing e fundadores de empresas de 5 a 200 funcionários no Brasil**, que tomam decisões recorrentes sobre campanhas e lançamentos sem acesso a validação de audiência acessível. O segmento enterprise (grandes corporações com budget acima de R$150K para pesquisa) está fora do recorte. Esse segmento já é atendido por players como a [Galaxies](https://www.galaxies.com.br/).

---

## 04. Evidências Secundárias

> Dados, estudos e referências que ajudam a contextualizar e dimensionar o problema.

### O custo e o prazo das alternativas existentes

- Pesquisa de mercado tradicional custa entre **R$30.000 e R$150.000 por projeto** e leva **3 a 4 semanas** para gerar resultados (referência: modelo de precificação da Galaxies e benchmarks da indústria)
- Focus groups têm custo médio de **US$3.000–8.000** por sessão com amostra de apenas 8–12 pessoas
- Recrutamento de públicos especializados (médicos, C-level, nichos de consumo) pode custar **US$150–500 por resposta** em painéis tradicionais
- A indústria global de pesquisa de mercado movimenta **US$142 bilhões** (ESOMAR, 2023), mas o acesso a esse recurso é profundamente desigual entre grandes empresas e o restante do mercado

### A demanda enterprise valida que o problema existe no Brasil

- A Galaxies (São Paulo, fundada em 2022) atende **Nestlé, Boticário, Bradesco Seguros, Banco do Brasil, TikTok e Meta** com personas sintéticas
- Resultados publicados pela Galaxies: **97% de redução no tempo de pesquisa** e **85% de economia em custos** (de R$1M para R$150K por projeto)
- A Galaxies opera exclusivamente no segmento enterprise, com projetos na faixa de **R$150.000+** — excluindo 95%+ do mercado potencial
- Nenhum player brasileiro oferece solução self-service acessível para PMEs e agências

### O mercado reconhece o gap, mas não o fecha

- Internacionalmente, a Aaru (EUA) atingiu valuation de **US$1 bilhão** em dezembro de 2025 resolvendo o mesmo problema no mercado americano
- A YouGov adquiriu a Yabble (plataforma de audiências sintéticas) por **£4,5 milhões** em agosto de 2024 — validando o valor da categoria
- **Dados sintéticos representarão mais de 50% dos inputs de pesquisa de mercado até 2027** (projeção de analistas do setor)
- O custo de inferência de LLMs caiu **78% em 2025** — o que viabiliza soluções acessíveis com margem saudável

### O que as alternativas atuais não resolvem

| Alternativa atual                  | Por que não resolve o problema                                         |
| ---------------------------------- | ----------------------------------------------------------------------- |
| Google Analytics / Meta Ads        | Mostra o que já aconteceu, não o que vai acontecer                    |
| A/B test                           | Funciona após o lançamento — o erro já custou mídia                |
| Opinião interna da equipe         | Viés de confirmação; não representa o público real                 |
| Pesquisa de mercado formal         | Cara demais (R$30K+) e demorada (3–4 semanas) para o ritmo de decisão |
| Focus group                        | Custo alto, amostra pequena, demorado para recrutar                     |
| Planilhas e benchmarks históricos | Dados do passado, não simulação de cenário novo                     |

**Fontes:**

- ESOMAR — Global Market Research 2025
- Galaxies — [Site oficial](https://www.galaxies.com.br/) e [Google Cloud Case](https://cloud.google.com/customers/intl/pt-br/galaxies)
- TechCrunch — [Aaru raised a Series A at $1B valuation](https://techcrunch.com/2025/12/05/ai-synthetic-research-startup-aaru-raised-a-series-a-at-a-1b-headline-valuation/)
- Ditto — [Synthetic Research Platforms: 2026 Market Map](https://askditto.io/news/synthetic-research-platforms-the-2026-market-map)
- Bain & Company — [How Synthetic Customers Bring Companies Closer](https://www.bain.com/insights/how-synthetic-customers-bring-companies-closer-to-the-real-ones/)

---

## 05. Evidências Primárias

> O que foi aprendido com entrevistas e conversas exploratórias com o público.
> **Esta seção será preenchida após a realização das entrevistas de campo.**
> Roteiro disponível em `roteiro-de-pesquisa.md`.

### Status da coleta

| Etapa                                     | Status     |
| ----------------------------------------- | ---------- |
| Definição de perfis a entrevistar       | Concluído |
| Recrutamento de entrevistados             | Pendente   |
| Realização das entrevistas (meta: 5–8) | Pendente   |
| Análise e consolidação dos achados     | Pendente   |

### O que precisamos aprender com o campo

- [ ] O problema é sentido como real e recorrente, ou as pessoas já se adaptaram e não o percebem como dor?
- [ ] Com que frequência a situação acontece?
- [ ] Qual é o impacto concreto que as pessoas conseguem narrar (tempo, dinheiro, cliente perdido)?
- [ ] O que as pessoas fazem hoje para contornar o problema?
- [ ] Já tentaram alguma ferramenta ou serviço? Por que não continuaram?
- [ ] Há disposição percebida para pagar por uma solução rápida e acessível?

### Perfis a entrevistar

- [ ] Gerente ou coordenador de marketing (empresa de 20–200 funcionários)
- [ ] Dono ou sócio de agência de marketing ou publicidade
- [ ] Consultor ou freelancer de estratégia/marketing
- [ ] Fundador de startup em estágio inicial
- [ ] Profissional de e-commerce ou D2C responsável por campanhas

### Template de registro (a preencher por entrevista)

**Entrevistado:** [perfil, sem nome]
**Data:** ___/___/______

**A dor foi confirmada?** [ ] Sim [ ] Parcialmente [ ] Não**Frequência relatada:****Impacto concreto mencionado:****O que faz hoje no lugar:****Citações diretas (palavras exatas):**

> " "

**O que surpreendeu:**

---

### Consolidação pós-entrevistas (a preencher)

**Total de entrevistados:** ___
**% que confirmaram a dor:** ___%

| Padrão identificado | Quantos mencionaram | Citação representativa |
| -------------------- | ------------------- | ------------------------ |
|                      |                     |                          |
|                      |                     |                          |
|                      |                     |                          |

**Hipóteses confirmadas:**
-----------------------

**Hipóteses refutadas ou ajustadas:**
----------------------------------

---

## 06. Síntese e Recorte

> O que foi validado, refutado ou ajustado, e qual problema seguirá para a próxima etapa.
> **Esta seção será preenchida após cruzar desk research com evidências primárias.**

### O que mudou em relação à percepção inicial

*(Preencher após as entrevistas)*

### Declaração refinada do problema

*(Reescrever com base nas evidências coletadas)*

> "Quando [contexto específico], [segmento delimitado] precisa [tarefa concreta], mas [obstáculo real], o que resulta em [consequência mensurável]."

### Recorte final

- **Problema:** *(a definir)*
- **Público:** *(a confirmar)*
- **Contexto:** *(a confirmar)*
- **O que está dentro do escopo:** *(a definir)*
- **O que está fora do escopo:** *(a definir)*

### O que este entregável alimenta no TCC

Este entregável contribui diretamente para as **Seções 1 e 2 do Business Deck** e orienta a construção da **Proposta de Valor na Aula 02**.

---

## Checklist de conclusão (FIAP)

Antes de considerar o entregável concluído:

- [ ] A dor está claramente descrita?
- [ ] O público-alvo e o recorte estão definidos?
- [ ] As principais hipóteses iniciais foram registradas?
- [ ] Há evidências secundárias relevantes com fontes identificadas?
- [ ] O grupo coletou evidências diretamente com pessoas relacionadas ao problema?
- [ ] Está claro o que foi aprendido, confirmado, refutado ou ajustado?
- [ ] O recorte final do problema está fundamentado nas evidências?

---

## O que NÃO entra neste entregável

Para manter o foco na investigação do problema:

- Detalhar funcionalidades da solução ou do produto
- Construir um Business Model Canvas completo
- Definir monetização, projeções financeiras ou go-to-market
- Tentar provar que a ideia original está certa
- Apresentar dados de mercado sem conectá-los ao problema investigado

---

## Timeline de execução (15 dias)

| Dias   | Atividade                                                                            | Status     |
| ------ | ------------------------------------------------------------------------------------ | ---------- |
| 1–2   | Formular a dor inicial, delimitar o público e definir 2–3 hipóteses prioritárias | Concluído |
| 3–5   | Desk research — dados e referências ligados às hipóteses                         | Concluído |
| 4–9   | Entrevistas e conversas exploratórias com o público                                | Pendente   |
| 9–11  | Cruzar achados do desk research com evidências de campo                             | Pendente   |
| 12–13 | Refinar o problema, o público e o contexto com base nas evidências                 | Pendente   |
| 14–15 | Estruturar o entregável final e revisão de coerência                              | Pendente   |
