---
author:
- name: Eric J. Ma
  affiliation: MIT
title: Predicting influenza virus risk by systematic genotype-phenotype mapping
---

***Introduction:*** One goal of viral genomic surveillance is to use a virus’ sequence to predict how virulent and pathogenic it may be. Because of allosteric and epistatic effects, single point mutations may not be sufficient for identifying a "risky" virus, yet this is the current gold standard for viral risk assessment. **The scientific gap here is a lack of viral protein sequence variants paired with systematically measured phenotype data**. Generating this data will enable us to progress towards training computational models to learn sequence-function mapping. As a Rowland Junior Fellow, I aim to (1) develop safe, scalable and standardized assays to systematically measure influenza virus protein variants, and (2) integrate the data generation pipeline with new advances in machine learning to accurately and rapidly predict a virus' risk profile from its sequence. <!--JR: I see number 2 as the real big thing. I wonder if there’s a better way to pose this as that as the focus and then using virus as an example of what could be done with any viral that you could accomplish #1 with. --><!--EM: Tricky part is that RJFs are meant to be experimentalists. Let me think about this... --> My long-term goal is to build a system for predicting *in silico* viral risk from its component proteins’ sequence, without requiring any experimentation on whole live viruses.

<!--
Bill's comments on section 1:
1. It's still a bit high level.
3. "dashboard" - might be a better word. Sounds a bit colloquial.
4. Rowland fellows - I might be writing with too much jargon here, as they are a diverse group of people, not necessarily life scientists.
5. "Plug-and-play" - sounds a bit colloquial. >>> done - removed from text.
6. Do not leave reader with impression that I'm only going to be looking at two proteins for all viruses. >>> done.
-->

***Aim 1: Scalable viral phenotyping.*** Health risk due to influenza virus infection is partially determined by host response, and partially determined by the virus' biochemical properties, which are in turn determined by its component proteins. In order to address the missing link of paired virus sequence-phenotype data, **we will systematically characterize influenza virus protein variants for their *in vitro* biochemical properties.**

We will start by systematically characterizing the phenotype of two influenza proteins: RNA replication rate of the polymerase complex, and drug resistance of the neuraminidase protein. We will use DNA synthesis and assembly methods to generate protein variants, and use robotics to scale our variant library generation and measurement steps. We will then scale established assays for measuring neuraminidase and polymerase activity in a 96-well microplate format, and standardize the measurements by using a standard reference control. The data generated will be a gold-standard, dense measurement of influenza viral properties, and will be released under a permissive public license. We will also build new assays for systematically measuring other influenza viral proteins' biochemical phenotypes, and leveraging our genetic systems to rapidly test other emerging pathogens. Our long-term goal here is to develop a generalizable experimental system for biochemically testing any new virus' proteins and its variants.

<!--
Bill's comments on section 2:
1. "viral forecasting system" - a bit misleading. >>> done
3. Might be good to put in an example? >>> done!
4. Put in some referenceable pointers for the reader, to help the reader connect back.
 -->

***Aim 2: Computational prediction.*** The data from Aim 1 can be leveraged for predicting viral protein activity from sequence. This problem can essentially be cast as learning a non-linear mapping from genotype space to phenotype space. **We will use established supervised learning algorithms to learn this mapping, while also partnering with current collaborators to develop new learning algorithms optimized for this task.** The models will be constructed using free and open source software (`autograd` and `scikit-learn`). The models will be integrated into a web-based viral phenotype prediction system, in which end users may input a viral protein sequence and have the predicted relevant phenotypes returned.

With our data generation and computational prediction pipelines, we will build an integrated and continually updated computational viral characterization system. Such a system may enable epidemiologists to monitor and predict which aspects of a virus' phenotype are trending towards danger (e.g. circulating strains are increasing in drug resistance but not antigenic distance to current vaccine strain), and hence tailor outbreak responses most effectively (e.g. deploying vaccines instead of drugs). It may also help guide clinical decision making, such as recommending drug combinations that a patient's virus population would be most sensitive to. With a rapid experimental pipeline, our machine learning models can also be refined in real-time as new viral protein variants are discovered and tested.

***Fellowship Support and Funding:*** The Rowland Institute can provide the necessary environment and support for this project. For example, I can foresee leveraging the machine shop to help design parts for custom robotics that may be required. The multidisciplinary nature of this project will likewise benefit from the varied subject areas represented at the Rowland Institute. In pursuit of the research goals described above, I have also co-written and won Broad *Next10* grant applications totaling $80,000, and have led the submission of an NIH R21 grant with my current advisor Jonathan Runstadler and collaborator David Duvenaud. Research funding provided by the Rowland Institute will also help me establish this research program, while we source funds from additional sources (e.g. DARPA, Gates Foundation). In order to ensure that our research and engineering efforts are self-sustaining, we will also explore data access & licensing models with interested industry partners.
