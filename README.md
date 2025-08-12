# Dashboard Comercial — Power BI

Projeto de análise de vendas em Power BI com dados fictícios e foco em **KPIs comerciais** e **ETL no Power Query**. Inclui arquivo PBIX e dataset para reprodutibilidade.

**Principais perguntas de negócio:** Quais produtos e categorias lideram a receita? Como evolui o faturamento por mês? Quais regiões/canais contribuem mais? Quem são os top sellers?

**Como abrir:**  
1) Baixe/clone o repositório.  
2) Power BI Desktop → abra `pbix/Mini-Projeto2.pbix`.  

**Destaques do dashboard:** navegação simples, segmentações por período/produto/região/vendedor(a), visuais comparativos (tendência mensal, barras por contribuição), KPIs em cartões e análise de produtividade.

### Prints do Dashboard

**Índice**
**Índice**  
Visão geral com navegação por seções do dashboard.  
![Índice do dashboard](https://raw.githubusercontent.com/myhtorres/powerbi-analise-comercial/main/images/Indice.png)

**Narrativa Inteligente**  
Resumo textual automático destacando os maiores faturamentos entre fabricantes e segmentos.  
![Narrativa Inteligente](https://raw.githubusercontent.com/myhtorres/powerbi-analise-comercial/main/images/Narrativa%20Inteligente.png)

**Principais Influenciadores**  
Visual de "principais influenciadores" que mostra como segmento e categoria impactam o Valor de Venda.  
![Principais Influenciadores](https://raw.githubusercontent.com/myhtorres/powerbi-analise-comercial/main/images/Principais%20Influenciadores.png)

**Total Valor Venda por Categoria**  
Gráfico de barras mostrando o volume de vendas por categoria.  
![Total valor venda por categoria](https://raw.githubusercontent.com/myhtorres/powerbi-analise-comercial/main/images/Total%20valor%20venda%20por%20categoria.png)

**Total Valor Venda por Estado e Vendedor**  
Mapa ou visual de localização geográfica, mostrando a contribuição por estado e vendedor.  
![Total valor venda por estado](https://raw.githubusercontent.com/myhtorres/powerbi-analise-comercial/main/images/Total%20valor%20venda%20por%20estado.png)

**KPIs implementados (exemplos):**  
- Receita / Faturamento  
- Quantidade vendida  
- Ticket médio  
- Meta x Realizado (% e var. abs.)  
- Crescimento % vs. período anterior  
- Participação por Categoria / Região / Canal  
- Produtividade por Vendedor(a)

**ETL (Power Query) – visão geral:**  
- Tipagem/limpeza de colunas, normalização de datas e percentuais.  
- Derivação de colunas de negócio (ex.: margem/percentual de comissão).  
- Parâmetros de caminho para facilitar portabilidade do `data/`.

**Dados do repositório:**  
- `data/Dados_Comerciais.xlsx`  
  - **Aba**: `Vendas` — 457 linhas, 14 colunas  
  - **Colunas** (principais): `ID-Produto`, `Produto`, `Categoria`, `Segmento`, `Fabricante`, `Loja`, `Cidade`, `Estado`, `Vendedor`, `ID-Vendedor`, `Comissão (Percentual)`, `Data Venda`  
- `pbix/Mini-Projeto2.pbix` → arquivo final do dashboard

**Licença:** MIT (veja `LICENSE`).

> Feito com 💛 por Myrelle.
