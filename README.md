# Geospatial dataset of normative zoning conflicts in the Itupararanga Environmental Protection Area, Brazil

This repository provides the geospatial datasets used and generated in the study:

> Gonçalves, B., Nicomedes, N. P., Nery, L. M., Oliveira, R. F., & Silva, D. C. C. (2026). Conflitos normativos entre Planos Diretores Municipais e Plano de Manejo de uma unidade de conservação: uma análise na Área de Proteção Ambiental de Itupararanga. *Finisterra*, 61(131), e42541. https://doi.org/10.18055/Finis42541

Dataset DOI: https://doi.org/10.5281/zenodo.21921498
v1.0.0

## Overview

The dataset supports the spatial analysis of normative compatibility between the Management Plan (PM) of the Itupararanga Environmental Protection Area (APA), São Paulo State, Brazil, and the Municipal Master Plans (PDMs) of the municipalities located within the protected area.

The repository also provides research-derived spatial products resulting from the comparison between these zoning instruments and from the assessment of land use and land cover (UCT) in areas identified as inadequate or conditionally adequate.

The dataset was prepared to improve transparency, reproducibility, reuse, and access to the geospatial information underlying the associated peer-reviewed study.

## Study area

The Itupararanga Environmental Protection Area encompasses portions of eight municipalities in the state of São Paulo, Brazil:

- Alumínio
- Cotia
- Ibiúna
- Mairinque
- Piedade
- São Roque
- Vargem Grande Paulista
- Votorantim

## Available datasets

| Dataset | Description |
| --- | --- |
| `APAitupararanga` | Spatial boundary of the Itupararanga Environmental Protection Area used as the study area. |
| `PDM` | Zoning derived from the Municipal Master Plans of municipalities located within the APA. Only portions located inside the APA boundary are included. |
| `PM` | Environmental zoning established by the Management Plan of the Itupararanga Environmental Protection Area. |
| `ConflPMPDM` | Research-derived spatial layer resulting from the comparison between PM and PDM zoning, indicating their normative compatibility. |
| `UCT` | Land-use and land-cover classes occurring in areas classified as inadequate or conditionally adequate in the PM–PDM comparison. |
| `ClassAdequacaoUCT` | Research-derived classification describing the compatibility between observed land use/land cover and the zoning requirements evaluated in the study. |

## Data formats

The official dataset release is distributed in two formats:

### ESRI Shapefile

Each spatial layer is provided separately as a ZIP archive containing the components required for the Shapefile format.

### GeoPackage

All spatial layers are also consolidated into a single GeoPackage:

`itupararanga_zoning_conflicts_v1.0.gpkg`

The GeoPackage format is recommended for users who wish to access all layers in a single geospatial database.

## Coordinate reference system

The analytical datasets were standardized using:

**SIRGAS 2000 / UTM zone 23S — EPSG:31983**

Users should verify the coordinate reference system metadata when incorporating these datasets into other spatial analyses.

GeoJSON files stored in the `preview` directory are web-optimized representations exported in geographic coordinates for visualization on GitHub and should not be considered the primary analytical dataset.

## Temporal scope

The Municipal Master Plan zoning represented in this dataset corresponds to the normative documents considered in the associated study:

| Municipality | Reference year |
| --- | ---: |
| Alumínio | 2021 |
| Cotia | 2024 |
| Ibiúna | 2016 |
| Mairinque | 2024 |
| Piedade | 2021 |
| São Roque | 2006 |
| Vargem Grande Paulista | 2013 |
| Votorantim | 2015 |

These layers therefore represent the versions of the planning instruments examined in the study and should not be interpreted as necessarily representing the currently valid zoning regulations of each municipality.

## Methodological provenance

The environmental zoning of the Itupararanga APA Management Plan was obtained from the Fundação Florestal.

Spatial information associated with the Municipal Master Plans was obtained from official institutional sources. Because the original information was available in different digital formats and coordinate systems, spatial standardization was required.

Where zoning information was not originally available as geospatial vector data, the corresponding maps were georeferenced using control points and manually vectorized through on-screen digitization.

The spatial datasets were standardized in SIRGAS 2000 / UTM zone 23S. Topological validation and manual editing were subsequently performed to correct overlaps, gaps, and inconsistent geometries.

Municipal zoning layers were clipped to the boundary of the Itupararanga APA.

Compatibility between the Management Plan and Municipal Master Plan zoning was evaluated through spatial overlay and comparative assessment of the normative requirements associated with each zoning category.

Areas were classified as:

- Adequate;
- Conditionally adequate (`Adequado com ressalvas`);
- Inadequate.

Areas classified as inadequate or conditionally adequate were subsequently evaluated using land-use and land-cover information from MapBiomas Brazil, Collection 9, reference year 2023.

For the complete methodology and interpretation criteria, users should consult the associated peer-reviewed article.

## Data access

Stable versions of the datasets are distributed through the GitHub Releases section:

https://github.com/nicholas-nicomedes/itupararanga-zoning-conflicts-data/releases

Users conducting spatial analyses should preferably download the Shapefile or GeoPackage versions provided in a numbered release.

## Web visualization

Simplified GeoJSON versions of selected layers are available in the `preview` directory for direct visualization through GitHub.

These files are intended for visualization only. They may have simplified geometries and a different coordinate reference system from the analytical dataset.

For quantitative, cartographic, or spatial analyses, use the files distributed in the official release.

## Scientific and legal notice

These datasets are provided for scientific research, reproducibility, education, and technical analysis.

Some spatial layers were reconstructed, standardized, georeferenced, vectorized, clipped, or otherwise processed from official planning documents. Consequently, these files should not be interpreted as official, cadastral, legally authoritative, or necessarily current zoning datasets.

The layers `ConflPMPDM` and `ClassAdequacaoUCT` are research-derived analytical products generated according to the methodology and classification criteria described in the associated article. They do not constitute official classifications issued by governmental authorities.

Users requiring information for legal, regulatory, licensing, cadastral, administrative, or official territorial-planning purposes should consult the original normative documents and the responsible governmental institutions.

Users are also responsible for verifying the temporal validity of the underlying planning instruments before applying these datasets to contemporary planning or regulatory analyses.

## Data sources and licensing

Detailed information about the provenance of the source datasets and normative documents is provided in [`SOURCES.md`](SOURCES.md).

Information regarding licensing, attribution, and third-party data is provided in [`LICENSES.md`](LICENSES.md).

## Data dictionary

Descriptions of the layers, attributes, classes, and codes are provided in [`DATA_DICTIONARY.md`](DATA_DICTIONARY.md).

## Versioning

This dataset follows numbered releases.

The first public scientific release is designated:

`v1.0.0`

Corrections or modifications to the spatial data will be documented in [`CHANGELOG.md`](CHANGELOG.md) and distributed as new releases.

Users should report the dataset version when using these data in scientific or technical work.

## Citation

If these datasets are used in scientific publications, reports, theses, dissertations, technical studies, or other derived products, users are requested to cite both the dataset and the associated article.

### Associated article

Gonçalves, B., Nicomedes, N. P, Nery, L. M., Oliveira, R. F., & Silva, D. C. C. (2026). Conflitos normativos entre Planos Diretores Municipais e Plano de Manejo de uma unidade de conservação: uma análise na Área de Proteção Ambiental de Itupararanga. *Finisterra*, 61(131), e42541. https://doi.org/10.18055/Finis42541

### Dataset

The definitive dataset citation and DOI will be added after publication of version 1.0.0 in Zenodo.

## Associated study authors

- Bianca Gonçalves
- Nícholas de Paula Nicomedes
- Liliane Moreira Nery
- Rafael Fabricio de Oliveira
- Darllan Collins Cunha e Silva

## Contact

**Nícholas de Paula Nicomedes**  
Universidade Estadual Paulista (UNESP)  
Instituto de Ciência e Tecnologia, Sorocaba, Brazil  
E-mail: nicholas.nicomedes@unesp.br

## Issues and corrections

Potential errors, metadata inconsistencies, or questions regarding the dataset may be reported through the GitHub Issues section of this repository or directly to the corresponding contact.

When reporting an issue, please identify the dataset name, version, affected attribute or geometry, and a brief description of the problem.
