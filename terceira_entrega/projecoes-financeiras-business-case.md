# Entrega 3 — Projeções Financeiras e Business Case

> Planilha de apoio: [FIAP_Modelo_Projecao_Financeira_MVP_Synthesis.xlsx](FIAP_Modelo_Projecao_Financeira_MVP_Synthesis.xlsx) (cópia da planilha FIAP com as células de entrada preenchidas; fórmulas e abas originais intactas).
> Insumos: [Estudo de mercado](../docs/estudo-de-mercado.md), [Proposta de valor](../segunda_entrega/proposta-valor.md), [Canvas](../segunda_entrega/CANVAS.pdf) e a pesquisa de validação (20 respondentes, ago/2026).

---

## 1. Resumo executivo

O Synthesis é um SaaS self-service de simulação de reação de audiência com personas sintéticas calibradas para o Brasil. A lógica econômica proposta é:

- **Monetização:** assinatura mensal por **conta/workspace** que dá um saldo de **créditos** (moeda interna, nome a definir), usados livremente em estudos simples ou complexos. Quem estoura o saldo pode **opcionalmente** comprar pacotes extras. Há também **plano anual** (com vantagens), pago antecipadamente.
- **Planos (preço inicial, a validar):** Starter R$ 79, Pro R$ 249 e uma faixa de topo **a partir de R$ 399, sob orçamento**.
- **Capital:** cenário principal com **capital próprio de R$ 90 mil**, liberado em três parcelas, **sem pró-labore para os sócios no ano 1** (os sócios mantêm renda própria). Seed como cenário alternativo.
- **Resultado (cenário base, modelo mensal de 36 meses):** receita de R$ 25 mil, R$ 292 mil e R$ 796 mil nos anos 1, 2 e 3; EBITDA mensal sustentadamente positivo a partir do mês 18; caixa mínimo de R$ 56 mil (mês 17), coberto pelo aporte com folga de R$ 34 mil; capital recuperado no mês 29.
- **Pontos de atenção:**
  1. O crescimento de novos clientes é a variável que mais pesa: com metade dos novos clientes, o EBITDA do ano 3 fica negativo.
  2. A planilha compartilhada traz uma inconsistência de fórmula que **subestima a receita dos anos 2 e 3** (seção 7.2). Lida AS IS, ela mostra o ano 3 com EBITDA positivo, porém baixo (+R$ 23 mil); com a fórmula corrigida, o mesmo cenário dá +R$ 153 mil.
  3. As premissas de preço, mix, pacotes extras, custo por crédito e CAC **não foram validadas com clientes reais**. A pesquisa dá indício de disposição a pagar, não prova de conversão. Todas as premissas estão registradas no Anexo C, com o efeito de errá-las.

---

## 2. Modelo de monetização

### 2.1 Como o Synthesis cobra

| Elemento | Regra |
|---|---|
| **Unidade de cobrança** | Conta/workspace (não por usuário/assento). Número pequeno de usuários incluído; o limitador real é o saldo de créditos. |
| **Créditos** | Moeda interna do Synthesis. Cada estudo consome créditos proporcionais ao seu custo (um teste rápido de título gasta pouco; um painel grande de personas gasta mais). O cliente escolhe: vários estudos simples ou poucos complexos. |
| **Saldo mensal** | Incluído na mensalidade. **Expira** no fim do ciclo. |
| **Pacotes extras** | Opcionais, comprados à parte. **Acumulam** (não expiram enquanto a conta estiver ativa; no plano anual, durante todo o contrato). Isso reduz o receio de "gastar demais" e incentiva o uso. |
| **Estouro do saldo** | Teto rígido com opt-in: sem pacote extra ativo, as simulações pausam. Alertas aos 80% e 100% do saldo. O cliente nunca recebe cobrança surpresa. |
| **Teste gratuito** | Créditos de boas-vindas **únicos** (não renovam todo mês), sem cartão. Limita o custo do plano gratuito, que é um dos riscos do modelo PLG. |

Por que créditos e não "entrevistas" ou "simulações": o saldo flexível acompanha o custo real de LLM de cada estudo e permite trocar de modelo de IA sem mudar o preço ao cliente. Os créditos expirados também geram receita sem custo associado ("breakage"), o que ajuda a margem.

### 2.2 Planos

| Plano | Mensal | Anual (pague 10, leve 12) | Equivalente/mês no anual | Público |
|---|---|---|---|---|
| **Free** | R$ 0 | — | — | Créditos de boas-vindas únicos, para experimentar |
| **Starter** | R$ 79 | R$ 790 | R$ 65,83 | Criadores de conteúdo e freelancers |
| **Pro** | R$ 249 | R$ 2.490 | R$ 207,50 | Freelancers sênior, analistas de marketing, PMEs |
| **Topo (sob orçamento)** | **A partir de R$ 399** | A partir de R$ 3.990 | A partir de R$ 332,50 | Agências, times de marketing e quem usaria mais que o Pro |

- O **plano anual** é pago antecipadamente, usando ou não. O desconto de 2 meses (16,7%) é uma premissa nossa, a validar. Os créditos mensais do plano seguem expirando no ciclo; os pacotes extras valem durante todo o contrato.
- A **faixa de topo** cobre quem pagaria R$ 300 ou mais (45% da pesquisa). Para o usuário, o convite é "faça um orçamento", **a partir de R$ 399**. As subfaixas internas ficam para uma discussão futura; no modelo financeiro, o piso de R$ 399 é usado como base, uma premissa conservadora (o ticket real será igual ou maior).
- Os nomes Starter e Pro vêm do Canvas.
- **Sobre a faixa sob orçamento:** o diferencial do Synthesis é o self-service, e o estudo de mercado critica a Galaxies justamente por exigir demo e implementação assistida. Para não reintroduzir esse atrito, o preço "a partir de" deve ser público, e o orçamento fica para quem precisa de volume ou condições especiais.
- **Sobre o preço do Pro.** Na pesquisa (n = 20), a disposição a pagar por mês é bimodal: R$ 0 (25%), até R$ 100 (25%), R$ 100–300 (5%), R$ 300–500 (25%) e acima de R$ 500 (20%). Os R$ 249 ficam mais perto do grupo de R$ 300 ou mais do que os R$ 197 anteriores, mas continuam na faixa onde só 5% se posicionaram. Vale testar o preço nos primeiros meses.

### 2.3 Orçamento de inferência por plano

O custo variável principal é o LLM. Para o plano não dar prejuízo ao cliente que usa 100% do saldo, adotamos como regra: **custo de inferência no saldo cheio ≤ 40% da mensalidade**.

| Plano | Mensalidade | Orçamento de inferência (40%) | Equivalente em entrevistas curtas* |
|---|---|---|---|
| Starter | R$ 79 | R$ 32 | 19 a 115 |
| Pro | R$ 249 | R$ 100 | 60 a 362 |
| Topo (a partir de) | R$ 399 | R$ 160 | 97 a 580 |

\* Custo de uma entrevista curta de US$ 0,05 a US$ 0,30 (estudo de mercado, seção 3.1), convertido a R$ 5,50 por dólar (premissa de câmbio a atualizar). A faixa é larga porque o custo por unidade depende do modelo, do cache de prompt e do tamanho do estudo. **O número de créditos de cada plano só pode ser fechado depois de medir o custo real por simulação no MVP.**

---

## 3. Fontes de receita

| Linha na planilha | O que é | Planos | Mapeamento |
|---|---|---|---|
| **Linha 1** | Assinaturas self-service + pacotes extras | Starter e Pro | Ticket médio por conta, novos clientes por mês e churn |
| **Linha 2** | Assinatura da faixa de topo + pacotes extras | A partir de R$ 399 | Ticket médio por conta e média de contas pagantes no ano |
| *Fora da projeção* | Subfaixas internas do topo, API, integrações | Sob orçamento | Potencial de expansão; não entra nos números |

A planilha permite duas linhas de receita recorrente, então os pacotes extras foram embutidos no ticket médio de cada linha em vez de virarem uma terceira linha.

### 3.1 Como o ticket médio foi construído

O ticket é **por conta**. Ele combina a mensalidade média (mix de planos), o efeito do desconto do plano anual e a receita de pacotes extras.

**Linha 1 (Starter e Pro)**

| | Ano 1 | Ano 2 | Ano 3 |
|---|---|---|---|
| Mix de contas Starter / Pro | 35% / 65% | 30% / 70% | 25% / 75% |
| Mensalidade média | R$ 189,50 | R$ 198,00 | R$ 206,50 |
| Contas em plano anual | 20% | 30% | 35% |
| Desconto médio (16,7% × share anual) | 3,3% | 5,0% | 5,8% |
| Mensalidade após desconto | R$ 183,20 | R$ 188,10 | R$ 194,50 |
| Pacotes extras (% da mensalidade) | 10% | 14% | 19% |
| **Ticket médio por conta** | **R$ 202** | **R$ 214** | **R$ 231** |

**Linha 2 (faixa de topo)**

| | Ano 1 | Ano 2 | Ano 3 |
|---|---|---|---|
| Mensalidade-base (piso da faixa) | R$ 399 | R$ 399 | R$ 399 |
| Mensalidade após desconto anual | R$ 385,70 | R$ 379,10 | R$ 375,70 |
| Pacotes extras (contas maiores usam mais) | 20% | 30% | 40% |
| **Ticket médio por conta** | **R$ 463** | **R$ 493** | **R$ 526** |

O mix migra para o Pro e os pacotes ganham peso porque o hábito de uso cresce e as contas descobrem que precisam de mais saldo. **Mix, percentual de extras e adesão ao plano anual são premissas nossas, sem evidência direta.** O mix de 65% no Pro é provavelmente otimista (a pesquisa indica muitos respondentes na faixa até R$ 100, e o Pro subiu para R$ 249); no Anexo C.3, um mix de 50/50 reduz o ticket do ano 1 para R$ 174.

### 3.2 O efeito do plano anual

- **No ticket:** o desconto reduz a receita mensal reconhecida (já incluído acima).
- **No churn:** quem assina o anual só cancela na renovação. Adotamos churn mensal de 9%, 7% e 6% para o plano mensal e o equivalente a 3% ao mês (cerca de 30% de não renovação ao ano) para o anual. O churn combinado fica em 7,8%, 5,8% e 5,0%, que arredondamos para **8%, 6% e 5%**.
- **No caixa:** o anual é recebido antes de a receita ser reconhecida. A planilha FIAP calcula caixa a partir do EBITDA e **não captura esse adiantamento**. Como ordem de grandeza (cobrança distribuída ao longo do ano e 70% de renovação), o adiantamento líquido seria de cerca de R$ 55 mil no ano 2 e R$ 100 mil no ano 3. Não entra nos números abaixo, então é uma folga conservadora. É também uma obrigação de entregar o serviço, não lucro; a política de cancelamento e reembolso do anual (inclusive o prazo legal de arrependimento em compras online) precisa ser validada com jurídico.

---

## 4. Tamanho de mercado (TAM, SAM, SOM)

### 4.1 Top-down

Fonte: [estudo de mercado](../docs/estudo-de-mercado.md), seção 1 (ESOMAR e outros). Câmbio de R$ 5,50 por dólar.

| Camada | Definição | Valor |
|---|---|---|
| **TAM** | Mercado global de pesquisa e insights (2023) | US$ 142 bi |
| **SAM global** | Research software + dados sintéticos (5 a 8% do TAM) | US$ 7 a 11 bi |
| **SAM regional** | América Latina (2 a 3% do mercado global de pesquisa) | US$ 140 a 330 mi (R$ 0,8 a 1,8 bi) |
| **SOM do plano** | MRR de R$ 83,9 mil no fim do ano 3, ou ARR de cerca de R$ 1,0 mi (US$ 183 mil) | 0,06% a 0,13% do SAM regional |

### 4.2 Bottom-up

Parte do nosso modelo: no fim do ano 3, cerca de **341 contas** nos planos Starter e Pro e **10 contas** na faixa de topo, com ticket médio de R$ 231 e R$ 526 por mês. É o SOM do plano: aproximadamente R$ 1,0 mi de ARR.

### 4.3 Leitura

- O SOM do plano é **conservador**: o estudo de mercado estimava US$ 0,5 a 2 mi de ARR em 24 meses (aproximadamente R$ 2,8 a 11 mi), de 3 a 11 vezes acima do que o plano projeta para o fim do ano 3. A diferença vem de partirmos de um MVP sem receita nos 6 primeiros meses, preços de entrada baixos e crescimento essencialmente orgânico.
- **Lacuna:** o top-down usa o mercado global/regional. Falta o recorte do universo brasileiro (número de agências, PMEs com marketing digital e criadores monetizados) a partir de fontes como IBGE, Sebrae e relatórios do setor. Esse levantamento está nos próximos passos; **não foram inventados números** para preencher o campo.

---

## 5. Premissas financeiras

Valores inseridos na planilha (aba Premissas). Os custos são mensais. **O registro completo das premissas, com origem, justificativa, impacto e forma de validação, está no [Anexo C](#anexo-c--registro-de-premissas).**

| Premissa | Ano 1 | Ano 2 | Ano 3 | Base da premissa | Confiança |
|---|---|---|---|---|---|
| Ticket médio Linha 1 | R$ 202 | R$ 214 | R$ 231 | Seção 3.1 | Baixa |
| Novos clientes/mês, Linha 1 | 3 | 16 | 28 | Ano 1: 6 por mês a partir do mês 7 (MVP nos 6 primeiros meses), média de 12 meses de 3 | Baixa |
| Churn mensal combinado | 8% | 6% | 5% | Seção 3.2; público de renda variável | Baixa |
| Ticket médio Linha 2 | R$ 463 | R$ 493 | R$ 526 | Seção 3.1 (piso de R$ 399) | Baixa |
| Contas na faixa de topo (média no ano) | 0,5 | 4 | 10 | Ano 1: 1 conta a partir do mês 7; parceria com agências é canal de aquisição | Baixa |
| COGS (% da receita) | 38% | 33% | 28% | Orçamento de inferência (2.3) e gateway, cloud e custo do trial; cai com cache de prompt, lote e modelos menores | Média-baixa |
| Pessoal | R$ 0 | R$ 7.000 | R$ 14.000 | Sem pró-labore no ano 1; a partir do ano 2, pró-labore escalonado e apoio part-time | Média |
| Marketing e aquisição | R$ 1.000 | R$ 2.500 | R$ 4.500 | Conteúdo, LinkedIn e comunidades (PLG, pouca mídia paga) | Média |
| Vendas e comissões | R$ 0 | R$ 500 | R$ 1.500 | Bônus de parceria com agências | Média |
| Tecnologia (fixa) | R$ 1.200 | R$ 2.500 | R$ 4.000 | Cloud base, observabilidade, ferramentas; o LLM está no COGS | Média |
| Administrativo | R$ 600 | R$ 1.000 | R$ 1.600 | Contador, jurídico e LGPD | Média |
| Impostos s/ receita | 6% | 8% | 10% | Simples Nacional (a confirmar com contador) | Baixa |
| Investimento inicial | R$ 18.000 | — | — | Tecnologia R$ 8 mil, marketing de lançamento R$ 5 mil, abertura da empresa e termos LGPD R$ 5 mil | Média |
| Capital próprio | R$ 90.000 | — | — | Seção 9 | Definição dos sócios |

Observações:

- **Pessoal no ano 1 é zero** porque os sócios têm renda própria e o produto é construído por eles. Isso **não é custo zero**: é custo de oportunidade assumido pelos sócios. Quem lê o plano deve considerar esse subsídio.
- **Impostos:** o regime tributário (Simples Nacional, anexo e fator R) pode elevar a alíquota acima do assumido, em especial no ano 1, quando não há folha de pagamento. Precisa ser validado com contador.
- **COGS** é uma meta, não uma medição. O primeiro marco do MVP é medir o custo real por crédito.

---

## 6. Estrutura de custos

| Tipo | Itens | Comportamento |
|---|---|---|
| **Variáveis (COGS)** | Chamadas de LLM por simulação, taxas do gateway de pagamento, armazenamento e egress, custo dos créditos do teste gratuito | Crescem com o uso; protegidos pelo teto de inferência por plano |
| **Fixos de pessoal** | Pró-labore e apoio part-time | Zero no ano 1; escalonados nos anos 2 e 3 |
| **Aquisição** | Marketing de conteúdo e comunidades, bônus de parceria | Pequenos: o modelo PLG e a indicação orgânica sustentam a aquisição |
| **Fixos de operação** | Cloud base, ferramentas, contador, jurídico/LGPD | Crescem devagar |
| **Investimento inicial** | MVP, marca, abertura da empresa, termos de uso e política de privacidade | R$ 18 mil, no ano 1 |

Dois riscos de custo vêm do estudo de mercado: SaaS de IA tem margem bruta de 25 a 65% (a nossa meta de 62 a 72% é ambiciosa) e heavy users podem custar de 50 a 100 vezes mais que os leves. O teto de inferência por plano e o excedente opcional existem para proteger essa margem.

---

## 7. Projeções

### 7.1 Planilha FIAP (leitura direta)

Resultado da aba **Projeção 3 Anos** com as premissas da seção 5, em R$:

| | Ano 1 | Ano 2 | Ano 3 |
|---|---|---|---|
| Receita Linha 1 | 28.740 | 193.935 | 469.874 |
| Receita Linha 2 | 2.778 | 23.664 | 63.120 |
| **Receita total** | **31.518** | **217.599** | **532.994** |
| COGS | (11.977) | (71.808) | (149.238) |
| **Lucro bruto** | **19.541** | **145.791** | **383.756** |
| Margem bruta | 62% | 67% | 72% |
| Pessoal | 0 | (84.000) | (168.000) |
| Marketing | (12.000) | (30.000) | (54.000) |
| Vendas | 0 | (6.000) | (18.000) |
| Tecnologia | (14.400) | (30.000) | (48.000) |
| Administrativo | (7.200) | (12.000) | (19.200) |
| Impostos | (1.891) | (17.408) | (53.299) |
| **EBITDA** | **(15.950)** | **(33.616)** | **23.256** |
| Margem EBITDA | −51% | −15% | 4% |
| Caixa final (início: R$ 90.000; investimento: R$ 18.000) | 56.050 | 22.433 | 45.689 |

### 7.2 Atenção: a fórmula de receita da Linha 1 subestima os anos 2 e 3

Na aba Premissas, a dica da célula F12 diz que a receita usa "a média entre clientes ativos no início e no fim do ano". Mas as fórmulas de D12 e E12 usam `ticket × clientes_finais / 2 × 12`, ou seja, tratam o início do ano como zero. No ano 1 isso está correto (a base começa em zero). Nos anos 2 e 3, a receita fica subestimada em **12% e 28%**.

**Não alteramos essa fórmula**, pois não é uma célula de entrada. A correção seria `=D8*(C11+D11)/2*12` em D12 e `=E8*(D11+E11)/2*12` em E12. Com ela, as mesmas premissas dão:

| | Planilha como está | Planilha com média corrigida | Modelo mensal (36 meses) |
|---|---|---|---|
| Receita ano 1 / 2 / 3 (R$ mil) | 32 / 218 / 533 | 32 / 248 / 742 | 25 / 292 / 796 |
| EBITDA ano 1 / 2 / 3 (R$ mil) | −16 / −34 / +23 | −16 / −16 / +153 | −20 / +10 / +186 |
| Caixa final ano 1 / 2 / 3 (R$ mil)* | 56 / 22 / 46 | 56 / 40 / 193 | −38 / −27 / +159 |

\* Planilhas partem de R$ 90 mil de capital; o modelo mensal parte de zero (mostra o caixa acumulado antes do aporte).

O **modelo mensal** é a nossa referência de cálculo: parte do lançamento no mês 7, aplica churn mês a mês e permite achar o **caixa mínimo** (o ponto mais fundo do vale da morte), que a planilha anual não mostra. É a base para dimensionar o aporte. Os valores diferem da planilha corrigida porque a planilha distribui os novos clientes de forma uniforme ao longo do ano e o modelo mensal reflete o MVP sem receita nos meses 1 a 6.

**Como ler:** a planilha oficial, lida como está, mostra um ano 3 com lucro baixo por causa da fórmula. Para o business case, a referência é o modelo mensal; a planilha corrigida confirma a ordem de grandeza.

### 7.3 Modelo mensal: cenário base

| | Ano 1 | Ano 2 | Ano 3 |
|---|---|---|---|
| Receita (R$) | 25.095 | 291.788 | 795.999 |
| EBITDA (R$) | (19.547) | 10.155 | 186.320 |
| MRR no fim do ano (R$) | 6.427 | 34.886 | 83.917 |
| Contas Starter/Pro no fim do ano | 30 | 154 | 341 |

- O EBITDA mensal passa a ser **sustentadamente positivo a partir do mês 18**.
- O **caixa mínimo** é de R$ 56 mil, no **mês 17**. Os R$ 90 mil de capital cobrem esse ponto com folga de R$ 34 mil.
- O **payback do capital** (mês em que o caixa acumulado volta a zero) é o **mês 29**.

---

## 8. Indicadores de viabilidade

### 8.1 Indicadores da planilha (aba Dashboard)

| Indicador | Ano 1 | Ano 2 | Ano 3 |
|---|---|---|---|
| MRR médio do ano (receita ÷ 12) | R$ 2.626 | R$ 18.133 | R$ 44.416 |
| ARR (receita anual) | R$ 31.518 | R$ 217.599 | R$ 532.994 |
| Contas Starter/Pro ativas no fim do ano | 24 | 151 | 339 |
| Churn mensal | 8% | 6% | 5% |
| CAC (marketing + vendas ÷ novos clientes) | R$ 333 | R$ 188 | R$ 214 |
| LTV (ticket × margem bruta ÷ churn) | R$ 1.566 | R$ 2.390 | R$ 3.326 |
| LTV/CAC | 4,7 | 12,7 | 15,5 |
| Payback do CAC (meses) | 2,7 | 1,3 | 1,3 |
| Margem bruta | 62% | 67% | 72% |
| EBITDA | −R$ 15.950 | −R$ 33.616 | +R$ 23.256 |
| Runway (meses de caixa) | 42,2 | 8,0 | Caixa gerador |
| Crescimento da receita YoY | — | 590% | 145% |

O "MRR" do dashboard é a receita média mensal do ano. O MRR de fim de ano (seção 7.3) é maior.

### 8.2 CAC honesto

O CAC da planilha considera só marketing e vendas. Como o modelo é PLG (conteúdo, indicação, parcerias), o CAC "de mídia" é baixo. Mas a partir do ano 2 há time dedicado e não é justo ignorar esse custo:

| | Ano 1 | Ano 2 | Ano 3 |
|---|---|---|---|
| CAC de mídia | R$ 333 | R$ 188 | R$ 214 |
| CAC completo (inclui pessoal) | R$ 333 | R$ 625 | R$ 714 |
| LTV/CAC completo | 4,7 | 3,8 | 4,7 |
| Payback do CAC completo (meses) | 2,7 | 4,4 | 4,3 |

A leitura prudente é **LTV/CAC em torno de 4 a 5**, acima da regra de ouro de 3×. O CAC de mídia, muito abaixo disso, depende de a aquisição orgânica funcionar de verdade, o que ainda não foi testado. O CAC do ano 1 é igual nas duas versões porque não há pessoal remunerado (o custo de oportunidade dos sócios não entra).

### 8.3 Ponto de equilíbrio

Receita mensal necessária para cobrir os custos fixos do ano, com margem de contribuição de 56%, 59% e 62%:

| | Ano 1 | Ano 2 | Ano 3 |
|---|---|---|---|
| Custos fixos mensais | R$ 2.800 | R$ 13.500 | R$ 25.600 |
| MRR de equilíbrio | R$ 5.000 | R$ 22.900 | R$ 41.300 |
| Equivalente em contas Starter/Pro | 25 | 107 | 179 |

### 8.4 Retorno

- **Payback do capital:** mês 29 (cenário base).
- **ROI em 36 meses:** o caixa acumulado ao fim de 36 meses é de R$ 159 mil, sobre um capital máximo investido de R$ 56 mil, ou seja, **ROI de cerca de 285%**. Não inclui valor residual do negócio, e depende de o cenário base se realizar.
- **Margem bruta de 62% a 72%:** dentro da faixa de 60 a 80% de referência para SaaS, mas na parte baixa; é a contrapartida do custo de LLM.
- **Churn de 5 a 8% ao mês:** acima do referencial de SaaS B2B (< 3%). É coerente com o público (freelancers e criadores), mas é o segundo ponto de atenção do modelo.

---

## 9. Capital, vale da morte e aporte dos sócios

O "vale da morte" do Synthesis é o período entre o gasto do MVP e a receita cobrir os custos: do lançamento (mês 7) até cerca do mês 18. O ponto mais fundo, no cenário base, ocorre no **mês 17**.

### 9.1 Proposta principal: capital próprio de R$ 90 mil

Todos os sócios mantêm renda própria e **ninguém recebe pró-labore no ano 1**. O aporte é liberado em três parcelas:

| Parcela | Valor | Quando | Condição |
|---|---|---|---|
| 1 | R$ 35 mil | Início | Cobre o investimento inicial (R$ 18 mil) e os custos fixos até o lançamento, com folga de cerca de R$ 3 mil. Para ganhar conforto, antecipar a parcela 2 em um mês ou subir a parcela 1 para R$ 40 mil |
| 2 | R$ 30 mil | Lançamento do MVP (mês 6) | MVP funcional entregue |
| 3 | R$ 25 mil | Mês 12 (reserva) | MRR de pelo menos R$ 3 mil. Se não atingir, os sócios decidem entre cortar custos ao mínimo, pivotar ou encerrar, com o capital já investido limitado |

Cerca de R$ 22,5 mil por sócio, se divididos igualmente. A divisão efetiva é uma decisão dos sócios. As parcelas e as condições são indicativas e precisam ser confirmadas.

### 9.2 Por que R$ 90 mil se sustenta

Aporte necessário = caixa mínimo de cada cenário (modelo mensal, sem capital inicial):

| Cenário | Caixa mínimo (aporte necessário) | Mês | Receita ano 3 | EBITDA ano 3 | Payback |
|---|---|---|---|---|---|
| **Base** | R$ 56 mil | 17 | R$ 796 mil | +R$ 186 mil | Mês 29 |
| Otimista | R$ 37 mil | 8 | R$ 1,29 mi | +R$ 495 mil | Mês 20 |
| Pessimista, com cortes de custo | R$ 60 mil | 20 | R$ 351 mil | +R$ 47 mil | Não ocorre em 36 meses |
| Pessimista, sem cortes | R$ 217 mil | 36 | R$ 351 mil | −R$ 89 mil | — |
| Base com ticket da Linha 1 20% menor | R$ 70 mil | 20 | R$ 650 mil | +R$ 96 mil | Mês 34 |
| Base com 1 sócio em tempo integral (variante 9.3) | R$ 98 mil | 17 | R$ 796 mil | +R$ 186 mil | Mês 31 |

- Os R$ 90 mil cobrem o **base** (folga de R$ 34 mil), o **pessimista com cortes** (folga de R$ 30 mil) e o **ticket 20% menor** (folga de R$ 20 mil).
- O caixa mínimo do base, do otimista e do pessimista com cortes fica abaixo de R$ 65 mil, o total das duas primeiras parcelas. Já o ticket 20% menor (R$ 70 mil) usa um pedaço da parcela 3. É para isso que ela existe como reserva.
- **Sem cortes, o pessimista não se sustenta só com capital próprio.** Por isso o plano exige disciplina: se o MRR ficar abaixo do esperado, congelar o pró-labore do ano 2 e reduzir marketing ao mínimo.
- Como o caixa mínimo do base é de R$ 56 mil, o aporte principal poderia ser menor. Mantivemos R$ 90 mil pela folga nos cenários adversos; reduzir é uma decisão dos sócios.

Premissas do cenário pessimista com cortes: metade dos novos clientes e das contas de topo, churn de 10%, 8% e 7%, e custos reduzidos (pessoal R$ 0, 3,5 mil e 7 mil por mês; marketing R$ 800, 1,5 mil e 2,5 mil). No otimista: 50% mais novos clientes e contas de topo, churn de 6%, 4,5% e 4%.

**Elasticidade ao preço do Pro.** O aumento de R$ 197 para R$ 249 é uma aposta. Se ele afastar 15% dos novos clientes da Linha 1, o ano 3 ainda fecha com receita de R$ 686 mil e EBITDA de +R$ 118 mil (caixa mínimo de R$ 66 mil), então o plano tolera uma queda de conversão dessa ordem.

### 9.3 Variante: um sócio em tempo integral

Se um sócio se dedicar integralmente já no ano 1, com pró-labore de R$ 3,5 mil por mês, o custo extra é de R$ 42 mil por ano. O aporte necessário no base sobe para cerca de **R$ 98 mil**, e a recomendação passa a ser de cerca de **R$ 120 mil**.

### 9.4 Cenário alternativo: plano acelerado com seed

Plano um pouco mais acelerado, com seed de **R$ 150 mil por volta do mês 9**, mais R$ 30 mil de capital próprio inicial:

| | Ano 1 | Ano 2 | Ano 3 |
|---|---|---|---|
| Receita | R$ 25 mil | R$ 385 mil | R$ 1,08 mi |
| EBITDA | −R$ 20 mil | −R$ 38 mil | +R$ 173 mil |

- Premissas: novos clientes de 22 e 38 por mês nos anos 2 e 3; 6 e 14 contas de topo; pessoal de R$ 12 mil e R$ 24 mil por mês; marketing de R$ 5 mil e R$ 8 mil.
- **Esse plano acelerado, por si só, precisa de cerca de R$ 90 mil de capital:** o caixa mínimo é de R$ 60 mil sobre os R$ 30 mil iniciais. Ou seja, ele cabe no mesmo aporte do cenário principal.
- O seed, portanto, **não é necessário para financiar** o plano; ele **substituiria capital próprio**. Com seed de R$ 100 mil no mês 9, os sócios precisariam colocar cerca de R$ 40 mil antes de a rodada fechar (rodadas demoram), e o caixa mínimo seguinte ficaria perto de R$ 40 mil. Com R$ 150 mil, a folga é maior (cerca de R$ 90 mil).
- **Comparação com o cenário principal:** o plano acelerado entrega cerca de R$ 280 mil a mais de receita no ano 3 (R$ 1,08 mi contra R$ 796 mil) com EBITDA parecido (R$ 173 mil contra R$ 186 mil). O que o seed compra é menos capital próprio exigido e mais velocidade, ao custo de diluição societária.
- As entradas para reproduzir esse cenário na planilha estão no Anexo B (ela vai subestimar o ano 3 pelo problema de fórmula descrito em 7.2).

---

## 10. Sensibilidade

EBITDA do ano 3, variando uma premissa por vez (planilha com média corrigida, base de +R$ 153 mil):

| Variação | EBITDA ano 3 |
|---|---|
| Base | +R$ 153 mil |
| Ticket da Linha 1 −20% | +R$ 69 mil |
| COGS +12 p.p. (50%, 45%, 40%) | +R$ 64 mil |
| Churn +4 p.p. (12%, 10%, 8%) | +R$ 64 mil |
| Novos clientes −50% | −R$ 58 mil |

Conclusões:

1. **Preço, custo de LLM e churn, cada um sozinho, reduzem o lucro do ano 3 a menos da metade.** O negócio funciona, mas a margem de segurança não é grande.
2. **A aquisição de clientes é a variável mais crítica.** Com metade dos novos clientes, o ano 3 fica no vermelho mesmo sem outros problemas.
3. Os três primeiros riscos (preço, COGS, churn) são mensuráveis cedo, ainda no MVP.

---

## 11. Conexão com a proposta de valor e o modelo de negócio

| Elemento da proposta de valor (Entrega 2) | Como aparece na lógica financeira |
|---|---|
| **Preço acessível, fora da faixa de pesquisa formal** (barreira de custo: 30%) | Planos de R$ 79 a "a partir de R$ 399", contra projetos de R$ 150 mil ou mais dos concorrentes enterprise (Galaxies) |
| **Velocidade, em horas** (barreira de demora: 35%) | Self-service e PLG: o cliente usa sozinho, sem consultoria, o que mantém o CAC baixo e o time pequeno |
| **Self-service, sem consultoria** | Estrutura de custos enxuta; sem custo de vendas assistidas no ano 1; preço "a partir de" público na faixa de topo |
| **Criador com renda variável** (fricção da jornada do Rafael) | Starter de R$ 79 com excedente opcional e teto rígido: ele paga mais só nos meses em que usa mais, sem surpresa |
| **Loop de feedback** (previsão contra resultado real) | Principal alavanca de retenção; sustenta a redução do churn de 8% para 5% |
| **Parceria com agências** (canal do Canvas) | Linha 2 e o baixo custo de vendas; agências trazem contas de maior ticket |
| **Compliance LGPD** | Custo registrado em administrativo e no investimento inicial |

O Canvas já previa assinatura mensal por perfil de uso e um modelo por créditos para criadores independentes; a proposta aqui unifica as duas ideias: todos os planos têm assinatura com saldo de créditos e pacote extra opcional.

**Expansão possível (fora das projeções):** subfaixas internas do topo, plano com SLA e API, integrações com ferramentas brasileiras (RD Station, Hotmart) e revenda para agências.

---

## 12. Riscos e limitações

| Risco | Efeito | Mitigação |
|---|---|---|
| Premissas de preço, mix, extras e adesão ao anual não validadas | Receita pode ficar 20% ou mais abaixo | Testar preços no lançamento (inclusive o Pro de R$ 249) |
| Custo real do LLM por crédito desconhecido | Margem bruta menor que 62 a 72% | Medir no MVP; cache de prompt, processamento em lote, modelos menores na triagem; teto de inferência por plano |
| Crescimento orgânico abaixo do esperado | Maior sensibilidade do modelo (seção 10) | Gatilhos de corte; reforço do canal de agências |
| Churn maior que o modelado | LTV menor | Plano anual, loop de feedback, dashboard de acurácia |
| Faixa sob orçamento reintroduz atrito de venda | Contradiz o diferencial self-service e pode atrasar a conversão | Preço "a partir de" público; orçamento só para volumes maiores |
| Ceticismo sobre dados sintéticos | Conversão baixa do trial | Transparência metodológica, cases com acurácia verificável |
| Concorrência (Galaxies no topo, global no entry) | Pressão de preço | Posição de self-service acessível e foco no Brasil |
| Plano gratuito consome custo de LLM | Margem do ano 1 | Créditos de boas-vindas únicos |
| Regime tributário e fator R | Impostos acima de 6% | Validar com contador |
| Fórmula da planilha subestima receita (7.2) | Resultado anual da planilha pior que o real | Reportado; fórmula corrigida mostrada em paralelo |
| Pesquisa com apenas 20 respondentes | Indício de disposição a pagar, não prova | Ampliar a amostra e validar com pré-vendas |
| Capital próprio dos sócios | Plano depende do aporte de R$ 90 mil | Parcelas condicionadas; cenário alternativo de seed |

---

## 13. Pendências e próximos passos

**Definições em aberto**

- Nome da moeda interna (créditos).
- Número de créditos de cada plano e custo por crédito (depende de medir o custo por simulação).
- Subfaixas internas da faixa de topo (hoje só existe o piso de R$ 399).
- Política de cancelamento e reembolso do anual.
- Política dos pacotes extras ao cancelar a assinatura.
- Se os créditos mensais do plano anual seguem expirando todo mês (premissa atual).
- Regime tributário.
- Se o mix de planos do cenário base continua em 35/65 ou passa a um valor mais prudente, como 50/50 (Anexo C.3).

**Para validar**

- Pré-venda ou teste de preço com respondentes da pesquisa (principalmente o Pro de R$ 249).
- Recorte brasileiro de TAM, SAM e SOM (IBGE, Sebrae, relatórios do setor).
- Custo real de inferência no MVP.
- Aplicar, ou não, a correção de fórmula da planilha com a professora (7.2).

---

## Anexo A — Mapa de preenchimento da planilha

Aba **Premissas**, apenas as células amarelas de entrada (todas as fórmulas e as demais abas permanecem como no original).

| Linha | Campo | Ano 1 | Ano 2 | Ano 3 |
|---|---|---|---|---|
| 7 | Descrição da receita (Linha 1) | Assinatura Starter/Pro + pacotes extras | idem | idem |
| 8 | Ticket médio (R$) | 202 | 214 | 231 |
| 9 | Novos clientes por mês | 3 | 16 | 28 |
| 10 | Churn mensal | 8% | 6% | 5% |
| 15 | Descrição da receita (Linha 2) | Assinatura faixa de topo (a partir de R$ 399) + extras | idem | idem |
| 16 | Ticket médio (R$) | 463 | 493 | 526 |
| 17 | Média de clientes pagantes | 0,5 | 4 | 10 |
| 23 | Pessoal (R$/mês) | 0 | 7.000 | 14.000 |
| 24 | Marketing (R$/mês) | 1.000 | 2.500 | 4.500 |
| 25 | Vendas e comissões (R$/mês) | 0 | 500 | 1.500 |
| 26 | Tecnologia (R$/mês) | 1.200 | 2.500 | 4.000 |
| 27 | Administrativo (R$/mês) | 600 | 1.000 | 1.600 |
| 28 | Impostos sobre receita | 6% | 8% | 10% |
| 33 | Investimento em tecnologia (R$) | 8.000 | 0 | 0 |
| 34 | Investimento em marketing (R$) | 5.000 | 0 | 0 |
| 35 | Outros investimentos (R$) | 5.000 | 0 | 0 |
| 37 | Capital próprio (R$) | 90.000 | 0 | 0 |
| 38 | Captação externa (R$) | 0 | 0 | 0 |
| 41 | COGS (% da receita) | 38% | 33% | 28% |

O capital próprio de R$ 90 mil entra inteiro na linha 37 (ano 1), embora seja liberado em parcelas; a planilha não modela parcelas.

## Anexo B — Entradas para reproduzir o cenário acelerado com seed na planilha

Trocar na aba Premissas (demais células como no Anexo A). A planilha vai subestimar o ano 3 pelo problema descrito em 7.2.

| Linha | Campo | Ano 1 | Ano 2 | Ano 3 |
|---|---|---|---|---|
| 9 | Novos clientes por mês | 3 | 22 | 38 |
| 17 | Média de contas de topo | 0,5 | 6 | 14 |
| 23 | Pessoal (R$/mês) | 0 | 12.000 | 24.000 |
| 24 | Marketing (R$/mês) | 1.000 | 5.000 | 8.000 |
| 25 | Vendas (R$/mês) | 0 | 1.000 | 2.500 |
| 26 | Tecnologia (R$/mês) | 1.200 | 3.000 | 5.000 |
| 27 | Administrativo (R$/mês) | 600 | 1.100 | 1.800 |
| 37 | Capital próprio (R$) | 30.000 | 0 | 0 |
| 38 | Captação externa (R$) | 150.000 | 0 | 0 |

## Anexo C — Registro de premissas

Este anexo reúne **todas as premissas** do business case em um só lugar, com a origem de cada uma, a justificativa, o que acontece se ela estiver errada e como validá-la. A seção 5 mostra os valores inseridos na planilha; aqui está o raciocínio por trás deles.

### C.1 Como ler

**Origem**
- **Dado:** vem de uma fonte citada (estudo de mercado, pesquisa de validação, material da disciplina).
- **Benchmark:** referência de mercado usada como ponto de partida.
- **Decisão do grupo:** definida pelos sócios.
- **Estimativa nossa:** hipótese sem evidência direta; precisa de validação.

**Confiança:** Alta (dado verificável), Média (benchmark ou decisão com respaldo), Baixa (estimativa sem evidência).

**Premissas de confiança baixa que mais movem o resultado:** mix de planos (P03), pacotes extras (P05), novos clientes por mês (P08), churn (P09) e COGS (P12). A seção C.3 mostra o efeito de errá-las.

### C.2 Registro

**A. Preço e receita**

| ID | Premissa e valor | Origem | Justificativa | Confiança | Como validar |
|---|---|---|---|---|---|
| P01 | Planos: Starter R$ 79, Pro R$ 249, topo a partir de R$ 399 (sob orçamento) | Decisão do grupo | O estudo de mercado propunha Starter R$ 197 e Pro R$ 497. O benchmark de entrada (Artificial Societies, US$ 40 por mês, cerca de R$ 220) é maior que o nosso Starter. O Starter de R$ 79 mira os 25% da pesquisa que gastam até R$ 100; o topo mira os 45% que pagariam R$ 300 ou mais | Média | Teste de preço e pré-venda com respondentes da pesquisa |
| P02 | Plano anual: pague 10, leve 12 (desconto de 16,7%), pago antecipadamente | Decisão do grupo | Desconto comum em SaaS; compra fidelidade e caixa antecipado | Média | Medir a adesão real ao anual |
| P03 | Mix de contas Starter/Pro: 35/65, 30/70 e 25/75 nos anos 1, 2 e 3 | Estimativa nossa | Supõe que o hábito de uso empurra as contas para o Pro. **Não há evidência.** Na pesquisa, metade gasta até R$ 100 ou nada, o que sugere mais contas no Starter; e o Pro subiu de R$ 197 para R$ 249 sem que o mix fosse refeito. **Provavelmente é otimista.** | Baixa | Distribuição real de planos no lançamento |
| P04 | Adesão ao plano anual: 20%, 30% e 35% das contas | Estimativa nossa | Crescimento gradual da confiança no produto | Baixa | Medir a adesão |
| P05 | Pacotes extras como % da mensalidade: Linha 1 com 10%, 14% e 19%; topo com 20%, 30% e 40% | Estimativa nossa | Contas maiores e mais maduras usam mais saldo. Sem dado de consumo | Baixa | Consumo real de créditos no MVP |
| P06 | Piso do topo: R$ 399 usado como mensalidade-base | Decisão do grupo | Conservador: o ticket real será igual ou maior. Subfaixas ficam para o futuro | Média | Orçamentos reais |
| P07 | Contas do topo (média no ano): 0,5, 4 e 10 | Estimativa nossa | Ano 1: 1 conta a partir do mês 7, via parceria com agências | Baixa | Pipeline de agências |

**B. Volume e retenção**

| ID | Premissa e valor | Origem | Justificativa | Confiança | Como validar |
|---|---|---|---|---|---|
| P08 | Novos clientes pagantes por mês na Linha 1: 6 (a partir do mês 7), 16 e 28. Na planilha, a média de 12 meses do ano 1 é 3 | Estimativa nossa | Informada diretamente, **sem funil modelado**. Com conversão de 5% do trial para pago (benchmark não validado), isso exige cerca de 120, 320 e 560 cadastros por mês | Baixa | Funil real: visitas, cadastros, conversão |
| P09 | Churn mensal: plano mensal 9%, 7% e 6%; plano anual equivalente a 3% (cerca de 30% de não renovação ao ano). Combinado: 8%, 6% e 5% | Estimativa nossa | Público de renda variável (freelancers e criadores). O referencial de SaaS B2B é menor que 3% | Baixa | Coortes reais |
| P10 | Lançamento no mês 7; os 6 primeiros meses (MVP) sem receita | Decisão do grupo | Alinhado ao 5W2H (MVP em 6 meses) | Média | Cronograma de desenvolvimento |
| P11 | Entrada de clientes constante ao longo de cada ano; churn constante; custos mudam em degrau no início de cada ano (modelo mensal) | Simplificação | Torna o modelo transparente; a realidade é irregular | Média | Comparar com o realizado |

**C. Custos**

| ID | Premissa e valor | Origem | Justificativa | Confiança | Como validar |
|---|---|---|---|---|---|
| P12 | COGS: 38%, 33% e 28% da receita. Regra de projeto: inferência no saldo cheio ≤ 40% da mensalidade | Estimativa nossa, com base em dado | Custo de LLM de US$ 0,05 a 0,30 por entrevista curta (estudo de mercado). Cai com cache de prompt, lote e modelos menores. Inclui gateway, cloud e o custo do teste gratuito | Baixa | Medir o custo por crédito no MVP |
| P13 | Câmbio: R$ 5,50 por dólar | Estimativa nossa | Só converte o custo de LLM e o mercado em dólar | Média | Cotação atual |
| P14 | Pessoal: R$ 0, 7 mil e 14 mil por mês | Decisão do grupo, com estimativa nossa | Ano 1 sem pró-labore (sócios com renda própria). A partir do ano 2, pró-labore escalonado e apoio part-time. **O custo de oportunidade dos sócios não entra** | Média | Decisão dos sócios |
| P15 | Marketing: R$ 1 mil, 2,5 mil e 4,5 mil por mês. Vendas: R$ 0, 500 e 1,5 mil | Estimativa nossa | Modelo PLG com conteúdo, comunidades e indicação; bônus de parceria com agências | Média | Custo real por canal |
| P16 | Tecnologia fixa: R$ 1,2 mil, 2,5 mil e 4 mil por mês. Administrativo: R$ 600, 1 mil e 1,6 mil | Estimativa nossa | Cloud base, ferramentas, contador, jurídico e LGPD. O LLM está no COGS | Média | Cotações |
| P17 | Impostos sobre receita: 6%, 8% e 10% | Estimativa nossa | Simples Nacional. O fator R, sem folha no ano 1, pode elevar a alíquota (ver C.3) | Baixa | Contador |
| P18 | Investimento inicial: R$ 18 mil (tecnologia R$ 8 mil, marketing R$ 5 mil, abertura e LGPD R$ 5 mil) | Estimativa nossa | O MVP é construído pelos sócios, sem custo de desenvolvimento | Média | Orçamentos |

**D. Capital**

| ID | Premissa e valor | Origem | Justificativa | Confiança | Como validar |
|---|---|---|---|---|---|
| P19 | Capital próprio de R$ 90 mil em três parcelas (R$ 35 mil, R$ 30 mil e R$ 25 mil). A parcela 3 depende de MRR de pelo menos R$ 3 mil no mês 12 | Decisão do grupo (valor sugerido por nós) | Dimensionado pelo caixa mínimo de cada cenário, com folga | Média | Aceite dos sócios |
| P20 | Seed de R$ 150 mil por volta do mês 9, só no cenário alternativo | Estimativa nossa | Rodadas pré-seed e seed brasileiras costumam ser dessa ordem de grandeza (não pesquisado em fonte) | Baixa | Conversas com investidores |

**E. Método e indicadores**

| ID | Premissa e valor | Origem | Justificativa | Confiança | Como validar |
|---|---|---|---|---|---|
| P21 | Horizonte de 36 meses, sem valor residual, depreciação, juros ou imposto de renda. O EBITDA aproxima o caixa operacional (sem capital de giro) | Simplificação do modelo FIAP | A planilha trabalha assim | Média | — |
| P22 | O modelo mensal é a referência de cálculo; a planilha FIAP é lida em paralelo (seção 7.2) | Decisão metodológica | A planilha anual não mostra o caixa mínimo e subestima a receita nos anos 2 e 3 | Média | Decisão com a professora |
| P23 | Adiantamento do plano anual: cobrança distribuída ao longo do ano e 70% de renovação; **fora dos números** | Estimativa nossa | Folga conservadora; é obrigação de entrega, não lucro | Baixa | Dados de cobrança |
| P24 | ROI = caixa acumulado em 36 meses ÷ capital máximo investido. Payback do capital = mês em que o caixa acumulado volta a zero. CAC payback = CAC ÷ (ticket × margem bruta) | Definição nossa, alinhada ao material da disciplina | O PDF define o ROI como (ganho − investimento) ÷ investimento | Média | — |
| P25 | TAM e SAM: 5 a 8% do mercado global para research software e dados sintéticos; América Latina com 2 a 3% | Dado, do estudo de mercado | Fontes citadas lá (ESOMAR e outras) | Média | Recorte brasileiro pendente |
| P26 | Disposição a pagar: pesquisa de 20 respondentes | Dado | n pequeno; sem garantia de representatividade | Baixa | Ampliar a amostra |
| P27 | Cenários: pessimista (metade dos novos clientes e das contas de topo, churn de 10%, 8% e 7%, custos cortados), otimista (50% mais novos clientes e contas, churn de 6%, 4,5% e 4%) | Estimativa nossa | Faixa de ±50% em volume, ordem de grandeza de uma startup em estágio inicial | Baixa | — |

### C.3 O que acontece se as premissas frágeis estiverem erradas

Modelo mensal, uma alteração por vez (ou combinada, quando indicado). O aporte necessário é o caixa mínimo; os R$ 90 mil só são suficientes se esse valor ficar abaixo deles.

| Premissa alterada | Ticket Linha 1, ano 1 | Receita ano 3 | EBITDA ano 3 | Aporte necessário | Payback |
|---|---|---|---|---|---|
| **Base** (mix 35/65, extras 10%) | R$ 202 | R$ 796 mil | +R$ 186 mil | R$ 56 mil | Mês 29 |
| P03: mix 50/50 em todos os anos | R$ 174 | R$ 647 mil | +R$ 94 mil | R$ 67 mil | Mês 34 |
| P03: mix 65% Starter / 35% Pro | R$ 147 | R$ 555 mil | +R$ 37 mil | **R$ 90 mil** | Não ocorre em 36 meses |
| P05: sem pacotes extras (L1 e topo) | R$ 183 | R$ 661 mil | +R$ 102 mil | R$ 65 mil | Mês 33 |
| P03 + P05: mix 50/50 e sem pacotes extras | R$ 159 | R$ 534 mil | +R$ 24 mil | **R$ 92 mil** | Não ocorre em 36 meses |
| P10: lançamento no mês 10 | R$ 202 | R$ 784 mil | +R$ 179 mil | R$ 72 mil | Mês 31 |
| P10: lançamento no mês 13 | R$ 202 | R$ 768 mil | +R$ 169 mil | R$ 88 mil | Mês 32 |
| Estresse: mix 50/50 e lançamento no mês 10 | R$ 174 | R$ 637 mil | +R$ 88 mil | R$ 83 mil | Mês 36 |
| P12: COGS de 45%, 40% e 35% | R$ 202 | R$ 796 mil | +R$ 131 mil | R$ 64 mil | Mês 32 |
| P17: imposto de 15,5% no ano 1 (fator R) | R$ 202 | R$ 796 mil | +R$ 186 mil | R$ 60 mil | Mês 29 |
| P02/P04: sem plano anual (churn de 9%, 7% e 6%) | R$ 202 | R$ 795 mil | +R$ 186 mil | R$ 54 mil | Mês 28 |

Leitura:

1. **O mix é a premissa mais frágil.** Se ele for 50/50, o resultado cai cerca de 19% na receita do ano 3 e pela metade no EBITDA, mas o aporte de R$ 90 mil ainda cobre com folga. Com 65% no Starter, o aporte é consumido por inteiro e o capital não se recupera em 36 meses.
2. **Combinar premissas ruins esgota o aporte.** Mix de 50/50 sem pacotes extras exige R$ 92 mil, acima dos R$ 90 mil.
3. **Atrasar o lançamento custa caro no caixa e pouco no resultado:** um atraso de 6 meses (mês 13) leva o aporte necessário a R$ 88 mil.
4. **No modelo, o plano anual é praticamente neutro na receita**, porque o desconto e o menor churn se compensam. O ganho do anual está no caixa antecipado e na fidelização, que não entram nos números (P23).
5. **Funil não modelado (P08):** os novos clientes por mês são uma meta, não o resultado de um funil. Com conversão de 5%, exigem de 120 a 560 cadastros por mês, e isso não foi validado.

**Ponto em aberto:** o cenário base mantém o mix 35/65. Diante da evidência de que ele é otimista, o grupo precisa decidir se adota um mix mais prudente (por exemplo, 50/50) como base.
