# Dashboard Comercial — Performance de Vendas (Power BI)

Este repositório contém um dashboard de vendas desenvolvido no **Microsoft Power BI** a partir de dados fictícios de uma operação comercial. O objetivo é demonstrar modelagem, ETL com Power Query, construção de medidas **DAX** e boas práticas de documentação para portfólio.

## 🎯 Objetivos do Projeto
- Visualizar a **performance de vendas** por período, produto, categoria, região e vendedor(a).
- Responder perguntas de negócio como:
  - Quais produtos lideram o faturamento?  
  - Como está a evolução mensal de vendas?  
  - Quais regiões e canais mais contribuem para a receita?  
  - Quem são os top sellers?  
- Demonstrar recursos do Power BI como **navegação por índice/menu**, **Principais Influenciadores**, **Gráfico de Faixas** e **Narrativa Inteligente**.

## 🗂️ Estrutura do Repositório
```
dashboard-comercial-powerbi/
├─ README.md
├─ LICENSE
├─ .gitignore
├─ .gitattributes
├─ /images/                 # prints/GIFs do dashboard (adicione aqui)
├─ /data/
│   └─ Dados_Comerciais.xlsx
├─ /pbix/
│   └─ Mini-Projeto2.pbix
├─ /docs/
│   ├─ MP2.pdf
│   ├─ O_Que_Representa_Area_Comercial.pdf
│   └─ Principais_KPIs_Area_Comercial.pdf
└─ /scripts/
    ├─ /powerquery/         # consultas M (.pq) - adicione se exportar
    ├─ /dax/                # medidas DAX (.dax) - adicione se exportar
    └─ /sql/                # scripts SQL (se houver)
```

## 🧭 Como Abrir e Reproduzir
1. **Baixe/clone** este repositório.
2. Abra no Power BI Desktop:
   - **PBIX**: `pbix/Mini-Projeto2.pbix`
3. Caso altere caminhos locais, ajuste parâmetros no Power Query (por exemplo, pasta `data/`).  
4. Clique em **Refresh** para atualizar as consultas.

> **Dica:** Para versionamento mais granular (ideal para PRs e diffs), salve como **Power BI Project (.pbip)**: `File > Save as > Power BI Project`. Assim, o modelo/relatório ficam em arquivos texto versionáveis.

## 📊 Principais KPIs (exemplos)
- **Receita / Faturamento**
- **Quantidade Vendida**
- **Ticket Médio**
- **Meta x Realizado**
- **Crescimento % vs. Período Anterior**
- **Participação por Categoria/Região/Canal**
- **Produtividade por Vendedor(a)**

> Ajuste esta lista conforme as medidas do seu modelo. Recomendo exportar as principais DAX para `scripts/dax/` com comentários.

## 🧱 Modelagem (resumo sugerido)
- **Esquema em estrela** com 1 tabela **Fato Vendas** e dimensões (ex.: **Produto**, **Cliente**, **Calendário**, **Região**, **Vendedor(a)**).
- **Relacionamentos** unidirecionais com cardinalidade muitos-para-um.
- **Calendário** com marcações (Ano, Mês, Trimestre, YTD, MTD).

## 🧼 ETL (Power Query)
- Limpeza de tipos, padronização de datas e moedas.
- Derivação de colunas de negócio (ex.: margem, categoria, canal).

## 📖 Dicionário de Dados (gerado automaticamente)
**Arquivo:** `data/Dados_Comerciais.xlsx`

**Abas encontradas:** Vendas

### Aba: `Vendas` — 457 linhas, 14 colunas

| Campo                 | Tipo (pandas)   | Exemplos (até 3)                                                                            |
|:----------------------|:----------------|:--------------------------------------------------------------------------------------------|
| ID-Produto            | object          | SKU-0000001, SKU-0000002, SKU-0000003                                                       |
| Produto               | object          | LG K10 TV Power, Geladeira Duplex, Lavadora 11 Kg                                           |
| Categoria             | object          | Celulares, Eletrodomésticos, Eletrônicos                                                    |
| Segmento              | object          | Corporativo, Doméstico, Industrial                                                          |
| Fabricante            | object          | LG, Brastemp, Electrolux                                                                    |
| Loja                  | object          | SP8821, A9990, SP8823                                                                       |
| Cidade                | object          | São Paulo, Belo Horizonte, Rio de Janeiro                                                   |
| Estado                | object          | São Paulo, Minas Gerais, Rio de Janeiro                                                     |
| Vendedor              | object          | Ana Teixeira, Josias Silva, Mateus Gonçalves                                                |
| ID-Vendedor           | int64           | 1009, 1006, 1003                                                                            |
| Comissão (Percentual) | int64           | 2, 3, 5                                                                                     |
| Data Venda            | datetime64[ns]  | 2012-10-04T00:00:00.000000000, 2012-01-01T00:00:00.000000000, 2012-02-02T00:00:00.000000000 |
| ValorVenda            | float64         | 679.0, 832.0, 790.0                                                                         |
| Custo                 | int64           | 345, 712, 390                                                                               |



## 🖼️ Prints / GIF de navegação
Adicione imagens do painel na pasta `images/` e referencie aqui:
- `images/overview.png`
- `images/detalhes-vendedor.png`
- `images/indice.gif`

## 📝 Roadmap / Melhorias Futuras
- Converter para **.pbip** e versionar M/DAX como texto.
- Criar **parâmetros de fonte** para alternar entre `data/sample` e dados reais.
- Adicionar **testes de medidas** (ex.: validação de totals vs. subtotais).

## 🧾 Licença
Este projeto é distribuído sob a licença **MIT** (veja `LICENSE`).

---

> Feito com 💛 por Myrelle — foco em BI, dados e traduções técnicas.
