# Brain Computer Interface Project
Project aiming to develop a full pipeline to record EEG data, preproces raw data, extract features and train a classification model to carry out desired motor tasks. From there we would like to implement this pipeline in realtime to carry out tasks during EEG recordings.

- Authors: Arthur Roumaillac, Arthur Lesle, Sasha Sutton

## Project Outline
We are currently working on a simple motor task to learn to preprocess raw data and extract features. The task involves lifting the right arm or left arm and using a classification model to differentiate between the two. We are using an OpenBCI cyton headset with 8 electrodes. Here are the current preprocessing and feature extraction steps we have taken.

#### Preprocessing
- High pass filter at 1Hz to elimenate DC drift
- Notch filter at 50Hz to remove the power line frequency
- Band pass filter between 8Hz and 30Hz to isolate motor movements
- Re-reference by removing the mean of every channel

ToDo
- Remove artifacts, such as eyeblinking, using ICA
- Identify and remove bad channels

#### Feature Extraction
- Currently evaluating the use of different features in the time and frequency domain.

## Future Plan
#### Model Classification
Once we have preprocessed the data and extracted features of interest we want to train a classification model. We currently envision using a support vector machine (SVM) for our current task but we would like to try different models to see how they differ and maybe even some deep learning models.
#### Motor Imagery
The final goal is to implement our pipeline for motor imagery tasks. This will therefore involve thinking of a motor action instead of physically carrying out the motor action. Changes will probably have to be made to the pipeline specifically in the feature extraction phase. 