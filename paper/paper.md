---
title: 'DBCLS BioHackathon 2024 report: Everything about workflow and container'
title_short: 'DBCLS BioHackathon 2024: workflow and container'
tags:
  - Workflow Languages
  - Workflow Engines
  - Containers
authors:
  - name: Tomoya Tanjo
    orcid: 0000-0002-4421-9659
    affiliation: 1, 2
  - name: Kentaro Yamamoto
    orcid: 0009-0006-0201-298X
    affiliation: 3
  - name: Pitiporn Noisagul
    orcid: 0000-0000-0000-0000
    affiliation: 4
  - name: Manabu Ishii
    orcid: 0000-0002-5843-4712
    affiliation: 3
  - name: David Steinberg
    orcid: 0000-0000-0000-0000
    affiliation: 5
  - name: Naohisa Goto
    orcid: 0000-0000-0000-0000
    affiliation: 6
  - name: Michael R. Crusoe
    orcid: 0000-0002-2961-9670
    affiliation: 7, 8
  - name: Arto Bendiken
    orcid: 0000-0000-0000-0000
    affiliation: 9
  - name: Chihiro Higuchi
    orcid: 0000-0000-0000-0000
    affiliation: 10, 11

affiliations:
  - name: Bioinformation and DDBJ Center, Japan
    index: 1
  - name: BioData Science Initiative, Japan
    index: 2
  - name: Genome Analytics Japan Inc., Japan
    index: 3
  - name: CMUTEAM, Chiang Mai University, Thailand
    index: 4
  - name: University of California, Santa Cruz
    index: 5
  - name: Osaka University, Japan
    index: 6
  - name: Freie Universität Berlin, Germany
    index: 7
  - name: ELIXIR Germany
    index: 8
  - name: ASIMOV by Haltia.AI, United Arab Emirates
    index: 9
  - name: National Institutes of Biomedical Innovation, Health and Nutrition (NIBIOHN), Japan
    index: 10
  - name: Tokyo Medical and Dental University (TMDU), Japan
    index: 11
date: 30th August 2024
cito-bibliography: paper.bib
event: DBCLS BioHackathon 2024
biohackathon_name: "DBCLS BioHackathon 2024"
biohackathon_url: http://2024.biohackathon.org/
biohackathon_location: "Fukushima, Japan, 2024"
group: Project 26
# URL to project git repo --- should contain the actual paper.md:
git_url: https://github.com/biohackathon-japan/bh24-everything-about-workflow-and-container
# This is the short authors description that is used at the
# bottom of the generated paper (typically the first two authors):
authors_short: Tomoya Tanjo, Kentaro Yamamoto \emph{et al.}
---


# Introduction

Workflow engines are now widely used for genome analysis workflows.
On the other hand, there are still difficulties to build and execute their workflows in various aspects.
For example:
- How to develop our workflows in workflow languages such as CWL, snakemake, nextflow, and others?
- How to integrate our workflows with containers such as Docker, Singularity, and Podman?
- How to integrate our workflows with job schedulers such as Slurm and GridEngine?

To solve these problems, our group did the following:
- Cooperate with other groups to develop their workflows,
- Cooperate with other groups to make their workflow integrated with containers, and
- Develop and improve workflow ecosystems to remove the barriors to develop and execute their workflows. Ecosystems include workflow executors, specifications of workflow languages, workflow-related tools

This paper reports what we did during the DBCLS BioHackathon 2024.

# Formatting

This document use Markdown and you can look at [this tutorial](https://www.markdowntutorial.com/).

## Subsection level 2

Please keep sections to a maximum of only two levels.

## Tables and figures

Tables can be added in the following way, though alternatives are possible:

Table: Note that table caption is automatically numbered and should be
given before the table itself.

| Header 1 | Header 2 |
| -------- | -------- |
| item 1 | item 2 |
| item 3 | item 4 |

A figure is added with:

![Caption for BioHackrXiv logo figure](./biohackrxiv.png)

# Other main section on your manuscript level 1

Lists can be added with:

1. Item 1
2. Item 2

# Citation Typing Ontology annotation

You can use [CiTO](http://purl.org/spar/cito/2018-02-12) annotations, as explained in [this BioHackathon Europe 2021 write up](https://raw.githubusercontent.com/biohackrxiv/bhxiv-metadata/main/doc/elixir_biohackathon2021/paper.md) and [this CiTO Pilot](https://www.biomedcentral.com/collections/cito).
Using this template, you can cite an article and indicate _why_ you cite that article, for instance DisGeNET-RDF [@citesAsAuthority:Queralt2016].

The syntax in Markdown is as follows: a single intention annotation looks like
`[@usesMethodIn:Krewinkel2017]`; two or more intentions are separated
with colons, like `[@extends:discusses:Nielsen2017Scholia]`. When you cite two
different articles, you use this syntax: `[@citesAsDataSource:Ammar2022ETL; @citesAsDataSource:Arend2022BioHackEU22]`.

Possible CiTO typing annotation include:

* citesAsDataSource: when you point the reader to a source of data which may explain a claim
* usesDataFrom: when you reuse somehow (and elaborate on) the data in the cited entity
* usesMethodIn
* citesAsAuthority
* citesAsEvidence
* citesAsPotentialSolution
* citesAsRecommendedReading
* citesAsRelated
* citesAsSourceDocument
* citesForInformation
* confirms
* documents
* providesDataFor
* obtainsSupportFrom
* discusses
* extends
* agreesWith
* disagreesWith
* updates
* citation: generic citation


# Results


# Discussion

...

## Acknowledgements

...

## References
