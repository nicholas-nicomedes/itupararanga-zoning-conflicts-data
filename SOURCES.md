# Data sources and provenance

This document describes the main source materials used to create the geospatial datasets distributed in this repository.

The definitive methodological description is provided in the associated peer-reviewed article:

Gonçalves, B., Nicomedes, N. P., Nery, L. M., Oliveira, R. F., & Silva, D. C. C. (2026). Conflitos normativos entre Planos Diretores Municipais e Plano de Manejo de uma unidade de conservação: uma análise na Área de Proteção Ambiental de Itupararanga. *Finisterra*, 61(131), e42541.

DOI: https://doi.org/10.18055/Finis42541

---

## 1. Itupararanga Environmental Protection Area

The spatial boundary and Management Plan information used in the study are associated with the Fundação Florestal do Estado de São Paulo.

### Management Plan

Fundação Florestal. (2010). *Plano de Manejo – APA Itupararanga*.

Source:
https://fflorestal.sp.gov.br/planos-de-manejo/planos-de-manejo-planos-concluidos/plano-de-manejo-apa-itupararanga/

The `PM` dataset represents the environmental zoning considered in the associated study.

The `APAitupararanga` dataset represents the spatial boundary of the protected area used for the analyses.

---

## 2. Municipal Master Plans

The `PDM` dataset was constructed from zoning information contained in the Municipal Master Plans and associated normative documents considered in the study.

Only portions located within the Itupararanga APA were retained in the final analytical dataset.

### Alumínio

Municipality of Alumínio. (2021). Lei nº 2.168, de 8 de setembro de 2021. Altera dispositivos da Lei nº 2.010, de 21 de setembro de 2018, que institui o Plano Diretor Participativo de Alumínio.

Source:
https://www.legislacaodigital.com.br/Aluminio-SP/LeisOrdinarias/2168

### Cotia

Municipality of Cotia. (2024). Lei Complementar nº 380, de 20 de maio de 2024. Dispõe sobre o Plano Diretor de Desenvolvimento Urbano, Econômico e Social do Município de Cotia.

Source:
https://leismunicipais.com.br/

### Ibiúna

Municipality of Ibiúna. (2016). Lei nº 2.129, de 7 de outubro de 2016. Institui a revisão e os subsídios para o Plano Diretor da Estância Turística de Ibiúna e dá outras providências.

Source:
https://www.ibiuna.sp.leg.br/ouvidoria/20171006090932

### Mairinque

Municipality of Mairinque. (2024). Lei nº 4.246, de 2024. Altera e acrescenta dispositivos da Lei nº 3.727, de 11 de outubro de 2019, Plano Diretor do Município de Mairinque, e das Leis nº 3.813/2020 e nº 3.790/2020.

Source:
https://leismunicipais.com.br/

### Piedade

Municipality of Piedade. (2021). Lei nº 4.716, de 4 de novembro de 2021. Dispõe sobre a revisão do Plano Diretor do Município de Piedade e dá outras providências.

Source:
https://sapl.piedade.sp.leg.br/ta/517/text

### São Roque

Municipality of São Roque. (2006). Lei Complementar nº 39, de 8 de novembro de 2006. Institui o Plano Diretor do Município da Estância Turística de São Roque e dá outras providências.

Source:
https://leismunicipais.com.br/

### Vargem Grande Paulista

Municipality of Vargem Grande Paulista. (2013). Lei Complementar nº 67, de 16 de dezembro de 2013. Dispõe sobre a revisão do Plano Diretor do Município de Vargem Grande Paulista.

Source:
https://leismunicipais.com.br/

### Votorantim

Municipality of Votorantim. (2015). Lei Complementar nº 4, de 17 de dezembro de 2015. Dispõe sobre o Plano Diretor de Desenvolvimento Integrado do Município de Votorantim e dá outras providências.

Source:
https://sapl.votorantim.sp.leg.br/norma/3179

---

## 3. Land use and land cover

Land-use and land-cover information used in the analysis was derived from:

MapBiomas. (2023). *Collection 9 of the historical series of land use and land cover in Brazil*.

Source:
https://mapbiomas.org/colecoes-mapbiomas

Reference year used in the associated study: **2023**.

Spatial resolution reported in the study: **30 m**.

The `UCT` and `ClassAdequacaoUCT` datasets contain information associated with this stage of the analysis.

---

## 4. Research-derived datasets

The following layers are analytical products created as part of the methodology of the associated study:

### ConflPMPDM

Derived from the spatial overlay and normative comparison between the Management Plan zoning (`PM`) and Municipal Master Plan zoning (`PDM`).

The compatibility assessment distinguishes:

- Adequate;
- Conditionally adequate (`Adequado com ressalvas`);
- Inadequate.

### ClassAdequacaoUCT

Derived from the analysis of land-use and land-cover classes occurring in areas identified as inadequate or conditionally adequate in the PM–PDM comparison.

These classifications represent research products and must not be interpreted as official governmental zoning classifications.

---

## 5. Processing and standardization

Source spatial information was obtained in different formats and coordinate reference systems.

Where the original zoning information was not available as a geospatial vector dataset, maps were georeferenced using control points and manually vectorized through on-screen digitization.

Spatial processing was performed using ArcGIS 10.8.

The analytical layers were standardized using SIRGAS 2000 / UTM zone 23S.

Topological validation and manual editing were performed to correct overlaps, gaps, and inconsistent geometries.

Municipal zoning layers were subsequently clipped to the Itupararanga APA boundary.

Users should consult the associated article for the complete methodological procedure.
