# Análise Exploratória de Dados - Bangladesh Weaving Dataset

Este repositório contém uma análise exploratória de dados (EDA) realizada sobre um conjunto de dados de produção têxtil de Bangladesh, com o objetivo de entender melhor os fatores que impactam o desperdício de tecido na produção.

## Estrutura do Projeto

- **fonte/**: Pasta contendo os arquivos de dados utilizados na análise:
  - `weaving_dataset_full.csv`: Arquivo principal com os dados de produção têxtil.
  - `another_data_source.csv` (se houver): Outras fontes de dados utilizadas.

- **bangladesh.ipynb**: Notebook Jupyter com o processo de análise, incluindo importação de dados, limpeza, visualizações e exploração estatística.

## Conteúdo da Análise

### 1. Importação de Bibliotecas

As seguintes bibliotecas foram usadas para a análise e visualização de dados:
- `pandas`: Manipulação e análise de dados.
- `matplotlib.pyplot` e `seaborn`: Visualização de dados.
- `plotly.graph_objects` e `plotly.subplots`: Visualização interativa.

### 2. Descrição das Colunas

Cada coluna do dataset representa uma métrica específica da produção têxtil. Aqui estão as principais colunas:
- **ID**: Identificação única da ordem de produção.
- **Month**: Mês de registro da produção.
- **Construction**: Detalhes sobre a construção do tecido.
- **Req_Finish_Fabrics**: Quantidade necessária de tecido acabado.
- **Fabric_Allowance**: Margem de tecido extra permitida.
- **Rec_Beam_length(yds)** e **Req_beam_length(yds)**: Comprimento do feixe de tecido (recomendado e necessário).
- **assump_crimp%** e **act_crimp%**: Ondulação de fios (assumida e real).
- **Rej_and_cut_Piece**: Peças rejeitadas ou cortadas.
- **warp_count** e **weft_count**: Contagem de fios longitudinais e transversais.
- **epi** e **ppi**: Densidade de fios longitudinais e transversais.

### 3. Limpeza de Dados

Durante a análise, os seguintes passos foram aplicados:
- Conversão de colunas para tipos adequados.
- Verificação e preenchimento de valores nulos. Valores nulos em colunas como `Previous_pdn` e `Total_pdn_m/c` foram preenchidos com 0, considerando os contextos específicos.

### 4. Análise Estatística

Estatísticas descritivas foram geradas para colunas numéricas, analisando média, desvio padrão, mínimo e máximo, entre outros parâmetros.

### 5. Visualizações

A análise contém diversas visualizações que auxiliam na compreensão dos dados, tais como:

- **Desperdício Total e por Mês**: Um gráfico de barras que mostra o desperdício ao longo do tempo, indicando variações mensais.
- **Desperdício Médio por Trimestre**: Análise de desperdício médio por trimestre.
- **Percentual de Desperdício por Ordem**: Percentual de desperdício por cada ordem de produção.
- **Razão de Desperdício com Tecido Requerido**: Gráfico de dispersão que explora a relação entre a quantidade de tecido requerido e o desperdício.
- **Desperdício Médio por Tipo de Construção**: Análise do desperdício médio por especificação de construção.
- **Desperdício por Tipo de Fio**: Um heatmap que mostra a relação entre o desperdício e as contagens de urdidura e trama.
- **Correlação entre Desperdício e Densidade do Tecido**: Gráficos mostrando a correlação entre desperdício e densidades `epi` e `ppi`.
- **Impacto do Fabric Allowance no Desperdício**: Gráfico de barras para o desperdício médio em diferentes faixas de tolerância de tecido.
- **Desperdício por Tipo de Ordem de Produção**: Análise do desperdício médio por padrão de ID da ordem de produção.

### 6. Insights da Análise

Os resultados da análise fornecem insights sobre fatores que influenciam o desperdício de tecido, como:
- Mês e trimestre em que há maior desperdício.
- Efeito do tipo de construção e contagem de fios.
- Impacto de variáveis como `Fabric_Allowance` e diferença de crimpagem (`act_crimp%` vs. `assump_crimp%`).

## Como Executar a Análise

1. Clone este repositório:
   ```bash
   git clone https://github.com/seu-usuario/nome-do-repositorio.git
   ```

2. Instale as dependências:
   ```bash
   pip install pandas matplotlib seaborn plotly
   ```

3. Abra o notebook `bangladesh.ipynb` e execute as células para gerar as visualizações e análises descritas.

## Conclusão

Esta análise fornece uma visão abrangente dos fatores que afetam o desperdício de tecido, permitindo identificar possíveis áreas de otimização na produção. b,bjlin

