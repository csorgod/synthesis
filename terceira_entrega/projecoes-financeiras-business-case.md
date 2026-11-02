# Entrega 3: Projeções Financeiras e Business Case

> Planilha de apoio: [Planilha preenchida](FIAP_Modelo_Projecao_Financeira_MVP_Synthesis.xlsx) (cópia da planilha com as células de entrada preenchidas; fórmulas e abas originais intactas).
> Insumos: [Estudo de mercado](../docs/estudo-de-mercado.md), [Proposta de valor](../segunda_entrega/proposta-valor.md), [Canvas](../segunda_entrega/CANVAS.pdf) e a pesquisa de validação (20 respondentes, ago/2026).

---

## 1. Resumo executivo

O Synthesis é um SaaS self-service de simulação de reação de audiência com personas sintéticas calibradas para o Brasil. A lógica econômica proposta é:

- **Monetização:** assinatura mensal, por empresa ou profissional, que dá um saldo de **créditos** (moeda interna, nome a definir), usados livremente em estudos simples ou complexos. Quem estoura o saldo pode **opcionalmente** comprar créditos extras. Há também **plano anual** (com vantagens), pago antecipadamente.
- **Planos (preço inicial, a validar):** Starter R$ 89, Pro R$ 279 e uma faixa Business **a partir de R$ 449, sob orçamento**. O plano anual tem preço fixo de R$ 790, R$ 2.490 e a partir de R$ 3.990 por ano, cerca de 26% abaixo de 12 mensalidades.
- **Capital:** cenário principal com **capital próprio de R$ 90 mil**, liberado em três parcelas, **sem pró-labore para os sócios no ano 1** (os sócios mantêm renda própria). Seed como cenário alternativo.
- **Resultado (cenário base, modelo mensal de 36 meses):** receita de R$ 28 mil, R$ 319 mil e R$ 865 mil nos anos 1, 2 e 3; EBITDA mensal sustentadamente positivo a partir do mês 17; caixa mínimo de R$ 50 mil (mês 16), coberto pelo aporte com folga de R$ 40 mil; capital recuperado no mês 26.
- **Pontos de atenção:**
  1. O crescimento de novos clientes é a variável que mais pesa: com metade dos novos clientes, o EBITDA do ano 3 fica negativo.
  2. A planilha compartilhada traz uma inconsistência de fórmula que **subestima a receita dos anos 2 e 3** (seção 7.2). Lida AS IS, ela mostra o ano 3 com EBITDA positivo, porém baixo (+R$ 52 mil); com a fórmula corrigida, o mesmo cenário dá +R$ 193 mil.
  3. As premissas de preço, mix, créditos extras, custo por crédito e CAC **não foram validadas com clientes reais**. A pesquisa dá indício de disposição a pagar, não prova de conversão. Todas as premissas estão registradas no Anexo C, com o efeito de errá-las.

---

## 2. Modelo de monetização

### 2.1 Como o Synthesis cobra

| Elemento | Regra |
|---|---|
| **Unidade de cobrança** | Uma assinatura por empresa ou profissional (não por usuário). Usuários incluídos: Starter 1, Pro até 3 e Business até 10 (seção 2.4); o limitador real é o saldo de créditos. |
| **Créditos** | Moeda interna do Synthesis. Cada estudo consome créditos proporcionais ao seu custo (um teste rápido de título gasta pouco; um painel grande de personas gasta mais). O cliente escolhe: vários estudos simples ou poucos complexos. |
| **Saldo mensal** | Incluído na mensalidade. **Expira** no fim do ciclo. |
| **Créditos extras** | Opcionais, comprados à parte. **Acumulam** (não expiram enquanto a assinatura estiver ativa; no plano anual, durante todo o contrato). Isso reduz o receio de "gastar demais" e incentiva o uso. |
| **Estouro do saldo** | Teto rígido com opt-in: sem créditos extras ativos, as simulações pausam. Alertas aos 80% e 100% do saldo. O cliente nunca recebe cobrança surpresa. |
| **Teste gratuito** | **200 créditos** de boas-vindas **únicos** (não renovam todo mês), sem cobrança e sem cadastro de cartão. Esse bônus tem custo relevante (ver P34 no Anexo C). |

Por que créditos e não "entrevistas" ou "simulações": o saldo flexível acompanha o custo real de LLM de cada estudo e permite trocar de modelo de IA sem mudar o preço ao cliente. Os créditos expirados também geram receita sem custo associado ("breakage"), o que ajuda a margem.

### 2.2 Planos

| Plano | Mensal | Anual | Equivalente por mês no anual | Economia no anual* | Público |
|---|---|---|---|---|---|
| **Free** | R$ 0 | n.a. | n.a. | n.a. | 200 créditos de boas-vindas únicos, para experimentar |
| **Starter** | R$ 89 | R$ 790 | R$ 65,83 | R$ 278 (26%) | Criadores de conteúdo e freelancers |
| **Pro** | R$ 279 | R$ 2.490 | R$ 207,50 | R$ 858 (26%) | Freelancers sênior, analistas de marketing, PMEs |
| **Business (sob orçamento)** | **A partir de R$ 449** | A partir de R$ 3.990 | A partir de R$ 332,50 | A partir de R$ 1.398 (26%) | Agências, times de marketing e quem usaria mais que o Pro |

\* Em relação a 12 mensalidades do plano mensal.

- O **plano anual** é pago antecipadamente, usando ou não. O preço anual é fixo e cerca de 26% menor que 12 mensalidades; o preço mensal foi definido para que o anual pareça claramente mais atrativo (registro da decisão no Anexo D). Esse desconto é uma premissa nossa, a validar. Os créditos mensais do plano seguem expirando no ciclo; os créditos extras valem durante todo o contrato.
- A **faixa Business** cobre quem pagaria R$ 300 ou mais (45% da pesquisa). Para o usuário, o convite é "faça um orçamento", **a partir de R$ 449**. As subfaixas internas ficam para uma discussão futura; no modelo financeiro, o piso de R$ 449 é usado como base, uma premissa conservadora (o ticket real será igual ou maior).
- Os nomes Starter e Pro vêm do Canvas.
- **Sobre a faixa sob orçamento:** o diferencial do Synthesis é o self-service, e o estudo de mercado critica a Galaxies justamente por exigir demo e implementação assistida. Para não reintroduzir esse atrito, o preço "a partir de" deve ser público, e o orçamento fica para quem precisa de volume ou condições especiais.
- **Sobre o preço do Pro.** Na pesquisa (n = 20), a disposição a pagar por mês é bimodal: R$ 0 (25%), até R$ 100 (25%), R$ 100 a 300 (5%), R$ 300 a 500 (25%) e acima de R$ 500 (20%). Os R$ 279 ficam perto do grupo de R$ 300 ou mais, mas ainda na faixa onde só 5% se posicionaram. Vale testar o preço nos primeiros meses.

### 2.3 Orçamento de inferência por plano

O custo variável principal é o LLM. Para o plano não dar prejuízo ao cliente que usa 100% do saldo, adotamos como regra: **custo de inferência no saldo cheio ≤ 40% da mensalidade**.

| Plano | Mensalidade | Orçamento de inferência (40%) | Equivalente em entrevistas curtas* |
|---|---|---|---|
| Starter | R$ 89 | R$ 36 | 22 a 130 |
| Pro | R$ 279 | R$ 112 | 68 a 407 |
| Business (a partir de) | R$ 449 | R$ 180 | 109 a 653 |

\* Custo de uma entrevista curta de US$ 0,05 a US$ 0,30 (estudo de mercado, seção 3.1), convertido a R$ 5,50 por dólar (premissa de câmbio a atualizar). A faixa é larga porque o custo por unidade depende do modelo, do cache de prompt e do tamanho do estudo. **O número de créditos de cada plano só pode ser fechado depois de medir o custo real por simulação no MVP.**

### 2.4 Usuários por assinatura

Uma assinatura é um **espaço de trabalho compartilhado**: o cliente (empresa ou profissional) paga uma mensalidade e convida as pessoas que vão usar o saldo de créditos. Não existe cobrança por login.

| Plano | Usuários incluídos |
|---|---|
| Starter | 1 |
| Pro | até 3 |
| Business (a partir de R$ 449) | até 10; acima disso, sob orçamento |

O custo do Synthesis vem do consumo de créditos, então mais usuários não aumentam o custo por si só. O limite existe para **diferenciar os planos** e evitar que uma agência use um Starter para atender a equipe toda. Os valores são estimativa nossa (P28, Anexo C).

### 2.5 Créditos por plano

**Unidade.** O crédito é a unidade de cobrança base da plataforma. Um estudo consome um ou mais créditos, conforme a complexidade da análise, na proporção do custo de LLM. Como referência de cálculo, 1 crédito equivale a uma resposta de uma persona sintética a um estímulo (uma pergunta, um conceito de campanha, um título ou uma thumbnail). Por ora, a moeda se chama apenas "créditos".

**Custo por crédito.** O estudo de mercado estima US$ 0,05 a 0,30 por entrevista curta de 5 perguntas, ou seja, US$ 0,01 a 0,06 por resposta (R$ 0,06 a R$ 0,33, a R$ 5,50 por dólar). Adotamos o ponto médio da faixa, **R$ 0,14 por crédito**. Como referência de cálculo, uma resposta com 1.500 tokens de entrada e 400 de saída, a US$ 3 e US$ 15 por milhão de tokens (preço do modelo usado no estudo), custa US$ 0,0105, ou R$ 0,06, sem otimização. A diferença para R$ 0,14 cobre contextos mais longos, imagens e novas tentativas. Os preços de LLM precisam ser atualizados para o modelo que for de fato usado.

**Cota proposta e viabilidade:**

| Plano | Mensalidade | Cota mensal | Preço por crédito | Custo no saldo cheio (R$ 0,14) | % do preço | Tokens por mês (aprox.) |
|---|---|---|---|---|---|---|
| Starter | R$ 89 | 200 créditos | R$ 0,45 | R$ 28 | 31% | 0,4 milhão |
| Pro | R$ 279 | 750 créditos | R$ 0,37 | R$ 105 | 38% | 1,4 milhão |
| Business (a partir de) | R$ 449 | 1.300 créditos | R$ 0,35 | R$ 182 | 41% | 2,5 milhões |

O preço por crédito cai nos planos maiores (de R$ 0,45 no Starter para R$ 0,37 no Pro e R$ 0,35 no Business, no plano mensal), porque quem contrata um plano mais caro espera pagar menos por crédito. No plano anual, o preço por crédito é de R$ 0,33, R$ 0,28 e R$ 0,26.

O custo da tabela é o do pior caso de uso, com o saldo inteiro consumido. No plano mensal, o Starter (31%) e o Pro (38%) ficam dentro da regra de 40% da seção 2.3; o **Business (41%) fica um pouco acima**. No plano anual, que cobra menos por mês, o saldo cheio custaria 43%, 51% e 55% do valor mensal equivalente, acima da regra nos três planos. Aceitamos isso porque o uso médio é menor: com 70% de uso do saldo, o custo seria de 22%, 26% e 28% do preço no mensal e de 30%, 35% e 38% no anual. Também cai com cache de prompt e modelos menores na triagem. Se o uso médio ficar acima do esperado, é preciso rever as cotas dos planos maiores.

**Risco.** Se o custo real por crédito ficar no teto da faixa do estudo (R$ 0,33), o saldo cheio custaria 74% do preço mensal no Starter, 89% no Pro e 96% no Business, e de 100% a 129% no plano anual, ou seja, prejuízo para quem usa tudo no anual do Pro e do Business. Se ficar no piso (R$ 0,06), o custo cai para 13% a 17% no mensal. Por isso a cota é uma proposta e só fecha depois de medir o custo real no MVP.

**O que o cliente contrata, em estudos (valores aproximados; o consumo real depende da complexidade):**

| Estudo | Créditos (aprox.) | Starter (200) | Pro (750) | Business (1.300) |
|---|---|---|---|---|
| Teste rápido: 1 conceito com 10 personas | 10 | cerca de 20 | cerca de 75 | cerca de 130 |
| Comparativo entre versões: 2 variantes com 20 personas cada | 40 | cerca de 5 | cerca de 18 | cerca de 30 |
| Aprofundado: 30 personas com 5 perguntas | 150 | cerca de 1 | cerca de 5 | cerca de 8 |

**Créditos extras: pacotes propostos.** Vendidos em três pacotes avulsos, com o mesmo preço no plano mensal e no anual (só a validade muda, conforme a seção 2.6):

| Pacote | Preço | Preço por crédito | Margem sobre o custo de R$ 0,14 | Margem se o custo for R$ 0,33 | Equivale a |
|---|---|---|---|---|---|
| 100 créditos | R$ 59 | R$ 0,59 | 76% | 44% | 10 testes rápidos |
| 300 créditos | R$ 159 | R$ 0,53 | 74% | 38% | 30 testes rápidos ou cerca de 7 comparativos entre versões |
| 1.000 créditos | R$ 499 | R$ 0,50 | 72% | 34% | Mais que um mês cheio do Pro (750 créditos) |

A média simples dos três pacotes é de R$ 0,54 por crédito, perto dos R$ 0,55 usados como referência até aqui (P33). **Regras que levaram a esses valores:**

1. **O crédito extra custa mais que o crédito de qualquer plano.** No mensal o crédito do plano custa R$ 0,45, R$ 0,37 e R$ 0,35; no anual, R$ 0,33, R$ 0,28 e R$ 0,26. O pacote mais barato por crédito (R$ 0,50) fica acima de todos, então o plano continua sendo o caminho mais barato e o extra é para o pico de uso.
2. **O extra deve levar a subir de plano.** Do Starter para o Pro a diferença é de R$ 190 por mês, e o Pro dá 550 créditos a mais. Um pacote de 300 créditos (R$ 159) fica abaixo desses R$ 190; dois pacotes já passam. Quem precisa de dois pacotes por mês paga mais que o Pro.
3. **Margem positiva mesmo no pior caso de custo.** Com o custo adotado (R$ 0,14 por crédito), a margem fica entre 72% e 76%. Se o custo real chegar ao teto da faixa de mercado (R$ 0,33), cai para 34% a 44%, ainda positiva.
4. **Desconto de volume pequeno.** Do pacote de 100 ao de 1.000 o desconto é de cerca de 15%. Um desconto maior faria o cliente esperar para comprar o pacote grande e esvaziaria o plano.
5. **Tamanhos ligados ao uso e entrada abaixo da mensalidade.** Cada pacote cobre uma situação concreta (algumas semanas de testes rápidos, um mês de pico, uma campanha grande). O pacote de entrada (R$ 59) é menor que a mensalidade do Starter (R$ 89), para que a compra avulsa não pareça uma troca de plano.

**O que ainda falta validar.** O preço não foi testado com clientes e depende do custo de R$ 0,14 por crédito, que só se mede no MVP. No plano anual o crédito extra (R$ 0,50 a R$ 0,59) custa de 1,5 a 2,3 vezes o crédito do plano (R$ 0,26 a R$ 0,33), uma diferença que pode soar como punição a quem pagou adiantado; vale testar um preço menor para o anual. No modelo financeiro, o gasto com extras entra como percentual da mensalidade (P05, 10% a 40%); o preço do pacote muda quantos créditos esse gasto compra e a margem de cada crédito vendido, não a receita projetada.

### 2.6 Cancelamento e reembolso

- **Se o cliente cancelar:** os créditos do plano e os créditos extras valem até o fim do período contratado. Depois, são perdidos.
- **Plano anual:** é pago adiantado e não há reembolso. Quem cancela, mesmo no primeiro mês, continua usando até o fim do plano contratado, e a assinatura não renova. É uma prática comum em SaaS anual, e o desconto de cerca de 26% e o teste gratuito servem para o cliente experimentar antes de se comprometer.
- **Ressalva a validar com o jurídico:** o Código de Defesa do Consumidor prevê prazo de arrependimento de 7 dias para contratações feitas fora do estabelecimento, o que inclui compras online. Se o cliente for consumidor, pode ser necessário reembolso integral nesse prazo.

---

## 3. Fontes de receita

| Linha na planilha | O que é | Planos | Mapeamento |
|---|---|---|---|
| **Linha 1** | Assinaturas self-service + créditos extras | Starter e Pro | Ticket médio por assinatura, novos clientes por mês e churn |
| **Linha 2** | Assinatura da faixa Business + créditos extras | A partir de R$ 449 | Ticket médio por assinatura e média de assinaturas pagantes no ano |
| *Fora da projeção* | Subfaixas internas do Business, API, integrações | Sob orçamento | Potencial de expansão; não entra nos números |

A planilha permite duas linhas de receita recorrente, então os créditos extras foram embutidos no ticket médio de cada linha em vez de virarem uma terceira linha.

### 3.1 Como o ticket médio foi construído

O ticket é **por assinatura**. Ele combina a mensalidade média (mix de planos, ponderando quem assina o mensal e quem assina o anual) e a receita de créditos extras. Quem assina o mensal paga a mensalidade; quem assina o anual paga o preço anual dividido por 12.

**Linha 1 (Starter e Pro)**

| | Ano 1 | Ano 2 | Ano 3 |
|---|---|---|---|
| Mix de assinaturas Starter / Pro | 35% / 65% | 30% / 70% | 25% / 75% |
| Mensalidade média no plano mensal (R$ 89 e R$ 279) | R$ 212,50 | R$ 222,00 | R$ 231,50 |
| Assinaturas anuais | 20% | 30% | 35% |
| Mensalidade equivalente no plano anual (R$ 790 e R$ 2.490 por ano) | R$ 157,92 | R$ 165,00 | R$ 172,08 |
| Mensalidade média ponderada | R$ 201,58 | R$ 204,90 | R$ 210,70 |
| Créditos extras (% da mensalidade) | 10% | 14% | 19% |
| **Ticket médio por assinatura** | **R$ 222** | **R$ 234** | **R$ 251** |

**Linha 2 (faixa Business)**

| | Ano 1 | Ano 2 | Ano 3 |
|---|---|---|---|
| Mensalidade-base no plano mensal (piso da faixa) | R$ 449 | R$ 449 | R$ 449 |
| Mensalidade equivalente no plano anual (a partir de R$ 3.990 por ano) | R$ 332,50 | R$ 332,50 | R$ 332,50 |
| Mensalidade média ponderada | R$ 425,70 | R$ 414,05 | R$ 408,23 |
| Créditos extras (assinaturas maiores usam mais) | 20% | 30% | 40% |
| **Ticket médio por assinatura** | **R$ 511** | **R$ 538** | **R$ 572** |

O mix migra para o Pro e os créditos extras ganham peso porque o hábito de uso cresce e os clientes descobrem que precisam de mais saldo. **Mix, percentual de extras e adesão ao plano anual são premissas nossas, sem evidência direta.** O mix de 65% no Pro é provavelmente otimista (a pesquisa indica muitos respondentes na faixa até R$ 100); no Anexo C.3, um mix de 50/50 reduz o ticket do ano 1 para R$ 192.

### 3.2 O efeito do plano anual

- **No ticket:** o preço anual, cerca de 26% menor, reduz a receita mensal reconhecida (já incluído acima). Com o preço mensal atual, o anual passa a custar receita: sem ele, a receita do ano 3 seria cerca de 3% maior (Anexo C.3).
- **No churn:** quem assina o anual só cancela na renovação. Adotamos churn mensal de 9%, 7% e 6% para o plano mensal e o equivalente a 3% ao mês (cerca de 30% de não renovação ao ano) para o anual. O churn combinado fica em 7,8%, 5,8% e 5,0%, que arredondamos para **8%, 6% e 5%**.
- **No caixa:** o anual é recebido antes de a receita ser reconhecida. A planilha calcula caixa a partir do EBITDA e **não captura esse adiantamento**. Como ordem de grandeza (cobrança distribuída ao longo do ano e 70% de renovação), o adiantamento líquido seria de cerca de R$ 55 mil no ano 2 e R$ 100 mil no ano 3. Não entra nos números abaixo, então é uma folga conservadora. É também uma obrigação de entregar o serviço, não lucro; a política de cancelamento e reembolso do anual (inclusive o prazo legal de arrependimento em compras online) precisa ser validada com jurídico.

---

## 4. Tamanho de mercado (TAM, SAM, SOM)

### 4.1 Top-down

Fonte: [estudo de mercado](../docs/estudo-de-mercado.md), seção 1 (ESOMAR e outros). Câmbio de R$ 5,50 por dólar.

| Camada | Definição | Valor |
|---|---|---|
| **TAM** | Mercado global de pesquisa e insights (2023) | US$ 142 bi |
| **SAM global** | Research software + dados sintéticos (5 a 8% do TAM) | US$ 7 a 11 bi |
| **SAM regional** | América Latina (2 a 3% do mercado global de pesquisa) | US$ 140 a 330 mi (R$ 0,8 a 1,8 bi) |
| **SOM do plano** | MRR de R$ 91,2 mil no fim do ano 3, ou ARR de cerca de R$ 1,1 mi (US$ 199 mil) | 0,06% a 0,14% do SAM regional |

### 4.2 Bottom-up

Parte do nosso modelo: no fim do ano 3, cerca de **341 assinaturas** nos planos Starter e Pro e **10 assinaturas** na faixa Business, com ticket médio de R$ 251 e R$ 572 por mês. É o SOM do plano: aproximadamente R$ 1,1 mi de ARR.

### 4.3 Leitura

- O SOM do plano é **conservador**: o estudo de mercado estimava US$ 0,5 a 2 mi de ARR em 24 meses (aproximadamente R$ 2,8 a 11 mi), de 3 a 10 vezes acima do que o plano projeta para o fim do ano 3. A diferença vem de partirmos de um MVP sem receita nos 6 primeiros meses, preços de entrada baixos e crescimento essencialmente orgânico.
- **Lacuna:** o top-down usa o mercado global/regional. Falta o recorte do universo brasileiro (número de agências, PMEs com marketing digital e criadores monetizados) a partir de fontes como IBGE, Sebrae e relatórios do setor. Esse levantamento está nos próximos passos; **não foram inventados números** para preencher o campo.

---

## 5. Premissas financeiras

Valores inseridos na planilha (aba Premissas). Os custos são mensais. **O registro completo das premissas, com origem, justificativa, impacto e forma de validação, está no [Anexo C](#anexo-c-registro-de-premissas).**

| Premissa | Ano 1 | Ano 2 | Ano 3 | Base da premissa | Confiança |
|---|---|---|---|---|---|
| Ticket médio Linha 1 | R$ 222 | R$ 234 | R$ 251 | Seção 3.1 | Baixa |
| Novos clientes/mês, Linha 1 | 3 | 16 | 28 | Ano 1: 6 por mês a partir do mês 7 (MVP nos 6 primeiros meses), média de 12 meses de 3 | Baixa |
| Churn mensal combinado | 8% | 6% | 5% | Seção 3.2; público de renda variável | Baixa |
| Ticket médio Linha 2 | R$ 511 | R$ 538 | R$ 572 | Seção 3.1 (piso de R$ 449) | Baixa |
| Assinaturas na faixa Business (média no ano) | 0,5 | 4 | 10 | Ano 1: 1 assinatura a partir do mês 7; parceria com agências é canal de aquisição | Baixa |
| COGS (% da receita) | 38% | 33% | 28% | Orçamento de inferência (2.3) e gateway, cloud e custo do trial; cai com cache de prompt, lote e modelos menores | Média-baixa |
| Pessoal | R$ 0 | R$ 7.000 | R$ 14.000 | Sem pró-labore no ano 1; a partir do ano 2, pró-labore escalonado e apoio part-time | Média |
| Marketing e aquisição | R$ 1.000 | R$ 2.500 | R$ 4.500 | Conteúdo, LinkedIn e comunidades (PLG, pouca mídia paga) | Média |
| Vendas e comissões | R$ 0 | R$ 500 | R$ 1.500 | Bônus de parceria com agências | Média |
| Tecnologia (fixa) | R$ 1.200 | R$ 2.500 | R$ 4.000 | Cloud base, observabilidade, ferramentas; o LLM está no COGS | Média |
| Administrativo | R$ 600 | R$ 1.000 | R$ 1.600 | Contador, jurídico e LGPD | Média |
| Impostos s/ receita | 6% | 8% | 10% | Simples Nacional (a confirmar com contador) | Baixa |
| Investimento inicial | R$ 18.000 | n.a. | n.a. | Tecnologia R$ 8 mil, marketing de lançamento R$ 5 mil, abertura da empresa e termos LGPD R$ 5 mil | Média |
| Capital próprio | R$ 90.000 | n.a. | n.a. | Seção 9 | Definição dos sócios |

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

### 7.1 Planilha (leitura direta)

Resultado da aba **Projeção 3 Anos** com as premissas da seção 5, em R$:

| | Ano 1 | Ano 2 | Ano 3 |
|---|---|---|---|
| Receita Linha 1 | 31.585 | 212.060 | 510.555 |
| Receita Linha 2 | 3.066 | 25.824 | 68.640 |
| **Receita total** | **34.651** | **237.884** | **579.195** |
| COGS | (13.167) | (78.502) | (162.175) |
| **Lucro bruto** | **21.484** | **159.382** | **417.021** |
| Margem bruta | 62% | 67% | 72% |
| Pessoal | 0 | (84.000) | (168.000) |
| Marketing | (12.000) | (30.000) | (54.000) |
| Vendas | 0 | (6.000) | (18.000) |
| Tecnologia | (14.400) | (30.000) | (48.000) |
| Administrativo | (7.200) | (12.000) | (19.200) |
| Impostos | (2.079) | (19.031) | (57.920) |
| **EBITDA** | **(14.195)** | **(21.648)** | **51.901** |
| Margem EBITDA | −41% | −9% | 9% |
| Caixa final (início: R$ 90.000; investimento: R$ 18.000) | 57.805 | 36.156 | 88.057 |

### 7.2 Atenção: a fórmula de receita da Linha 1 subestima os anos 2 e 3

Na aba Premissas, a dica da célula F12 diz que a receita usa "a média entre clientes ativos no início e no fim do ano". Mas as fórmulas de D12 e E12 usam `ticket × clientes_finais / 2 × 12`, ou seja, tratam o início do ano como zero. No ano 1 isso está correto (a base começa em zero). Nos anos 2 e 3, a receita fica subestimada em **12% e 28%**.

**Não alteramos essa fórmula**, pois não é uma célula de entrada. A correção seria `=D8*(C11+D11)/2*12` em D12 e `=E8*(D11+E11)/2*12` em E12. Com ela, as mesmas premissas dão:

| | Planilha como está | Planilha com média corrigida | Modelo mensal (36 meses) |
|---|---|---|---|
| Receita ano 1 / 2 / 3 (R$ mil) | 35 / 238 / 579 | 35 / 271 / 807 | 28 / 319 / 865 |
| EBITDA ano 1 / 2 / 3 (R$ mil) | −14 / −22 / +52 | −14 / −2 / +193 | −18 / +26 / +229 |
| Caixa final ano 1 / 2 / 3 (R$ mil)* | 58 / 36 / 88 | 58 / 56 / 249 | −36 / −10 / +219 |

\* Planilhas partem de R$ 90 mil de capital; o modelo mensal parte de zero (mostra o caixa acumulado antes do aporte).

O **modelo mensal** é a nossa referência de cálculo: parte do lançamento no mês 7, aplica churn mês a mês e permite achar o **caixa mínimo** (o ponto mais fundo do vale da morte), que a planilha anual não mostra. É a base para dimensionar o aporte. Os valores diferem da planilha corrigida porque a planilha distribui os novos clientes de forma uniforme ao longo do ano e o modelo mensal reflete o MVP sem receita nos meses 1 a 6.

**Como ler:** a planilha oficial, lida como está, mostra um ano 3 com lucro baixo por causa da fórmula. Para o business case, a referência é o modelo mensal; a planilha corrigida confirma a ordem de grandeza.

### 7.3 Modelo mensal: cenário base

| | Ano 1 | Ano 2 | Ano 3 |
|---|---|---|---|
| Receita (R$) | 27.593 | 319.006 | 864.972 |
| EBITDA (R$) | (18.148) | 26.214 | 229.083 |
| MRR no fim do ano (R$) | 7.065 | 38.142 | 91.188 |
| Assinaturas Starter/Pro no fim do ano | 30 | 154 | 341 |

- O EBITDA mensal passa a ser **sustentadamente positivo a partir do mês 17**.
- O **caixa mínimo** é de R$ 50 mil, no **mês 16**. Os R$ 90 mil de capital cobrem esse ponto com folga de R$ 40 mil.
- O **payback do capital** (mês em que o caixa acumulado volta a zero) é o **mês 26**.

---

## 8. Indicadores de viabilidade

### 8.1 Indicadores da planilha (aba Dashboard)

| Indicador | Ano 1 | Ano 2 | Ano 3 |
|---|---|---|---|
| MRR médio do ano (receita ÷ 12) | R$ 2.888 | R$ 19.824 | R$ 48.266 |
| ARR (receita anual) | R$ 34.651 | R$ 237.884 | R$ 579.195 |
| Assinaturas Starter/Pro ativas no fim do ano | 24 | 151 | 339 |
| Churn mensal | 8% | 6% | 5% |
| CAC (marketing + vendas ÷ novos clientes) | R$ 333 | R$ 188 | R$ 214 |
| LTV (ticket × margem bruta ÷ churn) | R$ 1.720 | R$ 2.613 | R$ 3.614 |
| LTV/CAC | 5,2 | 13,9 | 16,9 |
| Payback do CAC (meses) | 2,4 | 1,2 | 1,2 |
| Margem bruta | 62% | 67% | 72% |
| EBITDA | −R$ 14.195 | −R$ 21.648 | +R$ 51.901 |
| Runway (meses de caixa) | 48,9 | 20,0 | Caixa gerador |
| Crescimento da receita YoY | n.a. | 587% | 143% |

O "MRR" do dashboard é a receita média mensal do ano. O MRR de fim de ano (seção 7.3) é maior.

### 8.2 CAC honesto

O CAC da planilha considera só marketing e vendas. Como o modelo é PLG (conteúdo, indicação, parcerias), o CAC "de mídia" é baixo. Mas a partir do ano 2 há time dedicado e não é justo ignorar esse custo:

| | Ano 1 | Ano 2 | Ano 3 |
|---|---|---|---|
| CAC de mídia | R$ 333 | R$ 188 | R$ 214 |
| CAC completo (inclui pessoal) | R$ 333 | R$ 625 | R$ 714 |
| LTV/CAC completo | 5,2 | 4,2 | 5,1 |
| Payback do CAC completo (meses) | 2,4 | 4,0 | 4,0 |

A leitura prudente é **LTV/CAC em torno de 4 a 5**, acima da regra de ouro de 3×. O CAC de mídia, muito abaixo disso, depende de a aquisição orgânica funcionar de verdade, o que ainda não foi testado. O CAC do ano 1 é igual nas duas versões porque não há pessoal remunerado (o custo de oportunidade dos sócios não entra).

### 8.3 Ponto de equilíbrio

Receita mensal necessária para cobrir os custos fixos do ano, com margem de contribuição de 56%, 59% e 62%:

| | Ano 1 | Ano 2 | Ano 3 |
|---|---|---|---|
| Custos fixos mensais | R$ 2.800 | R$ 13.500 | R$ 25.600 |
| MRR de equilíbrio | R$ 5.000 | R$ 22.900 | R$ 41.300 |
| Equivalente em assinaturas Starter/Pro | 23 | 98 | 165 |

### 8.4 Retorno

- **Payback do capital:** mês 26 (cenário base).
- **ROI em 36 meses:** o caixa acumulado ao fim de 36 meses é de R$ 219 mil, sobre um capital máximo investido de R$ 50 mil, ou seja, **ROI de cerca de 436%**. Não inclui valor residual do negócio, e depende de o cenário base se realizar.
- **Margem bruta de 62% a 72%:** dentro da faixa de 60 a 80% de referência para SaaS, mas na parte baixa; é a contrapartida do custo de LLM.
- **Churn de 5 a 8% ao mês:** acima do referencial de SaaS B2B (< 3%). É coerente com o público (freelancers e criadores), mas é o segundo ponto de atenção do modelo.

---

## 9. Capital, vale da morte e aporte dos sócios

O "vale da morte" do Synthesis é o período entre o gasto do MVP e a receita cobrir os custos: do lançamento (mês 7) até cerca do mês 17. O ponto mais fundo, no cenário base, ocorre no **mês 16**.

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
| **Base** | R$ 50 mil | 16 | R$ 865 mil | +R$ 229 mil | Mês 26 |
| Otimista | R$ 36 mil | 8 | R$ 1,41 mi | +R$ 565 mil | Mês 18 |
| Pessimista, com cortes de custo | R$ 56 mil | 18 | R$ 382 mil | +R$ 66 mil | Mês 35 |
| Pessimista, sem cortes | R$ 190 mil | 36 | R$ 382 mil | −R$ 71 mil | n.a. |
| Base com ticket da Linha 1 20% menor | R$ 63 mil | 18 | R$ 706 mil | +R$ 131 mil | Mês 32 |
| Base com 1 sócio em tempo integral (variante 9.3) | R$ 92 mil | 16 | R$ 865 mil | +R$ 229 mil | Mês 29 |

- Os R$ 90 mil cobrem o **base** (folga de R$ 40 mil), o **pessimista com cortes** (folga de R$ 34 mil) e o **ticket 20% menor** (folga de R$ 27 mil).
- O caixa mínimo do base, do otimista, do pessimista com cortes e do ticket 20% menor fica abaixo de R$ 65 mil, o total das duas primeiras parcelas. A parcela 3 funciona como reserva e só é necessária no cenário do sócio em tempo integral.
- **Sem cortes, o pessimista não se sustenta só com capital próprio.** Por isso o plano exige disciplina: se o MRR ficar abaixo do esperado, congelar o pró-labore do ano 2 e reduzir marketing ao mínimo.
- Como o caixa mínimo do base é de R$ 50 mil, o aporte principal poderia ser menor. Mantivemos R$ 90 mil pela folga nos cenários adversos; reduzir é uma decisão dos sócios.

Premissas do cenário pessimista com cortes: metade dos novos clientes e das assinaturas Business, churn de 10%, 8% e 7%, e custos reduzidos (pessoal R$ 0, 3,5 mil e 7 mil por mês; marketing R$ 800, 1,5 mil e 2,5 mil). No otimista: 50% mais novos clientes e assinaturas Business, churn de 6%, 4,5% e 4%.

**Elasticidade ao preço mensal.** O preço mensal atual é uma aposta. Se ele afastar 15% dos novos clientes da Linha 1, o ano 3 ainda fecha com receita de R$ 746 mil e EBITDA de +R$ 155 mil (caixa mínimo de R$ 59 mil), então o plano tolera uma queda de conversão dessa ordem.

### 9.3 Variante: um sócio em tempo integral

Se um sócio se dedicar integralmente já no ano 1, com pró-labore de R$ 3,5 mil por mês, o custo extra é de R$ 42 mil por ano. O aporte necessário no base sobe para cerca de **R$ 92 mil**, acima dos R$ 90 mil previstos, e a recomendação passa a ser de cerca de **R$ 115 mil**.

### 9.4 Cenário alternativo: plano acelerado com seed

Plano um pouco mais acelerado, com seed de **R$ 150 mil por volta do mês 9**, mais R$ 30 mil de capital próprio inicial:

| | Ano 1 | Ano 2 | Ano 3 |
|---|---|---|---|
| Receita | R$ 28 mil | R$ 421 mil | R$ 1,17 mi |
| EBITDA | −R$ 18 mil | −R$ 17 mil | +R$ 231 mil |

- Premissas: novos clientes de 22 e 38 por mês nos anos 2 e 3; 6 e 14 assinaturas Business; pessoal de R$ 12 mil e R$ 24 mil por mês; marketing de R$ 5 mil e R$ 8 mil.
- **Esse plano acelerado, por si só, precisa de cerca de R$ 80 mil de capital:** o caixa mínimo é de R$ 50 mil sobre os R$ 30 mil iniciais. Ou seja, ele cabe no mesmo aporte do cenário principal.
- O seed, portanto, **não é necessário para financiar** o plano; ele **substituiria capital próprio**. Com seed de R$ 100 mil no mês 9, os sócios precisariam colocar cerca de R$ 40 mil antes de a rodada fechar (rodadas demoram), e o caixa mínimo seguinte ficaria perto de R$ 50 mil. Com R$ 150 mil, a folga é maior (cerca de R$ 100 mil).
- **Comparação com o cenário principal:** o plano acelerado entrega cerca de R$ 305 mil a mais de receita no ano 3 (R$ 1,17 mi contra R$ 865 mil) com EBITDA parecido (R$ 231 mil contra R$ 229 mil). O que o seed compra é menos capital próprio exigido e mais velocidade, ao custo de diluição societária.
- As entradas para reproduzir esse cenário na planilha estão no Anexo B (ela vai subestimar o ano 3 pelo problema de fórmula descrito em 7.2).

---

## 10. Sensibilidade

EBITDA do ano 3, variando uma premissa por vez (planilha com média corrigida, base de +R$ 193 mil):

| Variação | EBITDA ano 3 |
|---|---|
| Base | +R$ 193 mil |
| Ticket da Linha 1 −20% | +R$ 102 mil |
| COGS +12 p.p. (50%, 45%, 40%) | +R$ 96 mil |
| Churn +4 p.p. (12%, 10%, 8%) | +R$ 96 mil |
| Novos clientes −50% | −R$ 36 mil |

Conclusões:

1. **Preço, custo de LLM e churn, cada um sozinho, reduzem o lucro do ano 3 em cerca de metade.** O negócio funciona, mas a margem de segurança não é grande.
2. **A aquisição de clientes é a variável mais crítica.** Com metade dos novos clientes, o ano 3 fica no vermelho mesmo sem outros problemas.
3. Os três primeiros riscos (preço, COGS, churn) são mensuráveis cedo, ainda no MVP.

---

## 11. Conexão com a proposta de valor e o modelo de negócio

| Elemento da proposta de valor (Entrega 2) | Como aparece na lógica financeira |
|---|---|
| **Preço acessível, fora da faixa de pesquisa formal** (barreira de custo: 30%) | Planos de R$ 89 a "a partir de R$ 449", contra projetos de R$ 150 mil ou mais dos concorrentes enterprise (Galaxies) |
| **Velocidade, em horas** (barreira de demora: 35%) | Self-service e PLG: o cliente usa sozinho, sem consultoria, o que mantém o CAC baixo e o time pequeno |
| **Self-service, sem consultoria** | Estrutura de custos enxuta; sem custo de vendas assistidas no ano 1; preço "a partir de" público na faixa Business |
| **Criador com renda variável** (fricção da jornada do Rafael) | Starter de R$ 89 com excedente opcional e teto rígido: ele paga mais só nos meses em que usa mais, sem surpresa |
| **Loop de feedback** (previsão contra resultado real) | Principal alavanca de retenção; sustenta a redução do churn de 8% para 5% |
| **Parceria com agências** (canal do Canvas) | Linha 2 e o baixo custo de vendas; agências trazem assinaturas de maior ticket |
| **Compliance LGPD** | Custo registrado em administrativo e no investimento inicial |

O Canvas já previa assinatura mensal por perfil de uso e um modelo por créditos para criadores independentes; a proposta aqui unifica as duas ideias: todos os planos têm assinatura com saldo de créditos e créditos extras opcionais.

**Expansão possível (fora das projeções):** subfaixas internas do Business, plano com SLA e API, integrações com ferramentas brasileiras (RD Station, Hotmart) e revenda para agências.

---

## 12. Riscos e limitações

| Risco | Efeito | Mitigação |
|---|---|---|
| Premissas de preço, mix, extras e adesão ao anual não validadas | Receita pode ficar 20% ou mais abaixo | Testar preços no lançamento (inclusive o Pro de R$ 279) |
| Custo real do LLM por crédito desconhecido | Margem bruta menor que 62 a 72% | Medir no MVP; cache de prompt, processamento em lote, modelos menores na triagem; teto de inferência por plano |
| Preço mensal mais alto reduz a conversão no plano mensal | Menos novos clientes que o modelado (com 15% menos novos clientes na Linha 1: EBITDA do ano 3 de +R$ 155 mil e aporte de R$ 59 mil) | Testar o preço no lançamento; o plano anual, cerca de 26% mais barato, é a alternativa |
| Crescimento orgânico abaixo do esperado | Maior sensibilidade do modelo (seção 10) | Gatilhos de corte; reforço do canal de agências |
| Churn maior que o modelado | LTV menor | Plano anual, loop de feedback, dashboard de acurácia |
| Preço do crédito extra no anual (R$ 0,50 a R$ 0,59) é de 1,5 a 2,3 vezes o crédito do plano anual | Pode soar como punição a quem pagou adiantado e frear a compra de extras | Testar preço menor para o anual; manter o mesmo preço só se o teste não mostrar rejeição |
| Faixa sob orçamento reintroduz atrito de venda | Contradiz o diferencial self-service e pode atrasar a conversão | Preço "a partir de" público; orçamento só para volumes maiores |
| Ceticismo sobre dados sintéticos | Conversão baixa do trial | Transparência metodológica, cases com acurácia verificável |
| Concorrência (Galaxies no topo, global no entry) | Pressão de preço | Posição de self-service acessível e foco no Brasil |
| Teste gratuito de 200 créditos consome custo de LLM (R$ 28 por cadastro, a R$ 0,14 por crédito) | Margem e CAC: com 5% de conversão, cada cliente pagante carrega R$ 560 de bônus | Reduzir o bônus, exigir verificação de e-mail e limitar um bônus por pessoa (ver P34) |
| Regime tributário e fator R | Impostos acima de 6% | Validar com contador |
| Fórmula da planilha subestima receita (7.2) | Resultado anual da planilha pior que o real | Reportado; fórmula corrigida mostrada em paralelo |
| Pesquisa com apenas 20 respondentes | Indício de disposição a pagar, não prova | Ampliar a amostra e validar com pré-vendas |
| Capital próprio dos sócios | Plano depende do aporte de R$ 90 mil | Parcelas condicionadas; cenário alternativo de seed |

---

## 13. Pendências e próximos passos

**Definições em aberto**

- Nome da moeda interna: por ora, apenas "créditos".
- Confirmar a cota de créditos de cada plano (200, 750 e 1.300) medindo o custo real por crédito no MVP (seção 2.5).
- Preço dos pacotes de créditos extras (proposta de R$ 59, R$ 159 e R$ 499, seção 2.5), inclusive se o anual deve ter preço menor por crédito extra.
- Subfaixas internas da faixa Business (hoje só existe o piso de R$ 449).
- Validação jurídica da política de cancelamento e reembolso do anual (seção 2.6).
- Se os créditos mensais do plano anual seguem expirando todo mês (premissa atual).
- Regime tributário.
- Se o mix de planos do cenário base continua em 35/65 ou passa a um valor mais prudente, como 50/50 (Anexo C.3).

**Para validar**

- Pré-venda ou teste de preço com respondentes da pesquisa (principalmente o Pro de R$ 279).
- Recorte brasileiro de TAM, SAM e SOM (IBGE, Sebrae, relatórios do setor).
- Custo real de inferência no MVP.
- Aplicar, ou não, a correção de fórmula da planilha com a professora (7.2).

---

## Anexo A: Mapa de preenchimento da planilha

Aba **Premissas**, apenas as células amarelas de entrada (todas as fórmulas e as demais abas permanecem como no original).

| Linha | Campo | Ano 1 | Ano 2 | Ano 3 |
|---|---|---|---|---|
| 7 | Descrição da receita (Linha 1) | Assinatura Starter/Pro + créditos extras | idem | idem |
| 8 | Ticket médio (R$) | 222 | 234 | 251 |
| 9 | Novos clientes por mês | 3 | 16 | 28 |
| 10 | Churn mensal | 8% | 6% | 5% |
| 15 | Descrição da receita (Linha 2) | Assinatura faixa Business (a partir de R$ 449) + créditos extras | idem | idem |
| 16 | Ticket médio (R$) | 511 | 538 | 572 |
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

## Anexo B: Entradas para reproduzir o cenário acelerado com seed na planilha

Trocar na aba Premissas (demais células como no Anexo A). A planilha vai subestimar o ano 3 pelo problema descrito em 7.2.

| Linha | Campo | Ano 1 | Ano 2 | Ano 3 |
|---|---|---|---|---|
| 9 | Novos clientes por mês | 3 | 22 | 38 |
| 17 | Média de assinaturas Business | 0,5 | 6 | 14 |
| 23 | Pessoal (R$/mês) | 0 | 12.000 | 24.000 |
| 24 | Marketing (R$/mês) | 1.000 | 5.000 | 8.000 |
| 25 | Vendas (R$/mês) | 0 | 1.000 | 2.500 |
| 26 | Tecnologia (R$/mês) | 1.200 | 3.000 | 5.000 |
| 27 | Administrativo (R$/mês) | 600 | 1.100 | 1.800 |
| 37 | Capital próprio (R$) | 30.000 | 0 | 0 |
| 38 | Captação externa (R$) | 150.000 | 0 | 0 |

## Anexo C: Registro de premissas

Este anexo reúne **todas as premissas** do business case em um só lugar, com a origem de cada uma, a justificativa, o que acontece se ela estiver errada e como validá-la. A seção 5 mostra os valores inseridos na planilha; aqui está o raciocínio por trás deles.

### C.1 Como ler

**Origem**
- **Dado:** vem de uma fonte citada (estudo de mercado, pesquisa de validação, material da disciplina).
- **Benchmark:** referência de mercado usada como ponto de partida.
- **Decisão do grupo:** definida pelos sócios.
- **Estimativa nossa:** hipótese sem evidência direta; precisa de validação.

**Confiança:** Alta (dado verificável), Média (benchmark ou decisão com respaldo), Baixa (estimativa sem evidência).

**Premissas de confiança baixa que mais movem o resultado:** mix de planos (P03), créditos extras (P05), novos clientes por mês (P08), churn (P09) e COGS (P12). A seção C.3 mostra o efeito de errá-las.

### C.2 Registro

**A. Preço e receita**

| ID | Premissa e valor | Origem | Justificativa | Confiança | Como validar |
|---|---|---|---|---|---|
| P01 | Planos: Starter R$ 89, Pro R$ 279, Business a partir de R$ 449 (sob orçamento) | Decisão do grupo | O estudo de mercado propunha Starter R$ 197 e Pro R$ 497. O benchmark de entrada (Artificial Societies, US$ 40 por mês, cerca de R$ 220) é maior que o nosso Starter. O Starter mira os 25% da pesquisa que gastam até R$ 100; o Business mira os 45% que pagariam R$ 300 ou mais | Média | Teste de preço e pré-venda com respondentes da pesquisa |
| P02 | Plano anual: R$ 790, R$ 2.490 e a partir de R$ 3.990 por ano, pago antecipadamente (cerca de 26% abaixo de 12 mensalidades) | Decisão do grupo | O preço mensal foi definido para o anual parecer claramente mais atrativo; compra fidelidade e caixa antecipado. Ver Anexo D | Média | Medir a adesão real ao anual |
| P03 | Mix de assinaturas Starter/Pro: 35/65, 30/70 e 25/75 nos anos 1, 2 e 3 | Estimativa nossa | Supõe que o hábito de uso empurra os clientes para o Pro. **Não há evidência.** Na pesquisa, metade gasta até R$ 100 ou nada, o que sugere mais assinaturas no Starter; e os preços foram ajustados sem que o mix fosse refeito. **Provavelmente é otimista.** | Baixa | Distribuição real de planos no lançamento |
| P04 | Adesão ao plano anual: 20%, 30% e 35% das assinaturas | Estimativa nossa | Crescimento gradual da confiança no produto | Baixa | Medir a adesão |
| P05 | Créditos extras como % da mensalidade: Linha 1 com 10%, 14% e 19%; Business com 20%, 30% e 40% | Estimativa nossa | Clientes maiores e mais maduros usam mais saldo. Sem dado de consumo | Baixa | Consumo real de créditos no MVP |
| P06 | Piso do Business: R$ 449 usado como mensalidade-base | Decisão do grupo | Conservador: o ticket real será igual ou maior. Subfaixas ficam para o futuro | Média | Orçamentos reais |
| P07 | Assinaturas Business (média no ano): 0,5, 4 e 10 | Estimativa nossa | Ano 1: 1 assinatura a partir do mês 7, via parceria com agências | Baixa | Pipeline de agências |

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
| P21 | Horizonte de 36 meses, sem valor residual, depreciação, juros ou imposto de renda. O EBITDA aproxima o caixa operacional (sem capital de giro) | Simplificação do modelo da planilha | A planilha trabalha assim | Média | n.a. |
| P22 | O modelo mensal é a referência de cálculo; a planilha é lida em paralelo (seção 7.2) | Decisão metodológica | A planilha anual não mostra o caixa mínimo e subestima a receita nos anos 2 e 3 | Média | Decisão com a professora |
| P23 | Adiantamento do plano anual: cobrança distribuída ao longo do ano e 70% de renovação; **fora dos números** | Estimativa nossa | Folga conservadora; é obrigação de entrega, não lucro | Baixa | Dados de cobrança |
| P24 | ROI = caixa acumulado em 36 meses ÷ capital máximo investido. Payback do capital = mês em que o caixa acumulado volta a zero. CAC payback = CAC ÷ (ticket × margem bruta) | Definição nossa, alinhada ao material da disciplina | O PDF define o ROI como (ganho − investimento) ÷ investimento | Média | n.a. |
| P25 | TAM e SAM: 5 a 8% do mercado global para research software e dados sintéticos; América Latina com 2 a 3% | Dado, do estudo de mercado | Fontes citadas lá (ESOMAR e outras) | Média | Recorte brasileiro pendente |
| P26 | Disposição a pagar: pesquisa de 20 respondentes | Dado | n pequeno; sem garantia de representatividade | Baixa | Ampliar a amostra |
| P27 | Cenários: pessimista (metade dos novos clientes e das assinaturas Business, churn de 10%, 8% e 7%, custos cortados), otimista (50% mais novos clientes e assinaturas, churn de 6%, 4,5% e 4%) | Estimativa nossa | Faixa de ±50% em volume, ordem de grandeza de uma startup em estágio inicial | Baixa | n.a. |

**F. Créditos e regras de contratação**

| ID | Premissa e valor | Origem | Justificativa | Confiança | Como validar |
|---|---|---|---|---|---|
| P28 | Uma assinatura é um espaço de trabalho compartilhado: Starter com 1 usuário, Pro com até 3, Business com até 10 | Estimativa nossa | O custo vem dos créditos, então os usuários não o elevam. O limite diferencia os planos e evita um Starter servindo uma equipe | Baixa | Perfil real de uso |
| P29 | 1 crédito é a resposta de uma persona; custo de R$ 0,14 por crédito | Estimativa nossa, com base em dado | Estudo de mercado: US$ 0,01 a 0,06 por resposta (R$ 0,06 a R$ 0,33). Adotado o ponto médio. Referência de cálculo: 1.500 tokens de entrada e 400 de saída a US$ 3 e US$ 15 por milhão, ou R$ 0,06 | Baixa | Medir no MVP |
| P30 | Saldo mensal: Starter 200, Pro 750 e Business 1.300 créditos | Estimativa nossa | Preço por crédito cai nos planos maiores (R$ 0,45, R$ 0,37 e R$ 0,35 no mensal; R$ 0,33, R$ 0,28 e R$ 0,26 no anual). Custo no saldo cheio de 31%, 38% e 41% do preço mensal, e de 43%, 51% e 55% no anual: Business e anual acima da regra de 40%, aceitável com uso médio de 70% (22% a 28% no mensal, 30% a 38% no anual) | Baixa | Custo real por crédito |
| P31 | Créditos do plano e extras valem até o fim do período contratado; depois, são perdidos | Decisão do grupo | Coerente com a expiração mensal do saldo e com a regra dos créditos extras | Média | Revisão jurídica |
| P32 | Plano anual pago adiantado e sem reembolso; quem cancela usa até o fim do plano e não renova | Decisão do grupo | Prática comum em SaaS anual. Pode haver exceção legal de 7 dias de arrependimento | Média | Revisão jurídica |
| P33 | Créditos extras vendidos em pacotes de 100, 300 e 1.000 créditos, a R$ 59, R$ 159 e R$ 499 (R$ 0,59, R$ 0,53 e R$ 0,50 por crédito), com o mesmo preço no mensal e no anual | Estimativa nossa | Cinco regras (seção 2.5): acima do crédito de qualquer plano (R$ 0,26 a R$ 0,45); dois pacotes de 300 passam a diferença Starter e Pro (R$ 190), o que incentiva a troca de plano; margem de 72% a 76% com custo de R$ 0,14 e de 34% a 44% com R$ 0,33; desconto de volume de cerca de 15%; pacote de entrada menor que a mensalidade do Starter. Média simples de R$ 0,54 por crédito. Não altera a receita projetada (P05 continua valendo) | Baixa | Teste de preço; custo real por crédito; preço do extra no anual |
| P34 | Teste gratuito: 200 créditos de boas-vindas por cadastro, sem cartão. **Não está no modelo financeiro** | Decisão do grupo | Custo de R$ 28 por cadastro (200 × R$ 0,14). Com conversão de 5% (referência não validada), são 720, 3.840 e 6.720 cadastros nos anos 1, 2 e 3, ou R$ 20 mil, R$ 108 mil e R$ 188 mil por ano com o bônus inteiro consumido, de 73% a 22% da receita. O CAC completo do ano 2 iria de R$ 625 para R$ 1.185, e o LTV/CAC de 4,2 para 2,2. Com 50 créditos, seria R$ 7 por cadastro e LTV/CAC de 3,4 | Baixa | Taxa de uso do bônus e conversão reais |

### C.3 O que acontece se as premissas frágeis estiverem erradas

Modelo mensal, uma alteração por vez (ou combinada, quando indicado). O aporte necessário é o caixa mínimo; os R$ 90 mil só são suficientes se esse valor ficar abaixo deles.

| Premissa alterada | Ticket Linha 1, ano 1 | Receita ano 3 | EBITDA ano 3 | Aporte necessário | Payback |
|---|---|---|---|---|---|
| **Base** (mix 35/65, extras 10%) | R$ 222 | R$ 865 mil | +R$ 229 mil | R$ 50 mil | Mês 26 |
| P03: mix 50/50 em todos os anos | R$ 192 | R$ 700 mil | +R$ 127 mil | R$ 60 mil | Mês 31 |
| P03: mix 65% Starter / 35% Pro | R$ 162 | R$ 602 mil | +R$ 66 mil | R$ 72 mil | Mês 36 |
| P05: sem créditos extras (L1 e Business) | R$ 202 | R$ 718 mil | +R$ 138 mil | R$ 59 mil | Mês 31 |
| P03 + P05: mix 50/50 e sem créditos extras | R$ 175 | R$ 579 mil | +R$ 52 mil | R$ 73 mil | Não ocorre em 36 meses |
| P10: lançamento no mês 10 | R$ 222 | R$ 851 mil | +R$ 221 mil | R$ 67 mil | Mês 29 |
| P10: lançamento no mês 13 | R$ 222 | R$ 834 mil | +R$ 210 mil | R$ 83 mil | Mês 30 |
| Estresse: mix 50/50 e lançamento no mês 10 | R$ 192 | R$ 689 mil | +R$ 120 mil | R$ 77 mil | Mês 33 |
| P12: COGS de 45%, 40% e 35% | R$ 222 | R$ 865 mil | +R$ 169 mil | R$ 58 mil | Mês 30 |
| P17: imposto de 15,5% no ano 1 (fator R) | R$ 222 | R$ 865 mil | +R$ 229 mil | R$ 54 mil | Mês 27 |
| P02/P04: sem plano anual (churn de 9%, 7% e 6%) | R$ 234 | R$ 889 mil | +R$ 244 mil | R$ 47 mil | Mês 25 |

Leitura:

1. **O mix é a premissa mais frágil.** Se ele for 50/50, o resultado cai cerca de 19% na receita do ano 3 e 45% no EBITDA, mas o aporte de R$ 90 mil ainda cobre com folga. Com 65% no Starter, o aporte necessário é de R$ 72 mil e o capital só se recupera no mês 36.
2. **O aporte de R$ 90 mil cobre todas as combinações testadas.** A mais pesada, mix 50/50 sem créditos extras, exige R$ 73 mil, mas o capital não se recupera em 36 meses.
3. **Atrasar o lançamento custa mais no caixa que no resultado:** um atraso de 6 meses (mês 13) leva o aporte necessário a R$ 83 mil, o mais perto do limite.
4. **Com o preço mensal atual, o plano anual custa receita no modelo** (cerca de 3% da receita do ano 3), porque o desconto de cerca de 26% pesa mais que o ganho de churn. O ganho do anual está no caixa antecipado e na fidelização, que não entram nos números (P23). Esse custo é o preço de tornar o anual atraente.
5. **Funil não modelado (P08):** os novos clientes por mês são uma meta, não o resultado de um funil. Com conversão de 5%, exigem de 120 a 560 cadastros por mês, e isso não foi validado.

**Ponto em aberto:** o cenário base mantém o mix 35/65. Diante da evidência de que ele é otimista, o grupo precisa decidir se adota um mix mais prudente (por exemplo, 50/50) como base.

## Anexo D: Registro de decisões

Cada decisão que altera premissas do modelo fica registrada aqui, com a data, o motivo e o efeito nos números, para mantermos a rastreabilidade.

### D.1 Preço mensal mais alto para valorizar o plano anual (2 de novembro de 2026)

**Decisão do grupo.** Manter o preço anual como estava (R$ 790, R$ 2.490 e a partir de R$ 3.990) e aumentar o preço mensal, de R$ 79, R$ 249 e a partir de R$ 399 para **R$ 89, R$ 279 e a partir de R$ 449**.

**Motivo.** Com o anual igual a 10 mensalidades, a economia era de 16,7% e o plano anual não se destacava. Com o novo mensal, o anual fica cerca de **26% abaixo de 12 mensalidades** (R$ 278, R$ 858 e a partir de R$ 1.398 por ano), e a diferença se vê no primeiro olhar. Em texto voltado ao cliente, não se cita a quantidade de meses: aparece só o valor a pagar e a economia em reais.

**O que foi mantido.** Proporção de planos (35/65 a 25/75), adesão ao anual (20%, 30% e 35%), créditos extras, churn combinado (8%, 6% e 5%), novos clientes por mês, custos, capital e cotas de créditos. Ou seja, o novo cálculo supõe a mesma demanda de antes; o efeito de uma demanda menor está testado à parte (D.1.3).

**D.1.1 Efeito nos números (cenário base, projeção mensal):**

| Indicador | Antes (mensal R$ 79, R$ 249 e a partir de R$ 399) | Depois (mensal R$ 89, R$ 279 e a partir de R$ 449) |
|---|---|---|
| Economia do anual sobre 12 mensalidades | 16,7% | cerca de 26% |
| Ticket médio da Linha 1 (anos 1, 2 e 3) | R$ 202, R$ 214 e R$ 231 | R$ 222, R$ 234 e R$ 251 |
| Ticket médio da Linha 2 | R$ 463, R$ 493 e R$ 526 | R$ 511, R$ 538 e R$ 572 |
| Receita (anos 1, 2 e 3) | R$ 25 mil, R$ 292 mil e R$ 796 mil | R$ 28 mil, R$ 319 mil e R$ 865 mil |
| EBITDA (anos 1, 2 e 3) | −R$ 20 mil, +R$ 10 mil e +R$ 186 mil | −R$ 18 mil, +R$ 26 mil e +R$ 229 mil |
| Caixa mínimo (aporte necessário) | R$ 56 mil, no mês 17 | R$ 50 mil, no mês 16 |
| EBITDA mensal positivo de forma sustentada | Mês 18 | Mês 17 |
| Payback do capital | Mês 29 | Mês 26 |
| ROI em 36 meses | Cerca de 285% | Cerca de 436% |
| LTV/CAC completo (ano 2) | 3,8 | 4,2 |
| Preço por crédito no plano mensal | R$ 0,40, R$ 0,33 e R$ 0,31 | R$ 0,45, R$ 0,37 e R$ 0,35 |
| Custo de inferência no saldo cheio (mensal) | 35%, 42% e 46% do preço | 31%, 38% e 41% do preço |

**D.1.2 Onde a mudança foi aplicada.** Planilha preenchida (tickets médios das linhas 8 e 16 e descrição da linha 15), apresentação (slides de planos, ticket médio, projeção, indicadores, capital, cenários, sensibilidade e premissas), este documento e o guia de bolso.

**D.1.3 Riscos e o que validar.**
- O preço mensal mais alto pode reduzir a conversão no plano mensal. Com 15% menos novos clientes na Linha 1, o ano 3 ainda fecha com receita de R$ 746 mil, EBITDA de +R$ 155 mil e aporte necessário de R$ 59 mil.
- Um anual mais barato deve aumentar a adesão ao anual, mas o modelo mantém 20%, 30% e 35%. Se a adesão subir, o ticket médio cai e o churn também.
- Sem o plano anual, a receita do ano 3 seria cerca de 3% maior no modelo. O anual passa a custar receita em troca de caixa antecipado e fidelização.
- O ganho do resultado é mecânico: o cálculo supõe que o mesmo número de clientes aceita pagar mais. Só o teste de preço no lançamento mostra se isso se sustenta.

### D.2 Pacotes de créditos extras (2 de novembro de 2026)

**Decisão do grupo (proposta aceita para o slide de planos).** Os créditos extras passam a ser vendidos em três pacotes: **100 créditos por R$ 59, 300 por R$ 159 e 1.000 por R$ 499**. Antes havia só uma sugestão de R$ 0,55 por crédito, sem pacotes definidos (P33).

**Motivo.** As cinco regras estão na seção 2.5: preço acima do crédito de qualquer plano, incentivo à troca de plano, margem positiva mesmo com o custo no teto da faixa, desconto de volume pequeno e tamanhos ligados ao uso.

**Efeito nos números.** Nenhum nos resultados projetados. O modelo continua com créditos extras de 10%, 14% e 19% da mensalidade na Linha 1 e de 20%, 30% e 40% no Business (P05); os pacotes só definem quantos créditos esse gasto compra e a margem de cada crédito vendido. A média simples de R$ 0,54 por crédito é próxima dos R$ 0,55 anteriores.

**Onde foi aplicado.** Slide de planos da apresentação (faixa de pacotes, com a validade dos créditos extras e a nota sobre o preço "a partir de" do Business passando a notas de rodapé), seção 2.5, riscos, pendências e premissa P33 deste documento, e o guia de bolso. A planilha não muda.

**Riscos e o que validar.**
- Nenhum teste de disposição a pagar: o preço é uma proposta.
- No anual, o crédito extra custa de 1,5 a 2,3 vezes o crédito do plano. Testar um preço menor.
- Se o custo real por crédito ficar no teto da faixa (R$ 0,33), a margem do pacote de 1.000 cai para 34%.

