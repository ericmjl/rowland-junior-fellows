---
author:
- name: Eric J. Ma
  affiliation: MIT
title: Predicting influenza virus risk by systematic genotype-phenotype mapping
---

<!-- Jon's comments:

1. Could do more to emphasize the infrastructure & platform over influenza. (might just be a few word changes.) Play with wording to emphasize that the approach is broadly applicable.
1. Emphasize (in synthesis section, maybe?) the research & experimental utility of the approach.
  1. e.g. Research utility - good for predicting future outbreaks, but also for getting basic information on the protein.
  1. i.e. build as a clinical and research tool.
1. Use "I" instead of "we".
1.
 -->

***Introduction:*** One goal of viral genomic surveillance is to use a virus’ sequence to predict how virulent it may be. This is known as "phenotypic interpretation" of genomic data. The current gold standard for viral risk assessment is by identification of single point mutations experimentally associated with a phenotype, but point mutations may not be sufficient because of epistatic effects. **The scientific gap is two-fold: (1) the data gap, a lack of viral protein sequence variants paired with systematically measured phenotype data, and (2), the interpretation gap, understanding what protein features predict "riskiness".** Generating this data will enable us to progress towards a rational phenotypic interpretation, powered by computational models trained to learn sequence-function mapping. As a Rowland Junior Fellow, I aim to (1) develop safe, scalable and standardized assays to systematically measure influenza virus protein variants, and (2) integrate the data generation pipeline with new advances in machine learning to accurately and rapidly predict a virus' risk profile from its sequence. *My long-term goal is to build a system for predicting* in silico *a virus' risk from its component proteins’ sequence, while minimizing experimentation on its replicative form.*

***Aim 1: Scalable viral phenotyping.*** Health risk due to influenza virus infection is partially determined by host response, and partially determined by the virus' biochemical properties, which are in turn determined by the virus' component proteins. In order to address the missing link of paired virus sequence-phenotype data, **we will systematically characterize influenza neuraminidase for its *in vitro* biochemical properties.**

<!-- The problem of neuraminidase resistance is not well-stated. Why is neuraminidase important? (not a reason: its assay is scalable.) -->

The influenza neuraminidase is implicated in drug resistance, a clinically-relevant phenotype to measure. I will use DNA synthesis and assembly methods to generate neuraminidase variants, and use robotics to scale an established fluorescence-based assay for measuring neuraminidase activity in a 96-well microplate format. All measurements will be standardized by using a standard reference control that is repeatedly measured. The data generated will be a gold-standard, dense measurement of influenza neuraminidase properties, and will be released under a public license. I will also scale-up assays for systematically measuring other influenza viral proteins' biochemical phenotypes, such as replication rate by the polymerase (affecting viral load and hence pathogenicity). I will also leverage the genetic systems developed in my group to rapidly test other emerging pathogens. *Our long-term goal here is to develop a generalizable experimental system for biochemically testing any new virus' proteins and its variants, while minimizing experimentation on live viruses.*

***Aim 2: Computational prediction.*** The data from Aim 1 can be leveraged for predicting viral protein activity from sequence. This problem can essentially be cast as learning a non-linear mapping from genotype space to phenotype space. **I will use supervised learning algorithms trained to learn this mapping, while also partnering with current collaborators to develop more interpretable learning algorithms optimized for this task.** The models will be constructed using free and open source software (e.g. `autograd` and `scikit-learn` for Python), and will be integrated into a web-based viral phenotype prediction system, in which end users may input a viral protein sequence and have predicted phenotypes returned. All software developed will be released freely under a public license.

<!-- Change "danger" to.... some public health risk. Danger sounds a bit sensationalist. -->

***Synthesis:*** With our data generation (Aim 1) and computational prediction (Aim 2) pipelines, **I will build an integrated and continually updated viral phenotypic interpretation system**. Such a system may enable epidemiologists to monitor and predict which aspects of a virus' phenotype are trending towards "danger". For example, if circulating strains are increasing in drug resistance but remain antigenically similar to current vaccine strain, and the most effective tailored outbreak response would be deploying vaccines instead of drugs. Our phenotypic interpretation system may also help guide clinical decision making during outbreak scenarios, such as recommending drug combinations that a patient's virus population would be most sensitive to. With an integrated experimental and computational pipeline, our machine learning models can also be continually updated as new viral protein variants are discovered and tested.

<!-- Rewrite the transitions.
Most of the information in the paragraph is useful, but could be condensed/reworded more effectively.

"After developing the platform - it is likely to be attractive for ............"
-->

***Fellowship Support and Funding:*** In pursuit of the research goals described above, I have co-written and won Broad *Next10* grant applications totalling $80,000, and have led the submission of an NIH R21 grant with my current advisor Jonathan Runstadler and collaborator David Duvenaud. Other funding agencies may be interested in this effort, such as DARPA and the Gates Foundation. Furthermore, I will also explore data access & licensing models with interested industry partners to contribute to the sustainability of our research and engineering efforts.
