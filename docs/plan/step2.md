# Landscaping review

The main goal on this step collect information of available resources about species interaction data, study cases and *standard* development, creating a list and providing a detailed description of funcionalities, advantages and disadvantages of each resource.

## Planning

### Datasets

We analyzed **392** datasets from [GloBI sources](https://www.globalbioticinteractions.org/sources) and those found with [Google Dataset Search](https://datasetsearch.research.google.com/).

The Google Dataset Search was used to search for interaction datasets not indexed by GloBI, using the follow *search string*:
```
"species interaction" OR "biotic interaction" OR "interaction network" OR "trophic interaction" OR "food web" OR "plant-pollinator" OR "predator-prey"
```

The search returned **81** datasets which are not indexed by GloBI.

### Dataset metadata

The analysis of the datasets were conducted in order to understand how people organize and share interactions data. For each dataset the follow metadata are extracted (when available):
- Metadata about the related scientific publication (i.e. DOI, title, year, abstract, publication type, keywords, authors, journal).
- Repository where the dataset is stored
- General data structure/schema used, classified in following categories:
    + *TABULAR/INTERACTION_RECORDS*: interactions are represented by individual records (one interaction per line/row). Each record contains data about both interaction partners (**source** and **target** species).
    + *TABULAR/CHECK_LIST*: interactions are given as a list of interaction partners for a specific taxon (not mentioned in the dataset)
    + *DWCA*: Darwin Core Archives which may use *associatedTaxa*, *associatedOccurrences*, *ResourceRelationship* or another DwC term to stored interaction data.
    + *ADJ MATRIX*: adjacency matrix are used to share interactions network where the first row/column are species name or identifiers. The adjancency matrix can be binary or non-binary matrix, and usually a **0** represents no interaction and a value greater than **0** indicates an interaction between species at given row/column.
    + *G(V,E)*: a network interactions where a list of nodes (species) and a list of links (interactions) are given separately    
    + *NATURAL_LANGUAGE*: interactions are given in natural language (textual) within publications.
    + *CUSTOM_API*: custom API's comprising different schemas are grouped together.
- Dataset file format (e.g. CSV, ZIP, HTML, RData)
- Dataset Metadata (ie. title, description, keywords, year, metadata URL)
- Interaction types classified according to [Relation Ontology](http://www.ontobee.org/ontology/RO).
- Interaction level:
    + *species-species*: species interaction. No spatial or temporal information about the interacting species are given, just taxa.
    + *occurrence-species*: Spatial or temporal information are given to just one of the interacting partners.
    + *occurrence-occurrence*: Spatial or temporal information are given for both interacting partners.
- Relational model:
-   *single*: data is store in just one file (flat-table).
-   *multiple*: data is store in multiple files (relational).

## Results

### Datasets by Year of Publication

![Datasets by Year](/resources/images/dataset-years.png)

### Datasets Keywords

![Dataset keywords](/resources/images/wc-keywords.png)

### Repositores

![Dataset repositories](/resources/images/dataset-repos.png)

### File Formats

![Dataset formats](/resources/images/dataset-format.png)

### Structure/Schema

![Dataset schema](/resources/images/dataset-schemas.png)

### Interaction Level

![Dataset interaction level](/resources/images/dataset-interaction-level.png)

### Topic Modelling

![TM k 4](/resources/images/tm-k-4.png)

### Darwin Core Archives

Proportion of DwC-A that uses **associatedTaxa**, **associatedOccurrences** and **ResourceRelationship**. Data were not investigated in order to verify if interaction information are given using this terms/class. It just summarizes the proportion of DwC-A which have non-empty values of any of those terms/class.

![DwCA terms](/resources/images/dwca-chart.png)
