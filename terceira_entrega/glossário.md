# Glossário

**CAC (Custo de Aquisição de Cliente):** É quanto você gasta, em média, para conquistar um cliente pagante.

* CAC = gasto total em aquisição ÷ novos clientes no período.
* Se você gasta R$ 10 mil em mídia e conteúdo e converte 50 clientes, o CAC é R$ 200.
* Há duas versões. O CAC "de mídia" soma só marketing e vendas, e é o que o dashboard da planilha calcula. O CAC "completo" inclui também o tempo do time dedicado à aquisição. A segunda é mais honesta, e a primeira é a que costuma aparecer em pitch.

**LTV (Lifetime Value):** É quanto um cliente deixa na empresa durante o tempo em que permanece.

* O PDF usa LTV = ticket mensal × meses de retenção.
* A planilha usa LTV = ticket × margem bruta ÷ churn. O prazo médio de vida do cliente é 1 ÷ churn, e a margem bruta desconta o custo de entregar o serviço.
* Com churn de 5%, o cliente dura em média 20 meses. A versão da planilha é melhor para o Synthesis, porque o custo de LLM é alto e ignorá-lo infla o LTV.
* A regra prática é LTV/CAC maior que 3.

**Payback e ROI:** Os dois falam de retorno, mas respondem perguntas diferentes.

* O **payback** mede **tempo**: em quantos meses o dinheiro investido volta ao caixa.
    * Na definição do PDF, é o investimento inicial ÷ receita líquida mensal.
    * Em SaaS usa-se muito o "CAC payback": CAC ÷ (ticket × margem bruta). Ele diz em quantos meses um cliente "paga" o custo de ser adquirido.
* O ROI mede proporção: quanto você ganhou em relação ao que investiu.
    * ROI = (ganho − investimento) ÷ investimento.
    * Um ROI de 60% diz que, para cada R$ 1 investido, voltou R$ 1,60.
* Um projeto pode ter ROI alto com payback longo, ou o contrário. O payback mede liquidez e risco, e o ROI mede rentabilidade.
* A fórmula de ROI no PDF vem rotulada como "Payback", mas é um erro de digitação. Usaremos a fórmula correta.

## Indicadores de SaaS.

* **MRR:** receita recorrente do mês, ou seja, clientes pagantes × valor da assinatura. Mostra a tração.
* **ARR:** MRR × 12. É o "tamanho" anualizado do negócio, e investidores o usam para valuation.
* **Churn:** percentual de clientes que cancelam no mês. Com churn de 5%, você perde metade da base em cerca de 13 meses se não repuser.
* **ARPU/ARPA:** receita média por usuário ou por conta. É o ticket médio efetivo.
* **Margem bruta:** (receita − custos diretos de entrega) ÷ receita. Mostra o que sobra de cada real para pagar time, marketing e lucro.
* **Burn rate:** quanto a empresa queima de caixa por mês (despesas − receita).
* **Runway:** meses de sobrevivência com o caixa atual, ou seja, caixa ÷ burn.
* **Taxa de conversão:** do trial gratuito para pagante. Valida o funil PLG.

**Vale da morte:** É o período entre o dinheiro acabar e a receita se sustentar.

* A startup já gastou para construir e adquirir clientes, mas a receita ainda não cobre os custos.
* As causas típicas são:
    * subestimar o prazo até a tração;
    * CAC acima do esperado;
    * churn alto;
    * captação que não sai.
* A projeção financeira serve para saber quanto dura a "pista" e quanto de caixa é preciso para atravessá-lo.
* No nosso modelo, ele cobre o ano 1 e o começo do ano 2.

**COGS (Cost of Goods Sold):** São os custos diretamente ligados a entregar o produto.

* No Synthesis: chamadas de LLM por simulação, cloud, armazenamento, taxa do gateway de pagamento e, às vezes, suporte.
* É o custo que cresce com o uso, ao contrário de salário e aluguel.
* Lucro bruto = receita − COGS.

**EBITDA:** É o resultado operacional antes de juros, impostos sobre lucro, depreciação e amortização.

* Na planilha: receita − COGS − custos operacionais − impostos sobre receita.
* Mostra se a operação em si dá lucro, sem considerar o financiamento. * Ele não é o caixa, porque não inclui investimento nem captação.

**PLG (Product-Led Growth):** O produto é o principal canal de aquisição.

* O usuário experimenta de graça (trial ou free), sente o valor sozinho e converte sem falar com vendedor.
* É o que o Synthesis planeja: trial sem cartão e primeira simulação feita pelo próprio usuário.
* Seus riscos são custo de LLM no plano gratuito, taxa de conversão baixa e churn de quem converte sem ter sentido o valor.