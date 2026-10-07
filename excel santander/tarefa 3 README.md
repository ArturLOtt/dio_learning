# Porsche Sales Dashboard

## 1. Perguntas de negócio

A dashboard foi desenhada para responder três perguntas que podem orientar decisões comerciais, em vez de apenas apresentar gráficos:

1. **Quais modelos geram mais receita?**
   - Permite identificar os modelos que mais contribuem para o faturamento e comparar receita com volume de vendas.
   - Ajuda em decisões de mix de produtos, estoque, campanhas e priorização comercial.

2. **Onde as vendas estão concentradas?**
   - Compara a receita por estado e, por meio do filtro de cidade, permite aprofundar a análise geográfica.
   - Ajuda a encontrar mercados mais relevantes e oportunidades de expansão ou ações locais.

3. **Como os métodos de pagamento afetam volume e ticket médio?**
   - Compara receita e número de vendas por método de pagamento.
   - Ajuda a entender quais formas concentram faturamento e quais combinam maior/menor ticket.

### Indicadores de topo

- Total de vendas
- Receita
- Ticket médio
- Preço máximo

Todos os indicadores e gráficos respondem ao conjunto de filtros aplicado.

## 2. Prompt que gerou a dashboard

### Prompt inicial

> Tenho uma planilha com 100 vendas da Porsche, com modelo, cidade, estado, ano, preço e método de pagamento. Crie uma dashboard em HTML, arquivo único, que responda perguntas de negócio sobre as vendas. Inclua três perguntas de negócio, cada uma respondida por um gráfico ou indicador; filtros por modelo, cidade, ano e método de pagamento; indicadores de topo como total de vendas e receita; e um visual coerente, elegante e executivo, com paleta e tipografia consistentes. O resultado deve funcionar localmente em um único arquivo HTML, sem backend.

### O que mudou até a versão final

O prompt foi refinado para evitar uma dashboard genérica:

- As perguntas foram explicitadas como **decisões de negócio**, não como simples pedidos de gráficos.
- Foi acrescentado o filtro de **estado**, porque a análise geográfica fica mais útil junto com cidade.
- Foi definido que os gráficos devem reagir aos filtros em tempo real.
- Foram definidos indicadores de **ticket médio** e **preço máximo**, além de vendas e receita.
- Foi pedido que o gráfico de modelos mostre **receita + volume**, evitando interpretar faturamento sem considerar quantidade.
- Foi pedido que a análise de pagamento mostre **receita + volume**, permitindo enxergar concentração e ticket.
- A implementação final usa **HTML/CSS/JavaScript sem dependência de backend**, tornando o arquivo portátil.

## 3. Tratamento da base antes da IA

A planilha original contém a aba `Sanitized`, que já fornece campos tratados. Para a dashboard foram usados como fonte analítica os campos:

- `PorscheModelSanitized`
- `ModelYearSanitized`
- `SalesPriceSanitized`
- `PayMethodSanitized`
- `CitySanitized`
- `StateSanitized`
- `sale_id`

Tratamentos aplicados:

- Uso das colunas `Sanitized` em vez dos campos brutos, para reduzir inconsistências de texto, datas e números.
- Conversão do preço de venda para número.
- Conversão do ano do modelo para inteiro.
- Conversão do identificador da venda para inteiro.
- Verificação de duplicidade: os 100 `sale_id` são únicos.
- Preservação dos registros de venda; não foram inventados valores ausentes.
- A coluna `SaleDateSanitized` contém **24 datas classificadas como `INVALID`**. Como as três perguntas escolhidas não dependem de evolução mensal da venda, a data não foi usada nos gráficos e não foi “corrigida” artificialmente.
- A receita total da base é de aproximadamente **R$ 12,827,800.50** e o ticket médio é de aproximadamente **R$ 128,278.01**. A dashboard recalcula esses valores conforme os filtros.

## 4. Arquivos

- `index.html` — dashboard completa e interativa em arquivo único.
- `README.md` — documentação do raciocínio, prompt e tratamento da base.

## 5. Endereço da dashboard publicada

**Não publicada externamente nesta entrega.**

O ambiente desta conversa permite gerar o `index.html` pronto para download e hospedagem, mas não fornece um serviço de publicação web persistente com URL pública própria. Portanto, não foi inventado um endereço.

Para publicar, basta colocar `index.html` em um serviço de hospedagem estática, como GitHub Pages, Netlify ou Vercel. Depois disso, substitua esta seção pela URL pública gerada.

