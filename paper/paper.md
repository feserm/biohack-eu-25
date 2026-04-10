---
title: 'BioHackEU25 report: Minimal information standardization of phenomic experimental data in animals'
title_short: 'BioHackEU25 #17: Minimal information standardisation'
tags:
  - domestic animal
  - phenotyping
  - standardization
  - ISA
authors:
  - name: Sarah Oranna Fischer
    orcid: 0000-0002-6218-7275
    affiliation: 1
    role: Investigation, Conceptualization, Writing – original draft, Writing – review & editing
  - name: Rica Johanna Rehfeld
    orcid: 0009-0007-3289-5872
    affiliation: 2
    role: Investigation, Conceptualization, Writing – original draft, Writing – review & editing
  - name: McKinley Santiago
    orcid: 0009-0009-1160-5041
    affiliation: 3
    role: Investigation
  - name: Emily Clark
    orcid: 0000-0002-9550-7407
    affiliation: 4
    role: Conceptualization
  - name: Daniel Arend
    affiliation: 5
    role: Writing – review & editing
  - name: Manuel Feser
    orcid: 0000-0001-6546-1818
    affiliation: 5
    role: Investigation, Conceptualization, Writing – review & editing
affiliations:
  - name: FBN Dummerstorf
    ror: https://ror.org/02n5r1g44
    index: 1
  - name: IEC, University Medical Centre Rostock
    ror: https://ror.org/04dm1cm79 
    index: 2
  - name: Atrium Health Wake Forest Baptist
    ror: https://ror.org/0207ad724
    index: 3
  - name: EMBL EBI
    ror: https://ror.org/02catss52
    index: 4
  - name: IPK Gatersleben
    ror: https://ror.org/02skbsp27
    index: 5
date: 7 November 2025
cito-bibliography: paper.bib
event: BH25EU
biohackathon_name: "BioHackathon Europe 2025"
biohackathon_url:   "https://biohackathon-europe.org/"
biohackathon_location: "Bad Saarow, Germany, 2025"
group: Project 17
# URL to project git repo --- should contain the actual paper.md:
git_url: https://github.com/feserm/biohack-eu-25
# This is the short authors description that is used at the
# bottom of the generated paper (typically the first two authors):
authors_short: Fischer and Rehfeld \emph{et al.}
---


# Introduction

The current landscape of animal phenomics is characterized by a substantial lack of standardization, hindering data reuse, reproducibility, and interoperability across studies, all of which are particularly important in light of the 3Rs principles for animal experiments (replace, reduce, refine) [@citesAsRelated:hubrecht_3rs_2019]. Within ELIXIR, the [Domestic Animals Genome and Phenome Focus Group](https://elixir-europe.org/focus-groups/domestic-animals-genome-phenome) (since December 2025 an ELIXIR community) emerged to establish standardized practices that enhance the quality and interoperability of animal research data. In this context, the ISA (Investigation, Study, Assay) model [@citesAsRelated:sansone_toward_2012] provides a robust, domain-agnostic framework well established in several life sciences for describing experimental metadata, such as the ELIXIR [Plant](https://elixir-europe.org/communities/plant-sciences) and [Metabolomics](https://elixir-europe.org/communities/metabolomics) Communities (MIAPPE, PhenoMeNal), which have successfully leveraged the ISA model to improve the consistency and usability of their metadata [@citesAsRelated:papoutsoglou_enabling_2020][@citesAsRelated:peters_phenomenal_2019].

Our project aims to develop a minimal information checklist tailored to animal phenomics, facilitate the integration of diverse datasets, including recirculation systems in agriculture, and foster collaborative research efforts. We will focus on various goals.

1. Identifying essential aspects of animal phenotyping, informed by existing frameworks and community input. We aim to produce a concise and practical checklist that can be easily adopted by researchers and promote a culture of standardization.
2. Mapping the checklist to the ISA model ensures alignment with established standards, promotes interoperability between life science domains, facilitates data reuse and improves the overall quality of research outputs.
3. Adopting existing ISA tools streamlines the implementation of our metadata checklist, providing user-friendly interfaces for researchers to manage, document, and share animal phenotyping data efficiently.

## Updating the defined goals

Due to the unexpected complexity of our goal – but it's also the most important for all following – we adjusted our aims. Our updated objectives are centered on identifying the essential aspects of animal phenotyping, developing a concise and practical checklist to support standardization, and mapping these aspects to the ISA model. The requirement for a community-based approach has also become clear, with the needs of the wider community being a key consideration. Therefore, we decided to postpone these activities as well as activities related to configuring ISA tooling and showcasing the benefits of the checklist until after the hackathon. The results of our work were presented at the February meeting of the ELIXIR Domestic Animals Genome and Phenome Focus Group / Community, where we defined the next steps.

# Results

We began by compiling metadata information already available from established community standards, in particular FAANG [@citesAsRelated:harrison_faang_2018] and MIAPPE (Minimal Information About a Plant Phenotyping Experiment) [@citesAsRelated:papoutsoglou_enabling_2020]. These resources provided a solid foundation for identifying the core descriptors relevant to animal phenotyping and for understanding how similar initiatives have approached metadata harmonization.
MIAPPE
Building on this, we created a structured checklist aimed at capturing the essential aspects of animal phenotyping in a consistent and reusable way. The checklist was implemented as a [spreadsheet](https://github.com/elixir-europe/biohackathon-projects-2025/blob/364145ab8d705846ef3c1d32ecdb091ea1153ec7/17-minimal-information/Checklist_for_publication%20-%20animal_ISA_checklist_v0.pdf) with the following headers: Descriptor, Definition, Example, Format, Cardinality, Source, Comment, ISA Entity, and ISA Field. Structuring the content along ISA entities - alike MIAPPE - ensured that each metadata element could later be easily mapped to the appropriate component within the ISA model, thereby simplifying data integration and interoperability. Thus, the mapping to the ISA framework was carried out directly within the checklist spreadsheet, using references from the ISA‑JSON schemas. This approach allowed us to link each identified metadata term with its corresponding ISA field and to verify that the representation followed the ISA syntax and semantics. During this process, we identified the need to introduce additional animal‑specific terms that were naturally not present in MIAPPE, such as sex, date_of_birth, and animal_number. These additions were essential for adequately describing individuals or groups of animals and for supporting the reproducibility of experiments. 

Furthermore, we refined the section describing the study protocol by adding specific terms that follow a standardized SOP naming convention. This step improves clarity and facilitates the alignment of experimental procedures across studies. Overall, the resulting checklist and mapping provide a robust basis for future work on standardizing animal phenotyping metadata and for configuring ISA tools to demonstrate their benefits in practical data management workflows.

# Discussion
Due to fundamental differences between animal and plant phenotyping, ongoing discussions have emerged regarding the appropriate frameworks and standards for metadata collection and reporting. These debates continue to evolve as researchers strive to develop comprehensive, interoperable, and species-agnostic approaches. Key points of contention include:

The management and identification of individuals involved in phenotyping investigations, such as researchers, technicians, and data curators, remain a central challenge:

While the [MIAPPE standard](https://github.com/miappe/miappe) aggregates all personnel at the study level and provides a unified view across the entire investigation, identifying a single point of contact for specific data queries can be problematic considering the number of people involved in an animal-related project, in view of e.g. the stable staff or animal caregiver, the researchers and the veterinarians. This issue is echoed in other standards, including [ABCD (Access to Biological Collections Data)](http://www.tdwg.org/standards/115) and [FAANG (Functional Annotation of Animal Genomes)](https://dcc-documentation.readthedocs.io/en/latest/), which also recommend designating one or two primary contact persons. In alignment with MIAPPE’s structure, the ISA framework has been adopted, with the addition of the [CRediT (Contributor Roles Taxonomy)](https://credit.niso.org/) ontology to explicitly define the roles of individuals involved in data generation and analysis. In contrast, FAANG employs the [EFO (Experimental Factor Ontology)](http://www.ebi.ac.uk/efo/efo.owl) for role specification, applying it at both the organizational and individual levels, which introduces a different semantic layer for person-role associations.

Another persistent challenge lies in defining the minimum set of metadata required for animal phenotyping experiments. Certain metadata terms, such as location specifications, are critically important for some species, particularly those with strong environmental dependencies, while being less relevant or even redundant for others, such as laboratory animals housed in controlled environments. As a result, the decision to designate specific terms as "minimal" often involves trade-offs, with some terms included in the minimal set despite variable relevance across species.

## Missing cross-species ontologies
A significant gap in the animal phenotyping domain is the lack of comprehensive, cross-species ontologies. While [curated ontologies](https://opendata.inra.fr/EOL/page/eol_ontology) exist for livestock animals, developed by INRAE (Institut National de Recherche pour l’Agriculture, l’Alimentation et l’Environnement) in France, these are often unsuitable for other animal groups due to incorrect hierarchical classifications. For example, laboratory animals cannot be appropriately classified under the term *mixed husbandry* when its semantic placement resides within the *livestock management system*, creating a mismatch in biological context. Furthermore, many well-established ontologies in plant phenotyping, such as those describing growth protocols, measurement techniques, or experimental designs, are either absent or underdeveloped in the animal domain. This gap underscores the urgent need to develop or adapt new ontologies tailored to the specific needs of animal phenotyping research.
Linking data to controlled vocabularies, thesauri, or ontologies also presents practical difficulties. The ISA framework often associates terms with an ontology annotation. The ISA assay, e.g. characterizes the *measurementType* with an ontology annotation. However, in many animal phenotyping contexts, the appropriate ontology terms remain undefined or unavailable, leading to empty or placeholder entries. This limitation hinders data interoperability and semantic enrichment.

The conceptualization of biological material, particularly the identification of individual animals, has also sparked debate. In MIAPPE, the term *biological material* refers to discrete units such as plant accessions or seeds in genebanks. By analogy, in animal phenotyping, this could correspond to an embryo in utero or a newly born individual. However, in many experimental designs, especially those involving non-model organisms like fish or fruit flies, pedigree information may be absent, irrelevant, or impossible to trace. In such cases, the biological material may instead be defined as a single animal or a batch of animals originating from a shared source, complicating the standardization of material tracking.

Additionally, the use of external identifiers such as biosample accessions is common in animal phenotyping, but these are not considered as part of the minimal metadata standard. This distinction is important for ensuring that the core information required for reproducibility and interpretation remains focused and accessible, without being burdened by external referencing systems.

Finally, the naming of the proposed minimal information standard has been a topic of discussion. A memorable, intuitive, and logically structured name is essential for ensuring widespread adoption and discoverability. Several candidate names have been proposed, including *mispeds*, *PetMIAnimal* (Phenotypic Minimal Information Standard for Animals), and *MISape* (Minimal Information Standard for Animal Phenotyping Experiment), each aiming to reflect the standard’s purpose while remaining distinct and user-friendly.


# Outlook
Looking ahead, the transformation of the Domestic Animals Genome and Phenome Focus Group into a formal, collaborative ELIXIR community presents a promising opportunity to further advance and institutionalize our standardization approach. By integrating this framework with established tools from other communities, such as ARC and RO-Crate, we expect to significantly enhance the FAIRness of animal phenotypic data. This synergy will empower researchers to more easily share, integrate, and analyze data across domains and species, accelerating discovery in animal health, breeding, and welfare. The growing community will also serve as a hub for innovation, driving the development of new ontologies, best practices, and software extensions tailored to evolving research needs. 

# Acknowledgements

We would like to thank the ELIXIR community and the organizers of BioHackathon Europe for the opportunity to conduct this work as part of BioHackathon Europe 2025.
This work was funded by ELIXIR, the research infrastructure for life-science data; by the Federal Government of Germany and the county of North Rhine-Westphalia (de.NBI - the GermanNetwork for Bioinformatics Infrastructure); the DFG in frame of the FAIRagro (www.fairagro.net, project number 501899475), NFDI4BioDiversity (www.nfdi4biodiversity.org, project number 442032008) consortia of the NFDI; and KI Tierwohl (www.ki-tierwohl.de, funded by the European Regional Development Fund of the European Union as part of the ERDF programme 2021 to 2027 of the state of Mecklenburg-Vorpommern, EXF-25-1031 to EXF-25-1038).
