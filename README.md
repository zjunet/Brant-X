# Brant-X
Brant-X is the first physiological signal alignment framework that can model various physiological data like EOG, ECG and EMG. Brant-X performs knowledge transfer from EEG to other physiological signals, allowing the data and model resources in the EEG field to empower the research on other physiological signals. 

<br />

### Framework

![framework](./img/framework.png)

#### Pipeline

Firstly, based on the EEG foundation model, the EXG encoder is trained by the alignment between synchronously collected EEG and EXG data. 
Then, the EEG and EXG encoders, capable of learning strong representations from EEG and EXG signals, are applied to various downstream tasks in diverse scenarios.

#### The foudnation model

Brant-X employs the EEG foundation model Brant-2 as its EEG encoder to transfer the rich knowledge from the EEG foundation model to other physiological signals. 

> Zhizhang Yuan, Daoze Zhang, Junru Chen, Gefei Gu, and Yang Yang. Brant-2: Foundation Model for Brain Signals. arXiv preprint arXiv:2402.10251 (2024) [\[paper\]](https://arxiv.org/abs/2402.10251) 

<br />


### Review of Public Multi-type Physio-signal Datasets

To serve as a research resource for multi-type signal modeling, we summarize those public datasets that contain two or more types of signals among EEG, EOG, ECG, and EMG, as presented in `dataset_review_table.pdf`. 

In the table, we provide statistical information including: 
- data size, 
- number of participating subjects (`#Subj.`), 
- number of channels (`#Ch.`), and 
- sampling rate (`Samp.`) for each signal, 

for researchers to reference based on their needs. 
