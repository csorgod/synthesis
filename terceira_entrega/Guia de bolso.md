# Guia de bolso: premissas do Synthesis

Consulta rápida para a apresentação da Entrega 3. O detalhe de cada ponto está em `projecoes-financeiras-business-case.md`.

## 1. Resumo do modelo

- SaaS self-service. Cada assinatura, por empresa ou profissional, paga uma mensalidade que dá um saldo de créditos. Quem acaba o saldo pode comprar créditos extras, se quiser.
- Planos: Starter R$ 89, Pro R$ 279 e Business a partir de R$ 449 (sob orçamento). Plano anual: R$ 790, R$ 2.490 e a partir de R$ 3.990 por ano, cerca de 26% abaixo de 12 mensalidades.
- Capital próprio de R$ 90 mil, sem pró-labore para os sócios no 1º ano.

## 2. Regras de cobrança

| Regra | Definição |
|---|---|
| Unidade | Assinatura por empresa ou profissional, não por usuário |
| Saldo mensal | Expira no fim do ciclo |
| Créditos extras | Opcionais, acumulam enquanto a assinatura estiver ativa (no anual, durante o contrato) |
| Preço dos créditos extras | Pacotes de 100, 300 e 1.000 créditos, a R$ 59, R$ 159 e R$ 499 (R$ 0,59, R$ 0,53 e R$ 0,50 por crédito). Mesmo preço no mensal e no anual. Ver regras abaixo da tabela |
| Estouro do saldo | As simulações pausam, a menos que haja créditos extras ativos. Alertas aos 80% e 100% |
| Teste gratuito | 200 créditos de boas-vindas únicos, sem cobrança e sem cartão (custo de R$ 28 por cadastro; ver Anexo C, P34) |
| Plano anual | Preço fixo de R$ 790, R$ 2.490 e a partir de R$ 3.990, pago adiantado, com fidelidade. Os créditos mensais continuam expirando. Sem reembolso: quem cancela usa até o fim do plano e não renova |
| Usuários incluídos | Starter 1, Pro até 3, Business até 10 (espaço de trabalho compartilhado) |
| Saldo mensal por plano | Starter 200, Pro 750, Business 1.300 créditos. Preço por crédito menor nos planos maiores (R$ 0,45, R$ 0,37 e R$ 0,35 no mensal). Estudos por mês são aproximações: o consumo depende da complexidade |
| Se o cliente cancelar | Os créditos valem até o fim do período contratado; depois, são perdidos |

**Regras do preço dos pacotes de créditos extras:**
1. Acima do crédito de qualquer plano (R$ 0,26 a R$ 0,45), para o plano continuar sendo o caminho mais barato.
2. Incentivam a subir de plano: do Starter ao Pro são R$ 190 a mais por mês para 550 créditos a mais, e dois pacotes de 300 (R$ 318) já passam disso.
3. Margem de 72% a 76% com custo de R$ 0,14 por crédito, e de 34% a 44% se o custo for R$ 0,33.
4. Desconto de volume de cerca de 15% (de R$ 0,59 a R$ 0,50): maior que isso esvaziaria o plano.
5. Pacote de entrada (R$ 59) menor que a mensalidade do Starter (R$ 89); tamanhos ligados ao uso (100 = 10 testes rápidos; 1.000 = mais que um mês cheio do Pro).

Média simples de R$ 0,54 por crédito, perto dos R$ 0,55 da premissa P33. Não altera a receita projetada: os extras entram como 10%, 14% e 19% da mensalidade (Linha 1) e 20%, 30% e 40% (Business). Fragilidade: sem teste com cliente, e no anual o extra custa de 1,5 a 2,3 vezes o crédito do plano.

## 3. Premissas de receita

| Premissa | Ano 1 | Ano 2 | Ano 3 | Origem |
|---|---|---|---|---|
| Mix Starter / Pro | 35/65 | 30/70 | 25/75 | Estimativa nossa |
| Assinaturas anuais | 20% | 30% | 35% | Estimativa nossa |
| Créditos extras, Linha 1 (% da mensalidade) | 10% | 14% | 19% | Estimativa nossa |
| Créditos extras, Business | 20% | 30% | 40% | Estimativa nossa |
| **Ticket médio por assinatura, Linha 1** | **R$ 222** | **R$ 234** | **R$ 251** | Resultado das linhas acima |
| **Ticket médio por assinatura, Business** | **R$ 511** | **R$ 538** | **R$ 572** | Piso de R$ 449 com efeito do anual e extras |

Como sai o R$ 222: mensalidade média no mensal (0,35 × 89 + 0,65 × 279) = 212,50; no anual (0,35 × 65,83 + 0,65 × 207,50) = 157,92; com 20% das assinaturas no anual, 201,58; × 1,10 dos extras = 221,74.

O ticket é a receita média por assinatura e não coincide com o preço de nenhum plano. O mix de 65% no Pro é a hipótese mais frágil (ver seção 8).

## 4. Premissas de volume e retenção

| Premissa | Ano 1 | Ano 2 | Ano 3 | Origem |
|---|---|---|---|---|
| Novos clientes por mês, Linha 1 | 6 a partir do mês 7 (média de 12 meses: 3) | 16 | 28 | Estimativa nossa |
| Assinaturas Business (média do ano) | 0,5 | 4 | 10 | Estimativa nossa |
| Churn mensal, plano mensal | 9% | 7% | 6% | Estimativa nossa |
| Churn do plano anual | 3% ao mês equivalente (cerca de 30% de não renovação ao ano) | | | Estimativa nossa |
| **Churn combinado usado na planilha** | **8%** | **6%** | **5%** | Resultado das linhas acima |
| Lançamento | Mês 7 (MVP de 6 meses sem receita) | | | Decisão do grupo, alinhada ao 5W2H |

Os novos clientes são uma meta informada, não o resultado de um funil. Com 5% de conversão do trial, exigem cerca de 120, 320 e 560 cadastros por mês.

## 5. Premissas de custo

| Item (por mês) | Ano 1 | Ano 2 | Ano 3 | Origem |
|---|---|---|---|---|
| COGS (% da receita) | 38% | 33% | 28% | Estimativa nossa |
| Pessoal | R$ 0 | R$ 7.000 | R$ 14.000 | Decisão do grupo |
| Marketing | R$ 1.000 | R$ 2.500 | R$ 4.500 | Estimativa nossa |
| Vendas e comissões | R$ 0 | R$ 500 | R$ 1.500 | Estimativa nossa |
| Tecnologia fixa | R$ 1.200 | R$ 2.500 | R$ 4.000 | Estimativa nossa |
| Administrativo | R$ 600 | R$ 1.000 | R$ 1.600 | Estimativa nossa |
| Impostos sobre receita | 6% | 8% | 10% | Simples Nacional, a confirmar com contador |

- Investimento inicial de R$ 18 mil: tecnologia R$ 8 mil, marketing R$ 5 mil, abertura da empresa e LGPD R$ 5 mil. O MVP é desenvolvido pelos sócios.
- Regra de projeto do COGS: o custo de inferência com o saldo cheio deveria ficar em até 40% da mensalidade. O Business e o plano anual ultrapassam esse limite no uso máximo (tabela abaixo). Custo de LLM de US$ 0,05 a 0,30 por entrevista curta (estudo de mercado), câmbio de R$ 5,50.
- Pessoal zero no ano 1 é custo de oportunidade dos sócios, não custo nulo.

**Regra de inferência por plano.** Custo adotado de R$ 0,14 por crédito (ponto médio da faixa do estudo de mercado), como percentual da mensalidade:

| Plano | Créditos | Saldo cheio, mensal | Saldo cheio, anual | A 70% de uso, mensal | Se o crédito custar R$ 0,33, mensal |
|---|---|---|---|---|---|
| Starter | 200 | 31% | 43% | 22% | 74% |
| Pro | 750 | 38% | 51% | 26% | 89% |
| Business | 1.300 | 41% | 55% | 28% | 96% |

- No plano mensal, o Starter e o Pro respeitam a regra de 40%, e o Business fica um pouco acima. No plano anual, que cobra menos por mês, os três planos a ultrapassam quando o cliente usa o saldo inteiro.
- A premissa que sustenta isso é um uso médio de cerca de 70% do saldo. Com esse uso, o custo fica entre 22% e 28% do preço no mensal e entre 30% e 38% no anual.
- Pior caso: se o custo real por crédito chegar ao teto da faixa (R$ 0,33), o saldo cheio do plano anual passa de 100% do valor mensal equivalente (119% no Pro e 129% no Business), e o mensal chega a 96% no Business.
- Motivo da escolha: o grupo quer que o plano mais caro tenha o menor preço por crédito (R$ 0,45, R$ 0,37 e R$ 0,35 no mensal). Para o Business ficar nos 40% no mensal, bastaria um saldo de cerca de 1.280 créditos.
- Se o uso médio ficar acima do esperado, rever as cotas do Pro e do Business. O custo real por crédito só se mede no MVP.

## 6. Capital

| Item | Valor |
|---|---|
| Aporte principal | R$ 90 mil de capital próprio |
| Parcelas | R$ 35 mil no início, R$ 30 mil no lançamento do MVP, R$ 25 mil como reserva no mês 12 |
| Condição da parcela 3 | MRR de pelo menos R$ 3 mil no mês 12 |
| Alternativa | Seed de R$ 150 mil por volta do mês 9 |
| Variante com um sócio em tempo integral | Aporte necessário sobe para cerca de R$ 92 mil (recomendação: R$ 115 mil) |

O aporte foi dimensionado pelo caixa mínimo do modelo mensal, que é de R$ 50 mil no cenário base, no mês 16.

## 7. Resultados (cenário base)

| | Ano 1 | Ano 2 | Ano 3 |
|---|---|---|---|
| Receita, modelo mensal | R$ 28 mil | R$ 319 mil | R$ 865 mil |
| EBITDA, modelo mensal | −R$ 18 mil | +R$ 26 mil | +R$ 229 mil |
| MRR no fim do ano | R$ 7,1 mil | R$ 38,1 mil | R$ 91,2 mil |
| CAC (marketing e vendas) | R$ 333 | R$ 188 | R$ 214 |
| CAC completo (com pessoal) | R$ 333 | R$ 625 | R$ 714 |
| LTV | R$ 1.720 | R$ 2.613 | R$ 3.614 |
| LTV/CAC completo | 5,2 | 4,2 | 5,1 |
| MRR de equilíbrio | R$ 5,0 mil | R$ 22,9 mil | R$ 41,3 mil |

- EBITDA mensal positivo de forma sustentada a partir do mês 17. Payback do capital no mês 26.
- Mercado: TAM de US$ 142 bi, SAM regional (América Latina) de US$ 140 a 330 milhões, SOM de cerca de R$ 1,1 mi de ARR no fim do ano 3 (0,06% a 0,14% do SAM regional).

## 8. Onde o modelo é frágil

| Premissa alterada | Receita ano 3 | EBITDA ano 3 | Aporte necessário |
|---|---|---|---|
| Base | R$ 865 mil | +R$ 229 mil | R$ 50 mil |
| Mix 50/50 | R$ 700 mil | +R$ 127 mil | R$ 60 mil |
| Mix 65% Starter / 35% Pro | R$ 602 mil | +R$ 66 mil | R$ 72 mil |
| Sem créditos extras | R$ 718 mil | +R$ 138 mil | R$ 59 mil |
| Mix 50/50 e sem créditos extras | R$ 579 mil | +R$ 52 mil | R$ 73 mil |
| Lançamento no mês 13 | R$ 834 mil | +R$ 210 mil | R$ 83 mil |
| COGS de 45%, 40% e 35% | R$ 865 mil | +R$ 169 mil | R$ 58 mil |
| Metade dos novos clientes | | EBITDA negativo no ano 3 | |

- Nada disso foi validado com clientes. A pesquisa tem 20 respondentes e serve de indício de disposição a pagar.
- O mix 35/65 é provavelmente otimista. A decisão sobre usar 50/50 como base está em aberto.
- A variável que mais pesa é a aquisição de clientes.
- O custo real por crédito só se mede no MVP.

## 9. A fórmula da planilha

Na aba Premissas, as células D12 e E12 calculam `ticket × clientes_finais / 2 × 12`, mas a dica da célula F12 diz que o cálculo usa a média entre o início e o fim do ano. Isso subestima a receita da Linha 1 em 12% no ano 2 e 28% no ano 3.

| Leitura | Receita ano 3 | EBITDA ano 3 |
|---|---|---|
| Planilha como está | R$ 579 mil | +R$ 52 mil |
| Planilha com a média corrigida | R$ 807 mil | +R$ 193 mil |
| Modelo mensal | R$ 865 mil | +R$ 229 mil |

A correção proposta é `=D8*(C11+D11)/2*12` em D12 e `=E8*(D11+E11)/2*12` em E12. Não alteramos a fórmula original. Pendente: perguntar ao professor se a correção é aceita.

## 10. O que ainda está em aberto

- Nome da moeda interna (por ora, apenas "créditos").
- Confirmar a cota de créditos de cada plano com o custo real por crédito.
- Preço dos pacotes de créditos extras (testar com cliente; avaliar preço menor para o anual).
- Subfaixas do plano Business.
- Validação jurídica da política de cancelamento e reembolso do plano anual.
- Mix de planos do cenário base.
- Regime tributário.
- Recorte brasileiro de TAM, SAM e SOM.
