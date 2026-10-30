# mini_projeto
Mini-Projeto Avaliativo — Análise de Dados com Python

Objetivo
Realizar uma análise exploratória de uma base de compras no varejo, identificando inconsistências, padronizando dados e calculando estatísticas descritivas com Python e Pandas.
Base de dados
Fonte: Base Varejo — Kaggle.

A base original possui 830.000 registros e 10 colunas, com informações sobre datas de compras, clientes e produtos. O arquivo utiliza ; como separador.
Tecnologias utilizadas

- Python
- Pandas
- VS Code (ou outro ambiente Python)
  
Etapas realizadas

1. Importação: leitura do CSV e identificação dos tipos de dados.
2. Transformação: padronização dos textos, verificação das colunas numéricas e conversão de DATA para datetime.
3. Limpeza: tratamento de #N/D em nomes e categorias, identificação de linhas idênticas e criação de uma base tratada.
4. Estatística descritiva: medidas do número de filhos considerando clientes únicos, além de agrupamentos por gênero e categoria.
5. Relatório: impressão de contadores no terminal e exportação de df_limpo.csv.
   
Como executar

1. Baixe a base no Kaggle e coloque o CSV na mesma pasta de mini_projeto.ipynb
2. Verifique se o arquivo se chama Base Varejo.csv ou ajuste o nome no código.
3. Instale a biblioteca: pip install pandas.
4. Execute o mini_projeto.ipynb
5. Consulte o relatório e o arquivo df_limpo.csv gerado.
   
Resultados:

Indicador	Resultado
Registros originais	830.000
Registros após remoção de linhas idênticas	733.447
Linhas idênticas identificadas	96.553
Registros com categoria desconhecida no original	3.650
Compras distintas	18.471
Clientes únicos	1.000
Média de filhos por cliente	1,14
Mediana e moda do número de filhos	0
Datas inválidas	0


Principais insights
1. Perfil familiar: 527 dos 1.000 clientes (52,7%) não possuem filhos registrados.
2. Número de filhos: a média é de 1,14 e o máximo é de quatro filhos por cliente.
3. Compras por gênero: foram registradas 9.615 compras distintas associadas a clientes do gênero feminino e 8.856 do masculino.
4. Categorias de produtos: ALIMENTOS é a categoria com mais linhas na base tratada (384.197), seguida por HIGIENE e LIMPEZA.
5. Qualidade dos dados: havia 3.650 registros com categoria e nome de produto desconhecidos e 96.553 linhas integralmente repetidas.
   
Reflexão teórica: ETL e qualidade dos dados

O processo de ETL envolve extração, transformação e carga de dados. Neste projeto, a extração ocorreu com pd.read_csv(), a transformação incluiu padronização de textos, conversão de datas e tratamento de campos ausentes, e a carga foi representada pela exportação do CSV tratado com to_csv().

A qualidade dos dados influencia a confiabilidade dos resultados. Valores ausentes e formatos inconsistentes podem dificultar filtros, agrupamentos e cálculos. A limpeza deve preservar o significado original das informações e seguir regras de negócio justificadas.

Limitação importante: as 96.553 linhas idênticas foram removidas como exercício didático. Em dados reais, podem representar múltiplas unidades do mesmo produto em uma compra. Portanto, essa exclusão deve ser validada antes de gerar indicadores de volume de produtos vendidos. A base também não contém preços nem quantidades explícitas, impossibilitando análises confiáveis de faturamento.

Arquivos do projeto

- mini_projeto.ipynb — script da análise.
- df_limpo.csv — base tratada produzida pelo script.
- README.md — documentação e reflexões.
