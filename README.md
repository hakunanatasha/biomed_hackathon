# Welcome to the BigScience🌸 Biomedical NLP Hackathon!

Huggingface's BigScience🌸 initative is an open scientific collaboration of nearly 600 researchers from 50 countries and 250 institutions who collaborate on various projects within the natural language processing (NLP) space to broaden accessibility of language datasets while working on challenging scientific questions around language modeling.  
<!--- @Natasha From the PII hackathon link --->

We are running a **Biomedical Datasets hackathon** to centralize many NLP datasets in the biological and medical space. Biological data is often diverse, so a unified location that joins multiple sources while preserving the data closest to the original form can greatly help accessbility.

## Goals of this hackathon

We want to create as many biomedical dataset **dataloader scripts** for use with the [`datasets`](https://huggingface.co/docs/datasets/) library. 

The `datasets` library contains many different datasets, from a variety of domains, and the unique natural language attributes that describe them. The strength of this library is that all these datasets can be downloaded, and accessed with a single line of code.

Our goal is to do the same for biomedical datasets, so that practioners can have easy access to these datasets. 

There are two broad categories of biomedical datasets:

##### 1. Publically licensed data
##### 2. Externally licensed data

We will accept dataloder scripts for either datatype; please see the [FAQs](#FAQs) for more explicit details. 


### How will this data be used?
<!---
Here, we should write maybe 1-3 sentences around our plans for prompting.
-->

## Contribution Guidelines

There are official guides to contributing to the `datasets` library from Huggingface's (🤗) for a [shared dataset](https://huggingface.co/docs/datasets/share_dataset.html) and to [add a dataset](https://huggingface.co/docs/datasets/add_dataset.html). Our guide follows closely from these, with adaptations to suit this intitiative.

Contributors must implement an accepted dataloading script to the library for **at least 1 dataset** to be guaranteed acknowledgement. All PRs submitted will be subject to code review prior to acceptance.

Details for contributor acknowledgements can be found [here](#Thank_you!)

## Get started

A step-by-step guide on how you can implement a dataset can be found [here](CONTRIBUTING.md).

Please ensure your dataloader follows our expected biomedical schema <!---  @Natasha This needs to be a hyperlink [Biomedical Schema]() -->

#### Pre-Requisites

Please make a github account prior to implementing a dataset; you can follow instructions to install git [here](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git). 

You will also need at Python 3.6+. If you are installing python, we recommend downloading [anaconda](https://docs.anaconda.com/anaconda/install/index.html) to curate a python environment with necessary packages. 

All commands in the guide are executed via terminal.

#### Template scripts

You can find template scripts and examples as follows: <br>

1. [Template for publically licensed data](templates/template.py)
2. [Template for externally licensed data](templates/template_local.py)
3. [Example of publically licensed data](examples/chemprot.py)
4. [Example of externally licensed data](examples/cellfinder.py)
5. [Example of Bio-C format annotation](examples/bc5cdr.py)
6. Example with BRAT format annotation (coming soon)

<!---
@NATASHA Make DDI script

[Example with BRAT format annotation](examples/ddi.py)
-->

## Community channels

We welcome contributions from a wide variety of backgrounds; we are more than happy to guide you through the process. For instructions on how to get involved or ask for help, check out the following:

#### Join BigScience
Please join the BigScience initiative [here](https://bigscience.huggingface.co/); there is a [google form] to fill out to have access to the biomedical working group slack. Once you have filled out this form, you'll get access to BigScience's google drive. There is a document where you can fill your name next to a working group; be sure to fill your name on the "Biomedical" group. 

#### Join our Discord Server
Alternatively, you can ping us on the [Biomedical Discord Server](https://discord.gg/PrhGdhJE). The Discord server can be used to share information quickly or ask code-related questions.

#### Make a Github Issue
For quick questions and clarifications, you can [make an issue via Github](https://github.com/bigscience-workshop/biomedical/issues).


## FAQs

*What if my dataset does not have a public license?*

We understand that some biomedical datasets require external licensing. To respect the agreement of the license, we recommend implementing a dataloader script that works if the user has a locally downloaded file. You can find an example [here](examples/cellfinder.py) and follow the local [template](templates/template_local.py).

*What types of libraries can we import?*

*Can I upload the data directly?*

*My dataset is complicated, can you help me?*

## Thank you!

We greatly appreciate your help - as a token or our gratitude, contributors can get the following rewards:

<!---
@Natasha
Contribution rewards:

- t-shirts?
- can we get a github star/badge that people can host on their profiles
- minimum acknowledgement in a paper; may have authorship
-->