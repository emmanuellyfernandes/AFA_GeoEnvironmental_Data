# AFA_GeoEnvironmental_Data
Este repositório contém códigos para análise e visualização de dados ambientais da Academia da Força Aérea (AFA) referentes ao período de 2019 a 2024. Inclui um script para geração de gráficos do Índice de Vegetação por Diferença Normalizada (NDVI) e outro para análise dos dados de precipitação mensal. 

##Código 1 – Variação Sazonal do NDVI (2019–2024)
#Nome do arquivo: AFA_NDVI_VeraoInverno.ipynb

# Objetivo

Analisar a variação sazonal da vegetação por meio do índice NDVI (Normalized Difference Vegetation Index), comparando os períodos de verão e inverno na área da AFA, no período de 2019 a 2024.

# Fonte dos Dados

-Imagens de satélite: Sentinel-2 Surface Reflectance (Coleção COPERNICUS/S2_SR), via Google Earth Engine (GEE)

-Área de estudo: shapefile local da AFA

#Etapas Principais

- Importação das bibliotecas necessárias (geemap, geopandas, etc.);

- Carregamento e conversão da área de estudo para o formato GeoJSON;

- Definição das datas para os verões e invernos entre 2019 e 2024;

- Filtragem das imagens Sentinel-2 por data e cobertura de nuvens, e cálculo do NDVI médio por estação;

- Armazenamento dos dados em um DataFrame e criação de gráficos comparativos.

# Resultado Esperado

Gráfico de linha exibindo a variação dos valores médios de NDVI entre verão e inverno ao longo dos anos, evidenciando padrões sazonais e mudanças na cobertura vegetal.



## Código 2 – Análise da Precipitação Mensal (2019–2024)
# Nome do arquivo: AFA_Precipitação.ipynb

# Objetivo

Extrair e analisar dados de precipitação mensal entre 2019 e 2024 para a área da AFA, com base na coleção CHIRPS do Google Earth Engine (GEE), utilizando como referência o centróide da região de interesse (AFA).

# Fonte dos Dados

- Precipitação: Coleção UCSB-CHG/CHIRPS/DAILY (GEE)

- Área de estudo: shapefile da AFA, reprojetado para EPSG:4326


# Etapas Principais

- Instalação e importação das bibliotecas;

- Autenticação e inicialização do GEE;

- Leitura e reprojeção do shapefile;

- Cálculo do centróide da área;

- Definição do intervalo temporal (jan/2019 a dez/2024);

- Extração mensal da precipitação média no ponto de interesse;

- Armazenamento dos resultados em DataFrame e visualização em gráfico de linha.

# Resultado Esperado

Gráfico de linha representando a precipitação acumulada mensalmente no ponto central da área de estudo, permitindo identificar padrões climáticos, sazonalidade ou anomalias.



## Integração entre os Códigos

A análise combinada dos dois scripts proporciona uma visão abrangente da interação entre clima e vegetação na AFA:

O Código 1 revela como a vegetação responde sazonalmente, com base nos valores de NDVI.

O Código 2 fornece o contexto climático, mostrando os padrões de precipitação que podem influenciar diretamente o vigor vegetativo.

Essa abordagem integrada possibilita avaliar, por exemplo, se períodos de menor precipitação estão correlacionados com quedas no NDVI, indicando possíveis estresses ambientais. Assim, os dois conjuntos de dados se complementam e fortalecem a análise ambiental da área.
