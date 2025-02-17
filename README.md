# GREENFLOW - Análise de sustentabilidade para PMEs

Este projeto visa analisar dados de sustentabilidade de pequenas e médias empresas (PMEs) para fornecer insights valiosos sobre seus consumos de energia, água e emissões de CO2. Através da análise exploratória e visualização de dados, o projeto busca identificar padrões, empresas com consumo excessivo e agrupar empresas com perfis de consumo semelhantes.

Este ficheiro README oferece uma visão geral do projeto, da sua estrutura, de como executá-lo e das possíveis análises que podem ser realizadas com os dados.

### Estrutura do projeto

A estrutura de pastas do projeto é a seguinte:

dataops_greenflow/
├── data/
│   └── dados_sensores_5000.parquet
├── notebooks/
│   └── challenge1.ipynb
├── .gitignore
├── README.md
└── LICENSE

*   **`data/`**: Contém o ficheiro Parquet `dados_sensores_5000.parquet` com os dados das empresas.
*   **`notebooks/`**: Contém o notebook Jupyter `challenge1.ipynb` com o código da análise.
*   **`.gitignore`**: Ficheiro com instruções para o Git ignorar ficheiros específicos (e.g., ficheiros temporários).
*   **`README.md`**: Este ficheiro, com a descrição do projeto.
*   **`LICENSE`**: Ficheiro com a licença do projeto (e.g., MIT).

### Como executar o projeto (Google Colab)

1.  **Abra o notebook no Google Colab:**
    No Google Colab, abra o ficheiro `challenge1.ipynb` que está na pasta `notebooks/`.

2.  **Execute as células do notebook:**
    O notebook contém comentários e explicações sobre cada passo da análise. Deve no entanto carregar o ficheiro `dados_sensores_5000.parquet` dentro do Google Colab.

### Análise dos Dados

O ficheiro Parquet `dados_sensores_5000.parquet` contém dados de 5000 empresas. Cada linha representa uma empresa e contém as seguintes colunas:

*   **`id_empresa`**: Identificador único da empresa.
*   **`setor`**: Setor de atividade da empresa.
*   **`energia_kwh`**: Consumo de energia em kWh.
*   **`agua_m3`**: Consumo de água em m³.
*   **`co2_emissoes`**: Emissões de CO2.

### Possíveis Análises

Com base nos dados disponíveis, é possível realizar diversas análises, como:

*   **Análise exploratória inicial:**
    *   Visualização das primeiras linhas do dataframe.
    *   Informações gerais sobre os dados (tipos de dados, valores ausentes).
    *   Estatísticas descritivas (média, desvio padrão, etc.).
*   **Análise de consumo por setor:**
    *   Agrupamento dos dados por setor.
    *   Cálculo do consumo total e médio de energia, água e emissões de CO2 por setor.
    *   Comparação do consumo entre os setores.
*   **Identificação de empresas com consumo excessivo:**
    *   Definição de critérios para identificar empresas com consumo excessivo (e.g., empresas com consumo acima de um determinado limiar ou empresas com consumo muito acima da média do setor).
    *   Listagem das empresas com consumo excessivo.
*   **Visualização de dados:**
    *   Criação de gráficos para visualizar o consumo de recursos por setor (e.g., gráficos de barras, gráficos de pizza).
    *   Criação de gráficos para comparar o consumo entre setores (e.g., boxplots, histogramas).
    *   Visualização da distribuição do consumo de recursos (e.g., histogramas, KDE plots).
    *   Visualização da matriz de correlação entre as variáveis.
*   **Identificação de outliers:**
    *   Utilização de métodos estatísticos (e.g., z-score, IQR) para identificar empresas com consumo fora do padrão.
    *   Visualização dos outliers.
*   **Agrupamento de empresas:**
    *   Utilização de algoritmos de clustering (e.g., K-Means) para agrupar empresas com perfis de consumo semelhantes.
    *   Análise das características de cada cluster.
*   **Modelagem preditiva:**
    *   Utilização de modelos de regressão linear para prever o consumo de recursos com base em outras variáveis (poderia ser bastante útil caso tivesse algum tipo de dados temporais).

## Licença

Este projeto está licenciado sob a Licença MIT - veja o ficheiro (LICENSE) para detalhes.