+++
title = "MARIO challenge"
[data]
baseChartOn = 3
colors = ["#627c62", "#11819b", "#ef7f1a", "#4e1154"]
columnTitles = ["Section", "Status", "Author"]
fileLink = "content/projects.csv"
title = "Projects"
+++

{{< block "grid-2" >}}
{{< column >}}

# 🕹️ 🍄 Monitoring Age-related Macular Degeneration Progression In Optical Coherence Tomography (MARIO) - MICCAI Challenge 2024

<!-- Compose is a lean `Hugo` documentation theme, inspired by [forestry.io](https://forestry.io/docs/welcome/). -->

{{< tip "note" >}}
Welcome to the MARIO website 👋, MARIO was accepted for the edition of MICCAI challenge 2024 🚀.

 {{< /tip >}}

{{< tip >}}
For this special edition of MICCAI, we are proud to provide participants the chance to challenge their methods trained on patient data from Europe. Participants can test their algorithms with a unique set of patient data coming from the African continent to evaluate the domain generalizability of their models    
{{< /tip >}}

<!-- {{< button "docs/compose/" "Read the Docs" >}}{{< button "https://github.com/onweru/compose" "Download Theme" >}} -->

{{< /column >}}

{{< column >}}
![diy](./images/square_image_mario.png)
{{< /column >}}
{{< /block >}}





##### _**Part of [MICCAI 2024](https://conferences.miccai.org/2024/en/)  challenge**_ 

![](https://conferences.miccai.org/2024/files/images/layout/en/miccai2023-logo.png)

  

![](https://cdn-icons-png.flaticon.com/64/9874/9874671.png)Context
------------------------------------------------------------------

Age-related Macular Degeneration (AMD) is a progressive degeneration of the macula, the central part of the retina, affecting nearly 196 million people worldwide [1](#fn1). It can appear from the age of 50, and more frequently from the age of 65 onwards, causing a significant weakening of visual capacities, without destroying them. It is a complex and multifactorial pathology in which genetic and environmental risk factors are intertwined. Advanced stages of the disease (atrophy and neovascularization) affect nearly 20% of patients: they are the first cause of severe visual impairment and blindness in developed countries. Since their introduction in 2007, Anti–vascular endothelial growth factor (anti-VEGF) treatments have proven their ability to slow disease progression and even improve visual function in neovascular forms of AMD [2](#fn2). This effectiveness is optimized by ensuring a short time between the diagnosis of the pathology and the start of treatment as well as by performing regular checks and retreatment as soon as necessary [3](#fn3). It is now widely accepted that the indication for anti-VEGF treatments is based on the presence of exudative signs (subretinal and intraretinal fluid, intraretinal hyperreflective spots, etc.) visible on optical coherence tomography (OCT) [4](#fn4), a 3-D imaging modality.The use of AI for the prediction of AMD [5](#fn5) mainly focus on the first onset of early/intermediate (iAMD), atrophic (GA), and neovascular (nAMD) stage. And there is no current work on the prediction of the development of the AMD in close monitoring for patient in anti-VEGF treatments plan. Therefore, being able to reliably detect an evolution in neovascular activity [6](#fn6) by monitoring exudative signs is crucial for the correct implementation of anti-VEGF treatment strategies, which are now individualized. The objective of this challenge is to evaluate existing and new algorithms to recognize the evolution of neovascular activity in OCT scans of patients with exudative AMD, for the purpose of improving the planning of anti-VEGF treatments.  

![](https://cdn-icons-png.flaticon.com/64/3077/3077054.png)Motivation
---------------------------------------------------------------------

The objective of this challenge is to evaluate existing and new algorithms to recognize the evolution of neovascular activity in OCT scans of patients with exudative AMD, for the purpose of improving the planning of anti-VEGF treatments.  

![](https://cdn-icons-png.flaticon.com/64/8132/8132380.png)Challenge Format
---------------------------------------------------------------------------

There are three main phases to this challenge:  

1.  _**Training data & off-site validation data**_
2.  _**Off-site result submission ==> finalists**_
3.  _**Report  (For eligible solution present in the leader-board)+ Docker container submission period (for finalists)**_

All challenge submissions are in the form of a docker container, which means that participants should submit their method to be evaluated on the test sets. The training set will be released during the challenge and participants will not have access to any part of the test set.

![](https://cdn-icons-png.flaticon.com/64/762/762686.png) Tasks:
----------------------------------------------------------------

### Two tasks will be addressed in the challenge:

1.  The first task focuses on pairs of 2D slices (B-scans) from two consecutive OCT acquisitions. The goal is to classify the evolution between these two slices (before and after), which clinicians typically examine side by side on their screens.![](../../../images/mario_task_1_gray_bg.png)
2.  The second task focuses on 2D slices level. The goal is to predict the future evolution within 3 months with close monitoring of patients that are enrolled in an anti-VEGF treatments plan. 
    
    ![](../../../images/mario_task_2_gray_bg.png)
    

![](https://cdn-icons-png.flaticon.com/64/7793/7793417.png)To sum up
--------------------------------------------------------------------

 In summary, the first task aims to automate the initial step of the analysis (useful for decision support) and the second task aims to automate the complete analysis process (useful for autonomous AI).

![](https://cdn-icons-png.flaticon.com/64/8555/8555318.png) Institutions and partners
-------------------------------------------------------------------------------------

![](../../../images/partners.png)  

  

#### References  

* * *

1.  Jonas JB, Cheung CMG, Panda-Jonas S. Updates on the Epidemiology of Age-Related Macular Degeneration. Asia Pac J Ophthalmol (Phila). 2017 Nov-Dec;6(6):493-497. [↩︎](#fnref1)
    
2.  Rosenfeld PJ, Brown DM, Heier JS, Boyer DS, Kaiser PK, Chung CY, et al. Ranibizumab for neovascular age-related macular degeneration. N Engl J Med. 2006 Oct;355(14):1419-31. [↩︎](#fnref2)
    
3.  Rasmussen A, Sander B. Long-term longitudinal study of patients treated with ranibizumab for neovascular age-related macular degeneration. Curr Opin Ophthalmol. 2014 May;25(3):158-63. [↩︎](#fnref3)
    
4.  Freund KB, Korobelnik J-F, Devenyi R, Framme C, Galic J, Herbert E, et al. Treat-and-extend regimens with anti- VEGF agents in retinal diseases : A Literature Review and Consensus Recommendations. Retina (Philadelphia, Pa). 2015 Aug;35(8):1489-506. [↩︎](#fnref4)
    
5.  Bhuiyan A, Wong TY, Ting DSW, Govindaiah A, Souied EH, Smith RT. Artificial Intelligence to Stratify Severity of Age-Related Macular Degeneration (AMD) and Predict Risk of Progression to Late AMD. Transl Vis Sci Technol. 2020 Apr 24;9(2):25. doi: 10.1167/tvst.9.2.25. PMID: 32818086; PMCID: PMC7396183. [↩︎](#fnref5)
    
6.  Li E, Donati S, Lindsley KB, Krzystolik MG, Virgili G. Treatment regimens for administration of anti-vascular endothelial growth factor agents for neovascular age-related macular degeneration. Cochrane Database Syst Rev. 2020 May 5;5(5):CD012208. doi: 10.1002/14651858.CD012208.pub2. PMID: 32374423; PMCID: PMC7202375. [↩︎](#fnref6)