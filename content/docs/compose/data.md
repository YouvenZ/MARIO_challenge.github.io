+++
title = "🗂️ Data"
weight = 3
description = """ """
+++
Data source(s) characteristics
------------------------------

Imaging data was acquired with a Spectralis OCT device (Heidelberg Engineering). B-scan definition was 496x1024 pixels; the number of B-scans per C-scan was patient dependent (typically 49 B- scans). Consecutive examinations were registered using the Spectralis follow-up option. The data was exported in XML+bitmap format using the Spectralis software version 6.9.4.0. Data was collected at the Ophthalmology department of Brest University Hospital (France). All patients are followed-up for monitoring and treatment of vascular AMD. Imaging data was collected by ophthalmologists (retina specialists).

Training and test case characteristics
--------------------------------------

• A case refers to all information that is available for one particular patient in a specific study. This information always includes the image information as specified in data source(s) (see above) and may include context information (see above). Both training and test cases are annotated with survival (binary) 5 years after (first) image was taken.

• A case represents all the data from one patient. It is composed of 10 3-D volumes (C-scans) of OCT acquisitions per eye on average (x two eyes per patient) + a 2-D infrared image (localizer) related to each 3-D volume.

1.  Training cases: 68 patients
2.  Validation cases (off-site evaluation): 34 patients
3.  Test cases (on-site evaluation): 34 patients
4.  The number of B-scan or C-scan pairs is much larger.

For instance, for task 1, the number of B-scan pairs is 14,496 for training, 7,010 for validation and 8,341 for testing.

Data export was manual and therefore time-consuming. Manual annotation of thousands of image pairs by two retinal experts was also a time-consuming task. This was the reason for not collecting a larger dataset. However, this is larger than a similar study published by one of the organizers ([https://onlinelibrary.wiley.com/doi/full/10.1111/aos.14055](https://onlinelibrary.wiley.com/doi/full/10.1111/aos.14055)), which involved 70 patients, as opposed to 136 here.  
A ratio of 2:1:1 was used for training:validation:testing.

The patients were selected randomly among the vascular AMD patients, so their class distribution follows the real-world distribution. Assignment to the training, validation and test sets was made at random.

### Annotation characteristics

For test cases, two ophthalmologists performed the annotation independently. For training and validation cases, one ophthalmologist performed the annotation. An online annotation tool was designed for the study. Consecutive B-scans were viewed jointly on the same screen (older examination at the top, newer examination at  
the bottom).

For each pair of matched B-scans, the annotator had to assign one of the following 7 labels:

1.  _**Uninterpretable**_ 
2.  _**No activity**_
3.  _**Activity appearance**_
4.  _**Persistent activity (worsened)**_ 
5.  _**Persistent activity (stable)**_ 
6.  _**Persistent activity (improved)**_ 
7.  _**Activity disappearance.**_




While the annotations were first disign to be used this way. After some discussion and round of review we have decided to transform the annotation for the tasks.To make the problem less difficult we have reduced to four class the first task. And three class for the  

For evolution assessment between two consecutives examination (Task 1), the following fo classes are defined:
- REDUCED: 0 = ELIMINATED: 1 or PERSISTENT_REDUCED: 2
- STABLE: 1  = INACTIVE: 0 or PERSISTENT_STABLE: 3
- WORSENED: 2 = PERSISTENT_WORSENED: 4 or APPEARED: 6
- OTHER: 3 =  ININTERPRETABLE: -1 and APPEARED_AND_ELIMINATED: 5.



For the prediction of the evolution within 3 months (Task 2), the following fo classes are defined:
- REDUCE: 0 = ELIMINATED: 1 or PERSISTENT_REDUCED: 2
- STABLE: 1  = INACTIVE: 0 or PERSISTENT_STABLE: 3
- WORSENED: 2 = PERSISTENT_WORSENED: 4 or APPEARED: 6


5 patients (from the training set) were used to train the annotators. After annotating these 5 patients: 1) annotations were compared by the challenge organizers and presented to the annotators, 2) the organizers discussed their annotation strategy with each other and 3) they were given the opportunity to revise their annotations. Next, they annotated the remaining 131 patients independently.

Both annotators are ophthalmologists (retina specialists) with at least two years of experience in vascular AMD patient monitoring. Annotations from both human graders will not be merged. Agreement between both annotations will be used as a baseline to assess the agreement between an algorithm and a human grader.

Data pre-processing method(s) characteristics
---------------------------------------------

*   The XML metadata files were de-identified and all examination dates were masked (as they may be used to predict treatment decisions).  
    
*   Bitmap images (BMP) are converted to PNG to save space.
*   Two consecutives 3-D volumes are registered.
*   An automatic retina segmentation is provided for each B-scan. Participants are free to use them.

### Sources of error

The main sources of inter-annotator variability are the following

*   The distinction between an absence of disease activity and a stable activity (two types of non-evolution),
*   The distinction between an eliminated activity and a reduced (but not fully eliminated) activity. Experts thus disagreed for about 25% of the B-scan pairs.