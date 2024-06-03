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


### Requirements

The code runs on Python 3.8.16 and requires the following packages: 

```
info-nce-pytorch==0.1.4
mne==1.4.2
numpy==1.24.3
pandas==2.0.3
scikit-learn==1.2.2
scipy==1.10.1
torch==2.0.1
tqdm==4.64.1
transformers==4.36.2
```
<br />


### Code

- The program entry for the alignment process is in `/code/align.py` .
- The program entry for the four evaluation tasks is in `/code/downstream.py` . To select which evaluation task to run, you can choose one from the following four options as the input for the `--task` parameter: 
  - `SleepEDFx` for the sleep stage classification task,
  - `DREAMER` for the emotion recognition task,
  - `FOG` for the freezing of gaits (FoG) detection task, and
  - `EyeALS` for the eye movement communication task.
- `/code/src/align/` contains the code for the unsupervised alignmnet.
- `/code/src/downstream/` contains the code for training and evaluation on four main tasks.




