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

## 04. Desk research

Nessa sessão, vamos aprofundar o estudo para áreas ainda não exploradas. Queremos entender o mercado que estamos situados, a fatia que conseguiriamos alcançar inicialmente, e para quais verticais de mercado podemos extrapolar a solução. Esse estudo será fundamental para criarmos uma visão de longo prazo do negócio e quais são os primeiros passos pensando na proposta de valor imediata.

### Dimensionamento de Mercado (TAM SAM SOM)

#### Total Addressable Market (TAM)

A indústria global de pesquisa de mercado e insights movimentou **US$ 142 bilhões em 2023** (crescimento de 8% YoY), segundo a ESOMAR. O setor de research software cresceu 12,4% e o de reporting 6,5%, indicando que a camada tecnológica cresce mais rápido que o mercado base.

Analistas projetam que **dados sintéticos representarão mais de 50% dos inputs de pesquisa de mercado até 2027**.

O mercado de avatares e agentes IA está projetado para crescer de **US$ 0,8 bi (2025) para US$ 5,93 bi (2032)** CAGR de 33,1%.

#### Serviceable Addressable Market (SAM)

O SAM para uma plataforma de audência sintética inclui:
- Empresas que gastam com pesquisa de mercado terceirizada
- Agências de marketing e publicidade
- Times de produto/UX em empresas de tecnologia
- Consultorias de estratégia

Considerando que o segmento de research software + synthetic data representa ~5-8% do TAM global, o SAM estimado fica entre **US$ 7-11 bilhões globalmente**.

#### Serviceable Obtainable Market (SOM)

Para uma startup entrando pelo mercado brasileiro e latino-americano, com foco inicial em PMEs e agências:
- América Latina representa ~2-3% do mercado global de pesquisa
- Meta realista de captura no primeiro ano: 0,01-0,05% do SAM regional
- **SOM estimado: US$ 500K - US$ 2M ARR nos primeiros 24 meses**

**Fontes:**
- ESOMAR: [Drivers of our $142bn Insights Industry](https://researchworld.com/articles/drivers-of-our-142bn-insights-industry)
- ESOMAR: [Global Market Research 2025](https://esomar.org/publications/global-market-research-2025)
- Ditto: [Synthetic Research Platforms: 2026 Market Map](https://askditto.io/news/synthetic-research-platforms-the-2026-market-map)
- Bain & Company: [How Synthetic Customers Bring Companies Closer](https://www.bain.com/insights/how-synthetic-customers-bring-companies-closer-to-the-real-ones/)

### Análise Competitiva

#### Tier 1: Estabelecidos com funding relevante

| Empresa | Valuation / Funding | Diferencial | Preço |
|---|---|---|---|
| **Aaru** | US$ 1B valuation, US$50M+ Series A (dez/2025) | Simulação de populações sintéticas, predição eleitoral | ARR < US$10M, clientes: Accenture, EY, IPG |
| **Synthetic Users** | Não divulgado | Multi-agent + OCEAN + RAG, qualitativo profundo | US$2-60/entrevista |
| **Yabble** (YouGov) | Adquirida por £4,5M (ago/2024) | "Virtual Audiences", integrada ao ecossistema YouGov | Enterprise |

#### Tier 2: Especializados

| Empresa | Sede | Diferencial | Preço |
|---|---|---|---|
| **Minds** | Berlim/SF | Painéis multi-persona (5-50+ minds), GDPR-native | Customizado |
| **Lakmoos** | Alemanha | IA neuro-simbólica, 98%+ similaridade, indústrias reguladas | Customizado |
| **Evidenza** | EUA | Enterprise full-service em 72h, ex-LinkedIn B2B Institute | Customizado |
| **SimSurveys** | — | End-to-end survey + respondentes sintéticos | Customizado |

#### Tier 3: Entrantes e nichos

| Empresa | Diferencial | Preço |
|---|---|---|
| **Artificial Societies** | Simulações ilimitadas | US$40/mês |
| **OpinioAI** | Surveys + focus groups sintéticos, base na Rep. Tcheca | A partir de €99/mês |
| **Delve AI** | Personas para marketing baseadas em analytics | Freemium |
| **Ditto, Simile, SYMAR** | Pure-play synthetic, variados | Customizado/Demo |
| **Personia** | Digital twins, suporte PT/ES/EN para LatAm | Customizado |

###  Concorrentes no Brasil

#### Galaxies: Potencial concorrente direto

| Atributo | Detalhe |
|---|---|
| **Sede** | São Paulo, Brasil |
| **Fundação** | 2022 |
| **CEO** | Daniel Victorino |
| **Produto** | Plataforma de inteligência preditiva com personas sintéticas ("Nexus") |
| **Clientes** | Nestlé, Boticário, Bradesco Seguros, Banco do Brasil, TikTok, Meta, Logitech |
| **Resultados publicados** | 97% de redução no tempo de pesquisa; 85% de economia em custos (de R$1M para R$150K/projeto) |
| **Backing** | Google for Startups, NVIDIA Inception Program, Selo Cubo Itaú, vencedora do ITEC (China) |
| **Funding** | HSR Specialist Researchers adquiriu participação (valor não divulgado) |
| **Preço** | Não público, modelo enterprise (demo required). Projetos na faixa de R$150K+ |
| **Posicionamento** | Se autodefine como "primeira empresa no mundo a inovar com Personas Sintéticas" |
| **Setores** | Farmacêutico, entretenimento, bens de consumo, financeiro |

**Pontos fortes da Galaxies:**
- Base de clientes enterprise consolidada com marcas de peso
- Validação do Google Cloud e NVIDIA
- Resultados quantificados e publicados (97% menos tempo, 85% menos custo)
- Presença em hub de inovação (Cubo Itaú)
- Experiência em dados do consumidor brasileiro

**Vulnerabilidades da Galaxies (oportunidades para o Synthesis):**
- Modelo exclusivamente enterprise, sem tier self-service acessível
- Sem plano para PMEs, agências médias, startups ou freelancers
- Pricing na faixa de R$150K+ por projeto exclui 95%+ do mercado potencial
- Produto fechado, sem API pública documentada
- Não opera como SaaS self-service (requer demo e implementação assistida)

#### Outros players com presença no Brasil (não brasileiros)

| Empresa | Origem | Presença no Brasil |
|---|---|---|
| **Toluna** | Global (Londres) | Personas sintéticas ativas no Brasil como um dos mercados lançados, integradas à plataforma HarmonAIze |
| **Personia** | Internacional | Suporte PT-BR, digital twins, concept tests com 1000+ usuários sintéticos em minutos |
| **NVIDIA (Nemotron-Personas-Brazil)** | EUA | Dataset aberto de **6 milhões de personas sintéticas brasileiras** baseado em dados do IBGE, desenvolvido com a WideLabs. Disponível para qualquer empresa usar como base |

### O que as alternativas atuais não resolvem

| Alternativa atual                  | Por que não resolve o problema                                         |
| ---------------------------------- | ----------------------------------------------------------------------- |
| Google Analytics / Meta Ads        | Mostra o que já aconteceu, não o que vai acontecer                    |
| A/B test                           | Funciona após o lançamento, o erro já custou tempo e dinheiro                |
| Opinião interna da equipe         | Viés de confirmação; não representa o público real                 |
| Pesquisa de mercado formal         | Cara demais (R$30K+) e demorada (3-4 semanas) para o ritmo de decisão |
| Focus group                        | Custo alto, amostra pequena, demorado para recrutar                     |
| Planilhas e benchmarks históricos | Dados do passado, não simulação de cenário novo                     |

**Fontes:**

- ESOMAR: Global Market Research 2025
- Galaxies: [Site oficial](https://www.galaxies.com.br/) e [Google Cloud Case](https://cloud.google.com/customers/intl/pt-br/galaxies)
- TechCrunch: [Aaru raised a Series A at $1B valuation](https://techcrunch.com/2025/12/05/ai-synthetic-research-startup-aaru-raised-a-series-a-at-a-1b-headline-valuation/)
- Ditto: [Synthetic Research Platforms: 2026 Market Map](https://askditto.io/news/synthetic-research-platforms-the-2026-market-map)
- Bain & Company: [How Synthetic Customers Bring Companies Closer](https://www.bain.com/insights/how-synthetic-customers-bring-companies-closer-to-the-real-ones/)
- TechCrunch: [Aaru raised a Series A at $1B valuation](https://techcrunch.com/2025/12/05/ai-synthetic-research-startup-aaru-raised-a-series-a-at-a-1b-headline-valuation/)
- Uxia: [12 Best Synthetic Users Tools 2025](https://www.uxia.app/blog/synthetic-users-tools)
- Minds: [Best Synthetic User Research Platforms 2026](https://getminds.ai/blog/best-synthetic-user-research-platforms)
- Personia: [AI Market Research with Synthetic Users](https://site.personia.ai/)
- Galaxies: [Site oficial](https://www.galaxies.com.br/)
- Economia SP: [Startup revolucionando pesquisas com personas sintéticas](https://economiasp.com/2025/06/23/como-essa-startup-esta-revolucionando-pesquisas-de-mercado-com-personas-sinteticas/)
- Google Cloud: [Case Galaxies](https://cloud.google.com/customers/intl/pt-br/galaxies?hl=pt-BR)
- GVAngels: [Case Galaxies](https://gvangels.com.br/blog/postagem/galaxies)
- ABC da Comunicação: [Galaxies impulsionada pelo Google for Startups](https://www.abcdacomunicacao.com.br/de-startup-promissora-a-referencia-galaxies-gera-economia-de-85-para-os-clientes-apos-ser-impulsionada-pelo-google-for-startup/)
- NVIDIA: [Nemotron-Personas-Brazil](https://beta.hyper.ai/en/stories/7d0bdfd7adc69f7660bdf800ed0b305e)
- Toluna: [Synthetic Personas](https://tolunacorporate.com/ai-and-innovation/ai-is-everywhere/harmonaize/)
---

### Barreiras de Entrada e Defensibilidade (Moat)

#### O que não é moat em 2026

- **Acesso a LLMs**: Qualquer um pode usar APIs de Claude, GPT, Gemini, etc. O modelo não é diferencial.
- **Features de UI**: Podem ser replicadas em dias com Agentic engineering/vibe coding.
- **Prompt engineering**: Templates de prompt são commodities.

#### O que é defensível

| Tipo de Moat | Descrição | Prioridade |
|---|---|---|
| **Dados proprietários** | Cada pesquisa gera dados que melhoram as personas. Flywheel: mais pesquisas → personas mais precisas → mais clientes → mais pesquisas. | Alta |
| **Integração profunda** | Quanto mais o cliente usa, mais caro trocar (dados históricos, templates, configurações). | Alta |
| **Foco geográfico/cultural** | Personas calibradas para o consumidor brasileiro/LATAM que concorrentes globais não replicam facilmente. | Média/Alta |
| **Marca e confiança** | Em pesquisa de mercado, confiança nos dados é tudo. Publicar benchmarks de acurácia constrói credibilidade. | Média |
| **Velocidade de execução** | Estar no mercado antes dos concorrentes globais localizarem para PT-BR. Risco baixo a priori. | Média |
| **Compliance LGPD** | Ser nativamente LGPD enquanto concorrentes focam em GDPR. | Média |

**Fontes:**
- BuildMVPFast: [AI Wrapper Startup: Build a Defensible Business 2026](https://www.buildmvpfast.com/blog/ai-wrapper-startup-defensible-business-2026)
- Flybridge: [Building Defensibility in Vertical SaaS with Proprietary Data](https://www.flybridge.com/ideas/the-bow/building-defensibility-in-vertical-saas-with-proprietary-data-y5ehh)
- TechCrunch: [Investors spill what they aren't looking for in AI SaaS](https://techcrunch.com/2026/03/01/investors-spill-what-they-arent-looking-for-anymore-in-ai-saas-companies/)

### Riscos e Mitigações

| Risco | Probabilidade | Impacto | Mitigação |
|---|---|---|---|
| **Galaxies expande para mid-market** | Média | Alto | Velocidade de execução, self-service como diferencial, pricing acessível desde o dia 1 |
| **Concorrente global entra no Brasil** | Alta | Alto | Foco cultural/LGPD, integração local, relacionamento com mercado BR |
| **Custos de LLM sobem** | Baixa | Alto | Arquitetura multi-model, cache agressivo, modelos open-source como fallback |
| **Custos de LLM caem (commoditização)** | Alta | Médio | Bom para margens, mas reduz barreira de entrada. Investir em dados proprietários |
| **Desconfiança na acurácia** | Média | Alto | Publicar benchmarks, posicionar como "hipótese rápida" não substituto |
| **Colapso de diversidade das personas** | Média | Médio | Técnicas de diversificação, calibração com dados reais do mercado brasileiro |
| **Regulamentação restritiva de IA** | Média | Médio | Compliance proativo, transparência sobre natureza sintética dos dados |
| **Churn alto** | Alta | Alto | Feedback loops, integração profunda, dados persistentes do cliente |

## 05. Pesquisas e entrevistas

> O que foi aprendido com entrevistas e conversas exploratórias com o público.
> **Esta seção será preenchida após a realização das entrevistas de campo.**
> Roteiro disponível em `roteiro-de-pesquisa.md`.

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

---