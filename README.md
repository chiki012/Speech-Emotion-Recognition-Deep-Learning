# Speech-Emotion-Recognition-Deep-Learning

## Dataset: RAVDESS (Ryerson Audio-Visual Database of Emotional Speech and Song)

The RAVDESS dataset consists of 1440 audio files containing emotional expressions performed by 24 professional actors (12 female, 12 male). The emotions include calm, happy, sad, angry, fearful, surprise, and disgust, each expressed at normal and strong intensities, along with an additional neutral expression.

### Dataset Overview

Each file has a unique filename with a 7-part numerical identifier defining stimulus characteristics:

1. Modality (01 = full-AV, 02 = video-only, 03 = audio-only).
2. Vocal channel (01 = speech, 02 = song).
3. Emotion (01 = neutral, 02 = calm, ..., 08 = surprised).
4. Emotional intensity (01 = normal, 02 = strong).
5. Statement (01 = "Kids are talking by the door", 02 = "Dogs are sitting by the door").
6. Repetition (01 = 1st repetition, 02 = 2nd repetition).
7. Actor (01 to 24, odd numbered actors are male, even numbered actors are female).

## Project Overview

1. **Log Mel Spectrogram Generation:**
   - Create Log Mel Spectrograms for both genders for different emotions.

2. **Data Processing and Labeling:**
   - Distribution of classes through graph representation.
   - Feature extraction.

3. **Train-Test Split:**
   - Split data into training and testing sets.
   - `x_test` shape: (288, 259)
   - `x_train` shape: (1152, 259)
   - Base model prediction accuracy: 38.54%

4. **Data Preprocessing:**
   - One-hot encoding of labels.

5. **Initial Model: 1D CNN Layers:**
   - Total params: 1,129,384
   - Trainable params: 1,128,488
   - Non-trainable params: 896

6. **Model Training:**
   - Experimented with different batch sizes and epochs.
     - Batch_size=32, Epochs=50: Loss - 4.85, Accuracy - 44.79%
     - Batch_size=64, Epochs=50: Loss - 4.02, Accuracy - 50.0%
     - Batch_size=128, Epochs=50: Loss - 4.47, Accuracy - 50.34%

7. **Evaluation:**
   - Actual values vs. prediction values.
   - Confusion matrix of actual vs. predicted emotions.

**Note:** Make sure to install the required dependencies and libraries before running the code.
