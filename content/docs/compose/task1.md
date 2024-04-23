+++
title = "1️⃣🎯 Task 1"
weight = 6
description = """ """
+++

# TASK 1: Classify evolution between two pairs of 2-D slices from two consecutive 2D OCT acquisitions.

1.  The first task focuses on pairs of 2D slices (B-scans) from two consecutive OCT acquisitions. The goal is to classify the evolution between these two slices (before and after), which clinicians typically examine side by side on their screens.![](/../../images/mario_task_1_gray_bg.png)

For evolution assessment between two consecutives examination (Task 1), the following fo classes are defined.
- REDUCED: 0 = ELIMINATED: 1 or PERSISTENT_REDUCED: 2
- STABLE: 1  = INACTIVE: 0 or PERSISTENT_STABLE: 3
- WORSENED: 2 = PERSISTENT_WORSENED: 4 or APPEARED: 6
- OTHER: 3 =  ININTERPRETABLE: -1 and APPEARED_AND_ELIMINATED: 5.

Like it is illustrated we provide to participants along side with the OCT for each visit an localizers and some clinical data. We encourage the participants to develop multi-modal method to takle this task. **It should be noted that the minimun input expected for your algoritm development should be at least the OCT B-scan.**  




To participate to the challenge register using this [link]()