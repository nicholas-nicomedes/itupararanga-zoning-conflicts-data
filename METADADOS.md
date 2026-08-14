# Metadados do conjunto de dados geoespaciais da APA de Itupararanga

## Conflitos normativos entre Planos Diretores Municipais e o Plano de Manejo da Área de Proteção Ambiental de Itupararanga

**Versão do conjunto de dados:** 1.0.0  
**Tipo de recurso:** conjunto de dados geoespaciais  
**Idioma dos metadados:** português  
**Área de estudo:** Área de Proteção Ambiental de Itupararanga, estado de São Paulo, Brasil  
**Sistema de referência de coordenadas:** SIRGAS 2000 / UTM zona 23S — EPSG:31983  
**Contato:** Nícholas de Paula Nicomedes — nicholas.nicomedes@unesp.br  
**Data de atualização dos metadados:** 2026-08-14

> **Nota científica e jurídica:** as camadas disponibilizadas são bases de referência ou produtos geoespaciais preparados para a pesquisa citada neste documento. Elas não devem ser interpretadas como bases cadastrais, juridicamente vinculantes ou necessariamente representativas da legislação atualmente vigente. Para aplicações legais, regulatórias, administrativas, de licenciamento ou de planejamento territorial oficial, devem ser consultados os documentos normativos originais e os órgãos públicos responsáveis.

## 1. Descrição geral

Este conjunto reúne os dados geoespaciais utilizados e produzidos no estudo:

> Gonçalves, B., de Paula Nicomedes, N., Moreira Nery, L., Fabricio de Oliveira, R., & Collins Cunha e Silva, D. (2026). Conflitos normativos entre Planos Diretores Municipais e Plano de Manejo de uma unidade de conservação: uma análise na Área de Proteção Ambiental de Itupararanga. *Finisterra*, 61(131), e42541. https://doi.org/10.18055/Finis42541

O estudo comparou o zoneamento do Plano de Manejo (PM) da APA de Itupararanga com os zoneamentos dos Planos Diretores Municipais (PDMs) dos municípios parcialmente inseridos na unidade de conservação. A comparação espacial e normativa permitiu identificar combinações adequadas, adequadas com ressalvas e inadequadas entre os instrumentos de planejamento.

As áreas classificadas como inadequadas ou adequadas com ressalvas foram posteriormente avaliadas com dados de uso e cobertura da terra do MapBiomas Brasil, Coleção 9, ano de referência 2023 e resolução espacial nominal de 30 m. O conjunto permite consultar as bases utilizadas, reproduzir partes da análise espacial e examinar a distribuição territorial das classes de adequação.

### 1.1. Camadas disponíveis

| Camada | Natureza | Conteúdo |
|---|---|---|
| `APAitupararanga` | Camada de referência | Limite da APA utilizado para delimitar a área de estudo |
| `PDM` | Dado normativo espacializado | Zoneamentos dos Planos Diretores Municipais recortados pelo limite da APA |
| `PM` | Dado normativo espacializado | Zoneamento estabelecido pelo Plano de Manejo da APA |
| `ConflPMPDM` | Produto analítico derivado | Compatibilidade normativa entre as zonas do PM e dos PDMs |
| `UCT` | Produto derivado do MapBiomas | Classes de uso e cobertura da terra nas áreas selecionadas para análise |
| `ClassAdequacaoUCT` | Produto analítico derivado | Adequação do uso e cobertura da terra em relação às categorias dos instrumentos de planejamento |

As camadas `ConflPMPDM` e `ClassAdequacaoUCT` constituem resultados analíticos da pesquisa. Suas classificações não foram emitidas por órgãos governamentais.

## 2. Cobertura espacial e temporal

### 2.1. Cobertura espacial

A área de estudo corresponde à APA de Itupararanga, localizada no estado de São Paulo e abrangendo parcelas dos seguintes municípios:

- Alumínio;
- Cotia;
- Ibiúna;
- Mairinque;
- Piedade;
- São Roque;
- Vargem Grande Paulista;
- Votorantim.

As camadas analíticas foram processadas em **SIRGAS 2000 / UTM zona 23S (EPSG:31983)**. As unidades dos campos de área estão indicadas individualmente no dicionário de dados.

### 2.2. Cobertura temporal

A camada `PDM` representa as versões dos instrumentos municipais consideradas no estudo:

| Município | Ano do instrumento considerado |
|---|---:|
| Alumínio | 2021 |
| Cotia | 2024 |
| Ibiúna | 2016 |
| Mairinque | 2024 |
| Piedade | 2021 |
| São Roque | 2006 |
| Vargem Grande Paulista | 2013 |
| Votorantim | 2015 |

O zoneamento do Plano de Manejo corresponde ao documento publicado pela Fundação Florestal em 2010. Os dados de uso e cobertura da terra correspondem ao ano de 2023 da Coleção 9 do MapBiomas Brasil.

Essas referências temporais devem ser consideradas na interpretação dos dados. O conjunto não incorpora automaticamente revisões normativas ou alterações territoriais posteriores.

## 3. Proveniência e processamento

Os dados vetoriais do zoneamento ambiental do Plano de Manejo foram obtidos junto à Fundação Florestal. As informações relativas aos Planos Diretores Municipais foram coletadas em plataformas institucionais das prefeituras e em outros meios oficiais de divulgação utilizados no estudo.

As bases cartográficas estavam disponíveis em diferentes formatos e sistemas de referência. Por essa razão, os dados foram convertidos e padronizados. Documentos não geoespaciais foram georreferenciados por pontos de controle e vetorizados manualmente por digitalização em tela no ArcGIS 10.8. As camadas foram padronizadas para SIRGAS 2000 / UTM zona 23S, submetidas a validação topológica e editadas para correção de sobreposições, lacunas e geometrias inconsistentes. Os zoneamentos municipais foram recortados pelo limite adotado da APA.

A camada `ConflPMPDM` foi produzida pela sobreposição espacial das camadas `PM` e `PDM`, seguida da avaliação da compatibilidade normativa entre as categorias dos dois instrumentos. As áreas classificadas como inadequadas ou adequadas com ressalvas foram utilizadas como recorte para a análise de uso e cobertura da terra.

A informação de uso e cobertura da terra foi derivada do MapBiomas Brasil, Coleção 9, ano de referência 2023. A camada `ClassAdequacaoUCT` foi obtida pela integração das categorias do PM, dos PDMs e das classes de uso e cobertura da terra.

## 4. Formatos e organização dos dados

As seis camadas são disponibilizadas em duas formas:

1. **ESRI Shapefile:** cada camada é fornecida separadamente em um arquivo ZIP contendo seus componentes;
2. **GeoPackage:** as seis camadas são reunidas em um único arquivo `.gpkg`.

O GeoPackage e os Shapefiles representam a mesma versão científica do conjunto. O GeoPackage é recomendado para integração em fluxos de trabalho atuais por armazenar todas as camadas em um único arquivo e preservar melhor nomes de campos, codificação de caracteres e tipos de dados.

Cada pacote Shapefile deve ser mantido completo. Os componentes `.shp`, `.shx`, `.dbf` e `.prj` são necessários para a leitura adequada da geometria, dos atributos e do sistema de referência; o arquivo `.cpg`, quando presente, informa a codificação dos caracteres.

Identificadores internos como `FID`, `OBJECTID` ou equivalentes podem ser criados automaticamente pelo software de geoprocessamento ao abrir, copiar ou exportar uma camada. Esses identificadores não integram o dicionário temático e não devem ser utilizados como chaves persistentes entre formatos.

## 5. Dicionário de dados

### 5.1. Camada `APAitupararanga`

**Descrição:** limite espacial da Área de Proteção Ambiental de Itupararanga utilizado para delimitar a área de estudo e recortar as demais bases.  
**Geometria:** polígono.

| Campo | Definição | Uso recomendado |
|---|---|---|
| `Id` | Identificador local da feição correspondente ao limite da APA. | Identificação técnica da feição; não interpretar como código oficial persistente. |

### 5.2. Camada `PDM`

**Descrição:** zoneamentos estabelecidos pelos Planos Diretores Municipais dos municípios parcialmente inseridos na APA. As geometrias correspondem às parcelas situadas no interior da unidade de conservação.  
**Geometria:** polígono.

| Campo | Definição | Uso recomendado |
|---|---|---|
| `DESCRICAO` | Denominação original ou descrição da zona no instrumento municipal de origem. | Consultar quando for necessário preservar a terminologia específica do PDM. |
| `TIPO` | Categoria padronizada utilizada para harmonizar os diferentes zoneamentos municipais. | Utilizar nas comparações entre municípios e entre instrumentos de planejamento. |

`DESCRICAO` e `TIPO` não são sinônimos. O primeiro campo preserva a nomenclatura do documento municipal; o segundo expressa a harmonização analítica realizada na pesquisa.

### 5.3. Camada `PM`

**Descrição:** zoneamento estabelecido pelo Plano de Manejo da APA de Itupararanga.  
**Geometria:** polígono.

| Campo | Definição | Uso recomendado |
|---|---|---|
| `Name` | Nome ou sigla da zona definida no Plano de Manejo. | Campo temático principal da camada. |

As categorias gerais do Plano de Manejo apresentadas no estudo são:

| Sigla | Denominação |
|---|---|
| `ZCRH` | Zona de Conservação de Recursos Hídricos |
| `ZCB` | Zona de Conservação da Biodiversidade |
| `ZOR` | Zona de Ocupação Rural |
| `ZOC` | Zona de Ocupação Consolidada |
| `ZOD` | Zona de Ocupação Diversificada |

### 5.4. Camada `ConflPMPDM`

**Descrição:** produto analítico resultante da sobreposição espacial e da comparação normativa entre o zoneamento do Plano de Manejo e os zoneamentos dos Planos Diretores Municipais.  
**Geometria:** polígono.

| Campo | Definição | Uso recomendado |
|---|---|---|
| `Name` | Nome ou sigla da zona do Plano de Manejo. | Identificação da categoria do PM associada à geometria. |
| `DESCRICAO` | Denominação original da zona do Plano Diretor Municipal. | Consulta da terminologia do instrumento municipal de origem. |
| `TIPO` | Categoria municipal padronizada para comparação entre instrumentos. | Comparação temática entre PM e PDM. |
| `Analise` | Resultado da avaliação de compatibilidade normativa entre a zona do PM e a zona do PDM. | Campo analítico principal da camada. |

#### Domínio do campo `Analise`

| Valor | Interpretação |
|---|---|
| `Adequado` | Os usos previstos pelos dois instrumentos são convergentes. |
| `Adequado com ressalvas` | Existe compatibilidade formal, mas sua sustentabilidade depende de condicionantes e controle específico do uso da terra. |
| `Inadequado` | Há conflito entre os usos permitidos ou as restrições estabelecidas pelos instrumentos. |

A classificação registrada em `Analise` resulta da metodologia da pesquisa e não constitui decisão administrativa ou classificação oficial.

### 5.5. Camada `UCT`

**Descrição:** síntese das classes de uso e cobertura da terra presentes nas áreas classificadas como inadequadas ou adequadas com ressalvas na comparação entre PM e PDM.  
**Origem temática:** MapBiomas Brasil, Coleção 9, ano de referência 2023.  
**Resolução espacial da fonte:** 30 m.  
**Geometria:** polígono ou polígono multipartes resultante da agregação das geometrias de cada classe.

| Campo | Tipo/unidade | Definição | Uso recomendado |
|---|---|---|---|
| `gridcode` | Número inteiro | Código da classe de uso e cobertura da terra na legenda do MapBiomas. | Relacionar a classe à legenda da Coleção 9. |
| `Classes` | Texto | Denominação da classe de uso e cobertura da terra. | Campo temático principal. |
| `Area_m2_` | Metros quadrados | Área total ocupada pela classe no recorte analisado. | Análises quantitativas de área absoluta. |
| `Porc_area` | Percentual | Participação da classe em relação à área total representada na camada. | Comparações proporcionais entre classes. |

Os valores de `gridcode` e `Classes` devem ser interpretados segundo a legenda oficial da Coleção 9 do MapBiomas Brasil.

### 5.6. Camada `ClassAdequacaoUCT`

**Descrição:** produto analítico que relaciona as categorias do Plano de Manejo, dos Planos Diretores Municipais e do uso e cobertura da terra, classificando a adequação observada em cada unidade espacial.  
**Geometria:** polígono.  
**Número de feições na versão 1.0.0:** 264.

| Campo | Tipo/unidade | Definição | Uso recomendado |
|---|---|---|---|
| `PM` | Texto categórico | Zona do Plano de Manejo associada à unidade espacial. | Identificar a diretriz de zoneamento ambiental considerada na análise. |
| `UCT` | Texto categórico | Classe de uso e cobertura da terra observada, derivada do MapBiomas Brasil. | Identificar o uso ou a cobertura existente na unidade espacial. |
| `PD` | Texto categórico | Categoria do Plano Diretor Municipal associada à unidade espacial. | Identificar a diretriz municipal considerada na análise. |
| `Adequação` | Texto categórico | Classificação da compatibilidade entre o uso e cobertura da terra observado e as categorias dos instrumentos de planejamento. | Campo analítico principal da camada. |
| `area_km2` | Quilômetros quadrados | Área da unidade espacial representada pelo registro. | Quantificação e agregação das áreas por zona, classe de UCT ou categoria de adequação. |

#### Domínio do campo `Adequação`

| Valor | Interpretação |
|---|---|
| `Adequado` | O uso e cobertura da terra observado é compatível com as categorias dos instrumentos avaliados. |
| `Adequado com ressalvas` | A compatibilidade depende de condicionantes, controle ou manejo específico. |
| `Inadequado` | O uso e cobertura da terra observado é incompatível com pelo menos uma das diretrizes consideradas. |

Os campos `PM`, `UCT` e `PD` descrevem a combinação temática associada a cada geometria. Portanto, a repetição de valores entre registros é esperada e decorre da fragmentação espacial das diferentes combinações.

## 6. Qualidade, consistência e limitações

As camadas foram harmonizadas no mesmo sistema de referência, submetidas a procedimentos de correção geométrica e preparadas com atributos temáticos voltados à interpretação e à reutilização. Os Shapefiles e o GeoPackage correspondem à mesma versão do conteúdo científico.

As seguintes limitações devem ser consideradas:

1. Parte das bases foi reconstruída por georreferenciamento e vetorização manual de documentos não geoespaciais. A precisão espacial depende da qualidade cartográfica das fontes e dos pontos de controle utilizados.
2. A padronização das categorias municipais e as classificações de compatibilidade são interpretações metodológicas produzidas no estudo.
3. Os PDMs possuem diferentes datas de referência e podem ter sido alterados após os anos indicados neste documento.
4. O Plano de Manejo utilizado corresponde à versão publicada em 2010.
5. Os dados de uso e cobertura da terra representam o ano de 2023 e não devem ser extrapolados automaticamente para outros períodos.
6. A resolução espacial de 30 m do MapBiomas limita a representação de elementos menores do que o pixel e de mosaicos espaciais complexos.
7. As áreas calculadas podem apresentar pequenas diferenças por arredondamento, conversão de formato ou método de cálculo geométrico empregado pelo software.
8. A presença de uma classificação `Adequado` indica compatibilidade segundo os critérios da pesquisa; não comprova, isoladamente, regularidade fundiária, ambiental, urbanística ou administrativa.
9. As classificações `Inadequado` e `Adequado com ressalvas` constituem resultados científicos e não substituem análise jurídica ou manifestação dos órgãos competentes.

## 7. Condições de reutilização

As camadas reúnem informações de origem governamental, dados derivados de terceiros e produtos analíticos desenvolvidos pelos autores. As condições de reutilização podem variar conforme a origem do conteúdo.

Os dados derivados do MapBiomas devem ser reutilizados com a atribuição exigida pelo projeto. Para as demais camadas, devem ser observadas as condições indicadas no registro do Zenodo e na documentação de direitos que acompanha o conjunto.

A redistribuição ou transformação dos dados não elimina a necessidade de citar as fontes originais, o conjunto de dados e o artigo associado.

## 8. Citação

Ao utilizar o conjunto em trabalho científico, técnico ou cartográfico, recomenda-se citar:

1. o registro do conjunto de dados no Zenodo, utilizando a referência e o DOI exibidos na página do depósito;
2. o artigo científico associado;
3. o MapBiomas Brasil quando forem utilizados os campos ou produtos derivados de uso e cobertura da terra.

### Artigo associado

> Gonçalves, B., de Paula Nicomedes, N., Moreira Nery, L., Fabricio de Oliveira, R., & Collins Cunha e Silva, D. (2026). Conflitos normativos entre Planos Diretores Municipais e Plano de Manejo de uma unidade de conservação: uma análise na Área de Proteção Ambiental de Itupararanga. *Finisterra*, 61(131), e42541. https://doi.org/10.18055/Finis42541

## 9. Referências e fontes principais

- Fundação Florestal. (2010). *Plano de Manejo da Área de Proteção Ambiental de Itupararanga*.
- Gonçalves, B., de Paula Nicomedes, N., Moreira Nery, L., Fabricio de Oliveira, R., & Collins Cunha e Silva, D. (2026). Conflitos normativos entre Planos Diretores Municipais e Plano de Manejo de uma unidade de conservação: uma análise na Área de Proteção Ambiental de Itupararanga. *Finisterra*, 61(131), e42541. https://doi.org/10.18055/Finis42541
- MapBiomas Brasil. (2024). *Coleção 9 da Série Anual de Mapas de Cobertura e Uso da Terra do Brasil: 1985–2023*. https://brasil.mapbiomas.org/colecoes-mapbiomas/
- MapBiomas Brasil. *Códigos de legenda*. https://brasil.mapbiomas.org/downloads/codigos-de-legenda/
- Planos Diretores Municipais de Alumínio (2021), Cotia (2024), Ibiúna (2016), Mairinque (2024), Piedade (2021), São Roque (2006), Vargem Grande Paulista (2013) e Votorantim (2015), conforme as fontes institucionais utilizadas no estudo.
