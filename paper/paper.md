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
How to develop our workflows in workflow languages such as Common Workflow Language (CWL), snakemake, nextflow, and others?
How to integrate our workflows with containers such as Docker, Singularity, and Podman?
How to integrate our workflows with job schedulers such as Slurm and GridEngine?

Our group solved these problems with the following activities. First, we cooperated with other groups to develop their workflows, and to make their workflow integrated with containers.
Second, we developed and improved workflow ecosystems to remove the barriors to develop and execute their workflows. Ecosystems include workflow executors, specifications of workflow languages, and workflow-related tools.

This paper reports what we did during the DBCLS BioHackathon 2024.

# Outcomes in the DBCLS BioHackathon 2024


This document use Markdown and you can look at [this tutorial](https://www.markdowntutorial.com/).

## Cooperation with other groups

- share snakemake 8 tips about configuration, manabu's blog
  - configuration: https://snakemake.readthedocs.io/en/stable/snakefiles/configuration.html
  - blog: https://zenn.dev/manabuishii/scraps/6df9013c36268f
 
- We support people who want to install InterMine.

## Developments and improvements of workflow ecosystems

We reported several issues of workflow ecosystems.
- Report an issue to clarify a corner case in the spec of CWL v1.3
  - https://github.com/common-workflow-language/cwl-v1.3/issues/53
- Report an issue when passing array input parameters via command line arguments in cwltool
  - https://github.com/common-workflow-language/cwltool/issues/2034
  - Send a pull request to fix it
    - https://github.com/common-workflow-language/cwltool/pull/2037
- Report an issue that potentially breaks portability between workflow engines for CWL
  - https://github.com/common-workflow-language/schema_salad/issues/863

We also improved workflow ecosystems.

- Release a new version of shaft, an executor for CWL, to demonstrate new feature of CWL conformance test suite
  - https://github.com/tom-tan/shaft/releases/tag/v0.10.1
  - Now users see the detailed results of each test category
  - Example: detailed result of the CommandLineTool category
    - https://github.com/tom-tan/conformance/blob/master/shaft/cwl_v1.0/shaft_v0.10.1/command_line_tool.md
    - https://www.commonwl.org/v1.0/CommandLineTool.html
  - Other CWL engines can easily implement the same feature with custom GitHub Actions in the marketplace:
    - Run CWL conformance tests
      - https://github.com/marketplace/actions/run-cwl-conformance-tests
    - Upload CWL conformance badges
      - https://github.com/marketplace/actions/upload-cwl-conformance-badges
- Send a pull request to clarify undocumented spec of SALAD, that is underlying spec of CWL
  - https://github.com/common-workflow-language/schema_salad/pull/861
- Update a parser generator of SALAD for Dlang to support schemas for input objects
  - https://github.com/common-workflow-language/schema_salad/pull/825
- Update a CWL template for VSCode to use the latest syntax validator based on JSON schema
  - https://github.com/tom-tan/cwl-template-for-vscode



---

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
