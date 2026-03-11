# Identificação de Perfis de Consumidores: Matriz RFM e Clustering

Este projeto tem como objetivo a segmentação de uma base de clientes utilizando a metodologia RFM (Recência, Frequência, Valor Monetário) e o algoritmo de clusterização K-Means. A análise transforma dados brutos de vendas em perfis de consumidores considerando suas características de consumo, facilitando a personalização e o direcionamento de campanhas de marketing, visando aumento da retenção de consumidores.

### Metodologia de Análise

O pipeline de dados foi estruturado da seguinte forma:

* **Tratamento de Dados**: Tratamento das bases de vendas, produtos e clientes para a criação das métricas de Recência, Frequência e Valor Monetário.
* **Normalização**: Aplicação de transformação logarítmica (`log1p`) para diminuir o impacto de outliers e reduzir a variância dos dados financeiros.
* **Modelagem**: Padronização das variáveis e definição do número ideal de clusters (k=3) através do Método Elbow.

### Resumo dos conteúdos das bases da dados

**Planilha CLIENTES**:
ID_CLIENTE, NOME_CLIENTE, CIDADE, UF

**Planilha VENDAS**:
ID_VENDA, DATA_VENDA, ID_FILIAL, ID_CLIENTE, VALOR_VENDA

**Planilha VENDAS_PRODUTOS**:
ID_VENDA, ID_PRODUTO, QUANTIDADE, VALOR_UNITARIO_VENDA_PRODUTO, VALOR_VENDA_PRODUTO


### Perfis de Consumo Identificados

**VIP / Elite (418 clientes)**
Representam o grupo com a maior frequência de compra e o maior valor monetário individual da base. Para este perfil, a estratégia recomendada é a **retenção e exclusividade**, utilizando atendimento personalizado e benefícios diferenciados para proteger este faturamento de alto nível.

**Recorrente / Fiel (1.260 clientes)**
Este é o maior segmento identificado. São clientes que compram de forma estável e possuem um volume financeiro equilibrado. O objetivo aqui é a **rentabilização**, buscando aumentar o ticket médio por meio de ofertas complementares (*cross-selling*).

**Ocasional (947 clientes)**
Composto por consumidores com gasto e frequência inferiores, geralmente inativos há mais tempo. Este grupo apresenta maior risco de abandono (*churn*), exigindo táticas de **reativação** com campanhas promocionais direcionadas.

### Resultados e Impacto de Negócio

Além da segmentação dos clientes, pode-se realizar outras análises nas vendas. Um exemplo de análise foi identificar que quase 90% da receita — cerca de R$ 3,94 milhões de um faturamento total de R$ 4,39 milhões — está concentrada nos grupos VIP e Fiel. Esse dado muda a perspectiva do negócio: o crescimento não depende apenas de adquirir novos clientes, mas de manter a recorrência de quem já sustenta a maior parte da operação.

Com essa segmentação, o marketing deixa de enviar comunicações genéricas e passa a atuar de forma estratégica:

**Foco em Retenção**: Ações de exclusividade para os 418 clientes VIP e programas de fidelidade para os 1.260 clientes Fiéis.

**Recuperação de Receita**: Estratégias de reativação para os clientes Ocasionais, que movimentaram R$ 457.574,05, mas apresentam alto risco de abandono.
