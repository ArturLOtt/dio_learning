# Xbox Game Pass — Análise de Vendas e Assinaturas

## Sobre o projeto

Este projeto tem como objetivo analisar dados de assinaturas do **Xbox Game Pass** e transformar os registros de vendas em informações úteis para apoiar a tomada de decisões.

A análise foi desenvolvida a partir de uma base de assinantes contendo informações sobre planos, valores das assinaturas, renovação automática e aquisição de benefícios adicionais, como **EA Play Season Pass** e **Minecraft Season Pass**.

O projeto utiliza uma abordagem de **análise exploratória e visualização de dados**, organizando os resultados em um dashboard para facilitar a interpretação dos principais indicadores comerciais.

---

## Objetivos

O projeto busca responder perguntas de negócio relacionadas ao desempenho das assinaturas, incluindo:

1. Qual é o faturamento das assinaturas de acordo com o tipo de plano?
2. Qual é o faturamento relacionado às assinaturas com e sem renovação automática?
3. Qual é o total de vendas do **EA Play Season Pass**?
4. Qual é o total de vendas do **Minecraft Season Pass**?
5. Como os diferentes planos contribuem para as vendas dos produtos adicionais?
6. Quais informações podem ser utilizadas para compreender melhor o comportamento dos assinantes?

---

## Dados utilizados

Os dados utilizados estão armazenados na aba **Bases** da planilha.

A base possui **295 registros de assinantes** e **13 campos**.

### Dicionário de dados

| Campo | Descrição |
|---|---|
| `Subscriber ID` | Identificador único do assinante |
| `Name` | Nome do assinante |
| `Plan` | Plano contratado |
| `Start Date` | Data de início da assinatura |
| `Auto Renewal` | Indica se a assinatura possui renovação automática |
| `Subscription Price` | Preço da assinatura |
| `Subscription Type` | Tipo de assinatura |
| `EA Play Season Pass` | Indica se o assinante adquiriu o EA Play Season Pass |
| `EA Play Season Pass Price` | Valor do EA Play Season Pass |
| `Minecraft Season Pass` | Indica se o assinante adquiriu o Minecraft Season Pass |
| `Minecraft Season Pass Price` | Valor do Minecraft Season Pass |
| `Coupon Value` | Valor do desconto aplicado por cupom |
| `Total Value` | Valor total da transação |

### Principais categorias

A base contém três planos:

- **Core**
- **Standard**
- **Ultimate**

Os tipos de assinatura disponíveis são:

- **Monthly**
- **Quarterly**
- **Annual**

A renovação automática possui duas possibilidades:

- `Yes`
- `No`

Os dados também registram a contratação dos produtos adicionais **EA Play Season Pass** e **Minecraft Season Pass**.

---

## Estrutura do arquivo

A planilha está organizada em quatro abas principais:

### `Assets`

Contém elementos utilizados na identidade visual do projeto, como a paleta de cores e outros recursos gráficos.

### `Bases`

Contém os dados brutos utilizados nas análises.

Essa é a principal fonte de dados do projeto.

### `Cálculos`

Contém as análises intermediárias e respostas para as perguntas de negócio.

Entre os cálculos realizados estão:

- faturamento relacionado às assinaturas;
- análise de renovação automática;
- vendas do EA Play Season Pass;
- vendas do Minecraft Season Pass;
- segmentação dos resultados por plano.

### `Dashboard`

Contém a apresentação visual dos resultados e indicadores encontrados durante a análise.

O dashboard foi desenvolvido para permitir uma visualização rápida do desempenho das vendas e facilitar a interpretação dos dados.

---

## Principais análises

### Faturamento por renovação automática

Uma das análises compara o valor das assinaturas de acordo com a existência de renovação automática.

Os dados apresentam os seguintes valores no cálculo realizado:

| Renovação automática | Valor |
|---|---:|
| Não | 2824 |
| Sim | 747 |
| **Total** | **3571** |

Esses valores permitem comparar a contribuição financeira dos clientes com e sem renovação automática.

---

### Vendas do EA Play Season Pass

A análise também verifica as vendas do EA Play Season Pass de acordo com o plano contratado.

Resultado identificado:

| Plano | Valor |
|---|---:|
| Core | 0 |
| Standard | 0 |
| Ultimate | 1350 |
| **Total** | **1350** |

Nesse conjunto de dados, o valor registrado para o EA Play Season Pass está concentrado no plano **Ultimate**.

---

### Vendas do Minecraft Season Pass

Também foi analisada a receita associada ao Minecraft Season Pass.

| Plano | Valor |
|---|---:|
| Core | 0 |
| Standard | 900 |
| Ultimate | 900 |
| **Total** | **1800** |

Os resultados indicam participação dos planos **Standard** e **Ultimate** nas vendas do produto adicional.

---

## Metodologia

O processo de análise pode ser resumido nas seguintes etapas:

```text
Base de dados
     ↓
Organização dos dados
     ↓
Identificação das variáveis
     ↓
Definição das perguntas de negócio
     ↓
Cálculos e agregações
     ↓
Análise dos resultados
     ↓
Construção do Dashboard
```

As informações foram agrupadas principalmente por:

- plano;
- tipo de assinatura;
- renovação automática;
- produtos adicionais;
- valor total das transações.

---

## Como reproduzir o projeto

### Requisitos

Para reproduzir a análise, é necessário:

- Microsoft Excel ou software compatível com arquivos `.xlsx`;
- arquivo contendo a base de dados;
- acesso às fórmulas, tabelas dinâmicas e elementos utilizados no dashboard.

Não são necessárias bibliotecas externas de programação para reproduzir a versão original do projeto.

### Passo 1 — Abrir a base

Abra o arquivo `.xlsx` e acesse a aba:

```text
Bases
```

Essa aba contém os registros utilizados na análise.

### Passo 2 — Conferir os dados

Verifique se os campos estão corretamente estruturados e se os valores das colunas possuem os tipos esperados.

Especial atenção deve ser dada aos campos:

```text
Subscription Price
EA Play Season Pass Price
Minecraft Season Pass Price
Coupon Value
Total Value
```

### Passo 3 — Reproduzir os cálculos

Utilize os dados da aba `Bases` para reproduzir as agregações apresentadas na aba `Cálculos`.

Os resultados devem ser agrupados conforme as perguntas de negócio definidas no projeto.

### Passo 4 — Atualizar o Dashboard

Após atualizar os cálculos, os resultados podem ser utilizados para alimentar os indicadores e gráficos da aba:

```text
Dashboard
```

Caso novos registros sejam adicionados à base, os cálculos e elementos visuais deverão ser atualizados para refletir os novos dados.

---

## Tecnologias e ferramentas

O projeto foi desenvolvido utilizando principalmente:

- **Microsoft Excel**
- Tabelas e fórmulas para tratamento e agregação dos dados
- Tabelas dinâmicas para análises
- Dashboard para visualização dos indicadores

---

## Estrutura recomendada para uma nova versão

Caso o projeto seja transformado em uma solução de análise utilizando Python, uma estrutura possível seria:

```text
xbox-game-pass-analysis/
│
├── data/
│   └── base_assinaturas.xlsx
│
├── notebooks/
│   └── analise.ipynb
│
├── src/
│   ├── data_processing.py
│   ├── analysis.py
│   └── dashboard.py
│
├── output/
│   └── resultados/
│
└── README.md
```

Nesse caso, o Python poderia ser utilizado para automatizar a importação, limpeza, transformação e análise dos dados.

---

## Resultados

O projeto demonstra como uma base relativamente simples de assinaturas pode ser transformada em informações para análise comercial.

Entre os principais indicadores calculados estão:

- valor total das transações;
- desempenho por tipo de assinatura;
- comportamento relacionado à renovação automática;
- vendas do EA Play Season Pass;
- vendas do Minecraft Season Pass;
- participação dos diferentes planos nas vendas adicionais.

O dashboard consolida essas informações em uma interface visual, permitindo que os resultados sejam interpretados de maneira mais rápida.

---

## Possíveis melhorias

Como próximos passos, o projeto pode ser expandido para incluir:

- evolução das vendas ao longo do tempo;
- faturamento mensal;
- ticket médio por plano;
- quantidade de assinantes por plano;
- taxa de renovação automática;
- participação percentual de cada plano;
- análise de descontos;
- análise de produtos adicionais por cliente;
- indicadores de crescimento;
- filtros interativos por período e plano;
- automação da atualização dos dados utilizando Python.

---

## Conclusão

O projeto utiliza dados de assinaturas do Xbox Game Pass para responder perguntas de negócio por meio de cálculos, agregações e visualizações.

A combinação entre **base de dados, análise e dashboard** permite transformar registros individuais de assinantes em indicadores que podem apoiar decisões relacionadas a vendas, planos, renovação automática e produtos adicionais.

A estrutura também pode servir como base para uma evolução futura utilizando ferramentas de **Business Intelligence, SQL e Python**, tornando o processo de atualização e análise mais automatizado e escalável.