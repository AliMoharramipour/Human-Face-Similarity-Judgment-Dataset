# **Human-Face-Similarity-Judgment-Dataset**
A large-scale dataset of 60,000 human face-similarity ranking trials collected from 445 participants across diverse set of faces. Participants ranked four faces by similarity to a target face, providing rich perceptual judgments for research on face perception.

## **Overview**
This dataset includes a large collection of human face-similarity judgments across a diverse set of 2,275 faces. Online participants were recruited via the Prolific platform to perform a similarity ranking task. These participants passed a pre-screening, ensuring that they understood the task and were well-engaged. Multiple quality controls were also included in the main task to ensure the reliability of the collected responses. After excluding poor-quality sessions, a total of 33,465 similarity-ranking trials were collected, with about 42% completed by more than one participant. We also note that all participants provided online informed consent by clicking to agree to participate before starting the task. This experiment was conducted in accordance with RIKEN's ethical guidelines. 
Please refer to our paper titled “???” for a comprehensive description of the details. 
## **Task description**
In each trial, participants viewed one target face and four choice faces. They were instructed to rank the four choice faces from most to least similar to the target face. They were asked to ignore differences in expression or head orientation. No additional cues or instructions were provided to avoid biasing their natural similarity judgments.  
## **Dataset contents**
The dataset consists of two main CSV files as follows:
## **1. Similarity_ranking_data.csv**
This file contains all completed trials across all participants. We describe each column briefly in the following: 
### **Participant number:** 
A numeric identifier for each of the 445 participants.
### **Session ID:** 
An arbitrary number reflecting the session in which a trial was completed; useful for identifying participants who completed two experimental sessions (i.e., participated twice; 147 participants after excluding poor sessions).
### **Target Face:** 
This column specifies the face ID shown as the target in each trial. The Face IDs range from 1 to 2,819. 
IDs 1 to 2,222 correspond exactly to the 2,222 faces in the 10k US Adult Faces Dataset (USAFD), with the same numbering as in the dataset folder “annotations/Face Annotations/Images and Annotations.” Note that among the 2,222 IDs, 544 IDs (i.e., faces) were not used in our data. The USAFD dataset is accessible from the following link:
[Face dateset1](https://wilmabainbridge.com/facememorability2.html)
IDs 2,223 to 2,819 correspond exactly to 597 neutral-expression faces from the Chicago Face Database (CFD). For example, face 2,223 is face 1 in the CFD dataset, face 2,224 is face 2, and so on. The CFD dataset is accessible from the following link:
[Face dateset2](https://www.chicagofaces.org/)
### **Face 1 to Face 4:** 
These columns specify the face IDs shown as the choice faces in each trial. Faces 1 to 4 were located from left to right of the screen under the target face. The IDs' descriptions are similar to those above. 
### **Trial number:** 
Each experimental session consisted of 100 trials. This column indicates the trial’s position within the session.
### **Face click order:** 
This column shows the participant’s rankings in each trial, from first (most similar to the target face) to last (least similar to the target face). For example, ['Face3', 'Face4', 'Face2', 'Face1'] indicates that the face in the column “Face3” was ranked first, the face in the “Face 4” second, the face in the “Face 2” third, and the face in “Face 1” last. 
### **Displayed-as-control:** 
Marks trials included as quality controls:
#### **Control 1:** 
Indicate a trial performed twice by the same participant within a session, but at different times in the session (e.g., trial number 15 and 50 or trial number 30 and 70), with the choice face positions on the screen reversed in the repeat.
#### **Control 2:** 
Indicate a trial in which one of the choice faces is identical to the target.
### **Unique trial number:** 
Identifies a unique trial number across our dataset. Note that some trials were performed by more than one participant or repeated by the same participant (as described by Control 1 above), or both. 
To better understand these descriptions, see our paper “???”.
## **2. Participants_demographic_data.csv**
This file contains anonymized demographic information of the participants, including Age, Gender, Ethnicity, Country of birth, Country of residence, Nationality, and first language.
