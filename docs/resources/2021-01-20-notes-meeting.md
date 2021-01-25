# Notes from 2021-01-20 meeting

## TDWG Species Interaction Data Meeting Notes

Date: `2021-01-20`

### Participants:

Antonio Saraiva, University of São Paulo
Quentin Groom, Meise Botanic Garden
Dmitry Schigel, GBIF Secretariat
Maarten Trekels, Meise Botanic Garden
José Augusto Salim, University of São Paulo
Kayna Agostini, Federal University of São Carlos
Paula Zermoglio, VertNet
Francisco Pando, Real Jardin Botanico, Madrid /GBIF-Spain
Willem Coetzer, South Africa Inst Aquatic Biodiversity

### Notes from the meeting

- Salim shared an interested publication calling the community to debate the definition of *species interactions*: [Species interaction: Revisiting its terminology and concept
](https://doi.org/10.1111/1440-1703.12164)
- Salim point out that Event Sample Data has been used to create and share datasets of plant-pollinator interactions within Brazilian Network on Plant-Pollinator Interactions. At this moment, a vocabulary of terms is being developed to be used with DwC:MeasurementOrFact to describe characteristics of Interaction.
- Dmitry Schigel, GBIF Secretariat, confirms that GBIF is (long-term) interested in interactions data, and the timing is great as GBIF is working on the next strategic period in 2021, which will be for the 2023-2028
- Dmitry put the questions to be handle by the group:
    - Possible question to ask and to answer to help inform practical work on developing efficient - and popular! - standard:
    - How do people handle, store, exchange, export their interactions data today? Landscaping review paper on the world of interactions data today (task group paper?)
    - What would be the efficient way to handle and to output interactions data to enable uptake and reuse? As we want i-data to be reused, and not only in sci context, but also policy such as indicators, EBVs, etc.
- Kayna presented a great schema - on ecological interactions:
![ecological interaction schema][image2]
- Dmitry mention that Pensoft’s journals introduce a standard appendix template for primary biodiversity data to provide direct harvesting and conversion to interlinked FAIR data
[https://blog.pensoft.net/2020/04/24/how-to-get-data-from-research-articles-back-into-the-research-cycle-%D0%B0t-no-additional-costs/](https://blog.pensoft.net/2020/04/24/how-to-get-data-from-research-articles-back-into-the-research-cycle-%D0%B0t-no-additional-costs/)
- Francisco presented the Plinian Core (Species Information IG > https://github.com/tdwg/PlinianCore ) approach for Biological Interactions at the aggregation level (organism-organism), and reuses DwC terms for it: [https://github.com/tdwg/PlinianCore/wiki/InteractionsType](https://github.com/tdwg/PlinianCore/wiki/InteractionsType)
![plinian core][image1]
    - A presentation on the whereabouts and issues found of this approach was delivered at TDWG 2017: (https://api.zotero.org/users/7403307/publications/items/YNS4J57J/file/view) 
    - Some concerns have been expressed about using dwc:ResourceRelationship in RDF:
        - "Any Darwin Core class IRI may be used as a value for rdf:type, although it is not clear whether dwc:ResourceRelationship instances make sense in the context of RDF" (RDF Guide, Section 2.3.1.5, [https://dwc.tdwg.org/rdf/](https://dwc.tdwg.org/rdf/) 
        - [TDWG dicussion on ResourceRelationship and RDF](https://github.com/tdwg/rdf/blob/master/ResourceRelationship.md)
        - [Open Annotation Model and ResourceRelantionship](https://github.com/tdwg/rdf/blob/071d40c2412fc9a032183a92e64757aaa412c539/OpenAnnotationAndTDWG.md)
        - [Open Annotation Model and ResourceRelantionship 2](https://github.com/tdwg/rdf/blob/071d40c2412fc9a032183a92e64757aaa412c539/OAThread.md)
        - **Possible solutions** (still in discussion):
            - [RDF Reification](https://www.w3.org/TR/2004/REC-rdf-primer-20040210/#reification)
            - [N-ary Relations](https://www.w3.org/TR/swbp-n-aryRelations/)
- A old discussion about *species interaction data* in GBIF mail list: [https://lists.gbif.org/pipermail/ipt/2018-July/000713.html](https://lists.gbif.org/pipermail/ipt/2018-July/000713.html)
- Salim speak about the experience with plant-pollinators interactions, it has shown that most of the descriptors/terms/fields are more or less related to species traits than with the interactions. And proposed that each community should create its own vocabulary of traits (e.g. traits most important to interactions) and use Ecological Trait Data Standard (ETS) [https://terminologies.gfbio.org/terms/ets/pages/index.html](https://terminologies.gfbio.org/terms/ets/pages/index.html).

### Possible work setup:
- Figure out and use a robust theory of biological interactions, including food web and network ecology concepts (thanks QG!). Some refs:
    - [https://en.wikipedia.org/wiki/Biological_interaction](https://en.wikipedia.org/wiki/Biological_interaction)
    - [https://doi.org/10.1111/1440-1703.12164](https://doi.org/10.1111/1440-1703.12164)
- Landscaping review **standard development**: case studies for dynamic refine of the developing model, such as pollinators, soil, microbes, etc.
- Calls for separating occurrence, fact recording capture and management of interactions data from human interpretations of those co-occurrences from species level summaries (which is not data, but knowledge)
- Data centralisation, aggregation means compromise

### What can DwC can do today?
 - Dmitry presented a sketch of data model for *species interaction data* based on DwC Event Sample Data.
 ![wild sketch][image3]
 - Salim confirms that the sketch presented by Dmitry is similar of one used within Brazilian Network on Plant-Pollinators.
- Questions to be addressed: 
    - A good glossary / ontology to document interactions is available at GloBI?
- Salim brings a (short) list of examples of how and who has been used DwC to document *species interaction*:
    - Catalogue of the Rust Fungi of Belgium: [https://trias-project.github.io/uredinales-belgium-checklist/dwc_mapping.html](https://trias-project.github.io/uredinales-belgium-checklist/dwc_mapping.html)
    - Plinian Core [https://github.com/tdwg/PlinianCore/wiki/InteractionAtomizedClass](https://github.com/tdwg/PlinianCore/wiki/InteractionAtomizedClass)
    - Non-standard DwC *association extension* developed by Encyclopedia of Life (EOL) and employed in the Global Biotic Interactions and in the Tri-Trophic Thematic Collection Network (TTD): [https://content.iospress.com/articles/semantic-web/sw190](https://content.iospress.com/articles/semantic-web/sw190)
    - GloBI:[https://www.globalbioticinteractions.org/2018/08/16/models-in-fashion/](https://www.globalbioticinteractions.org/2018/08/16/models-in-fashion/)
    - Tri-trophic Thematic Collection Network (TTD): [http://tcn.amnh.org/](http://tcn.amnh.org/)
    - Species Interactions of Australia Database [https://www.discoverlife.org/siad/](https://www.discoverlife.org/siad/) with examples of datasets and vocabulary of *interaction types*


[image1]: images/image1.png
[image2]: images/image2.png
[image3]: images/image3.png


