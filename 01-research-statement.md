---
author: Eric J. Ma (MIT)
title: Systematic Measurements for Genotype-Phenotype Mapping
---

<!--
Robert's comments on the title, and general comments.:
1. Make title more direct. "Prediction of viral risk by systematic genotype-phenotype mapping." Make it clear that it was about viruses.
    2. >>>> done!
2. Using a single example gives the reader a "tangible example" on which I can build the case for generalizable measurements & principles.
    3. >>>> done!
 -->

**Introduction:** One goal of viral genomic surveillance is to use a virus’ sequence to predict how virulent and pathogenic it may be. **Unfortunately, the biggest gap hampering this vision is a lack of viral protein sequence variants paired with systematically measured phenotype data**, on which computational models can be trained to learn the sequence-function mapping. As a Rowland Junior Fellow, I aim to (1) develop safe, scalable and standardized assays to systematically measure influenza virus protein variants, and (2) integrate the data generation pipeline with new advances in machine learning to accurately and rapidly predict of viral risk profiles from sequence. <!--JR: I see number 2 as the real big thing. I wonder if there’s a better way to pose this as that as the focus and then using virus as an example of what could be done with any viral that you could accomplish #1 with. --><!--EM: Tricky part is that RJFs are meant to be experimentalists. Let me think about this... --> My long-term goal is to build a system for predicting, *in silico*, viral risk from its component proteins’ sequence, without requiring any experimentation on whole live viruses.

<!--
Bill's comments on section 1:
1. It's still a bit high level.
2. "neuraminidase variants' drug resistance" - not so clear.
3. "dashboard" - might be a better word. Sounds a bit colloquial.
4. Rowland fellows - I might be writing with too much jargon here.
5. "Plug-and-play" - sounds a bit colloquial.
6. Do not leave reader with impression that I'm only going to be looking at two proteins for all viruses.
7.
-->

<!--EM: I took out the figure. It isn't accurate for what I'm trying to communicate. Still thinking...-->

<!-- Try adding some content that hints at "flu being the starting system" -->

**(1) Viral phenotyping:** Health risk due to influenza virus infection is partially determined by host response, and partially determined by the virus' biochemical properties, which are in turn determined by its component proteins. In order to address the missing link of paired virus sequence-phenotype data, **we will systematically characterize influenza virus protein variants for their *in vitro* biochemical properties.**

We will start by characterizing variants of two influenza proteins: the polymerase complex's replication rate, and neuraminidase's drug resistance. We will use DNA synthesis and assembly methods to synthesize protein variants, and use robotics to scale our variant library generation and measurement steps. We will also build new assays for systematically measuring other influenza viral proteins' biochemistry, for example, by leveraging our genetic systems to rapidly test other emerging pathogens. Our long-term goal here is to develop an expandable and generalizable experimental system for biochemically testing any new virus' proteins and its variants within days of sequencing, for which the generated data could help guide clinical treatment and epidemiological interventions. A "stretch goal" would be determining the minimum number of assays required to reliably predict a virus' risk profile.

<!--
Bill's comments on section 2:
1. "viral forecasting system" - a bit misleading.
2. pointers on allostery, folding - these are important, but right now not yet mentioned. these could be added to the first paragraph.
3. Might be good to put in an example?
4. Put in some referenceable pointers for the reader, to help the reader connect back.
 -->


**(2) Computational prediction:** The viral phenotyping data generated constitute a gold standard, densely measured dataset with paired sequence and biochemical measurements. This data can be leveraged for predicting viral protein activity from sequence. This problem can essentially be cast as learning a non-linear mapping from genotype space to phenotype space.<!--JR: What is the possible/probable noise that interferes? How can it be avoided, or what else might need to be considered? Alternatives? --><!--EM: Not sure what you mean by this? --> **We will use established supervised learning algorithms to learn this mapping, while also partnering with current collaborators to develop new learning algorithms optimized for this task.**

With our experimental pipeline, data, and models, I aim to build an integrated and updateable “viral forecasting” system. This system would be backed by sequence and biochemical data, powered by machine learning, and deliver insights into viral pathogenesis. As a long-term extension of this work, such a system may enable epidemiologists to monitor and forecast which aspects of a virus' risk are trending towards danger (e.g. vaccine vs. drug susceptibility), and hence tailor outbreak responses most effectively (e.g. deploying vaccines vs. drugs). It may also help guide bedside clinical decision making, such as recommending drug combinations that a patient's virus population would be most sensitive to. With a rapid experimental pipeline, our machine learning models could be refined in real-time as new viral protein variants are discovered and tested.

<!--
Bill's comments on planned funding avenues:
1. How will being an RJF help with advancing the science? May want to emphasize this isntead of the "Funding Avenues" portion.
 -->

**Funding Avenues:** In pursuit of these goals, I have written two Broad*Next10* grant applications, one of which was co-written with colleagues at the Broad Institute, to <!-- Can we highlight this? -->pilot the development of such standardized, safe and scalable assays for the influenza polymerase and neuraminidase. **Both grants were awarded, totalling \$80,000 in funds.** Together with my current advisor, we are also collaborating with the Harvard Intelligent and Probabilistic Systems group on an NIH R21 grant to fund these efforts further. Other planned funding sources include DARPA’s Prophecy program, philanthropic groups (Gates and Simons foundations), and the NIH/NIAID. We may also explore data access/licensing models with interested industry partners to enable our research and engineering efforts to be self-sustaining.