# Dashboard Comercial — Power BI

Projeto de análise de vendas em Power BI com dados fictícios e foco em **KPIs comerciais**, **modelagem em estrela** e **ETL no Power Query**. Inclui arquivo PBIX e dataset para reprodutibilidade.

**Principais respostas de negócio:** Quais produtos e categorias lideram a receita? Como evolui o faturamento por mês? Quais regiões/canais contribuem mais? Quem são os top sellers? Como está o **Meta x Realizado** e o crescimento vs. período anterior?

**Como abrir:**  
1) Baixe/clone o repositório.  
2) Power BI Desktop → abra `pbix/Mini-Projeto2.pbix`.  
3) Se necessário, ajuste parâmetros de caminho no Power Query para `data/`.  
4) Atualize com **Refresh**.

**Destaques do dashboard:** navegação simples, segmentações por período/produto/região/vendedor(a), visuais comparativos (tendência mensal, barras por contribuição), KPIs em cartões e análise de produtividade.

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
