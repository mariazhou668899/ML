# Self-Learning Experiment: WaveNet Testing using RAW EEG Features
This notebook explores using WaveNet to predict brain events based on raw EEG waveforms in Kaggle's Brain competition. The main objective is to assess how effectively WaveNet can learn patterns in brain activity from minimal EEG features. This notebook achieves a Cross-Validation (CV) score of 0.91 and a Leaderboard (LB) score of 0.66. As a benchmark, predicting train means yields CV 1.26 and LB 0.97, indicating that WaveNet is successfully learning relevant patterns in EEG signals to make predictions.

## Experiment Goals:
- Assess WaveNet's Ability to Predict Brain Events: By using just two EEG features, we aim to see how well WaveNet can capture temporal patterns in EEG data.
- Explore Feature Engineering and Model Adjustments:
    - Evaluate the impact of engineering additional EEG features on model performance.
    - Experiment with dual-input models that use both EEG waveforms and spectrograms for richer data representation.

## EEG Feature Details:
- Feature 1: Difference between the beginning and end of the montage chains LL and LP (Fp1 - O1).
- Feature 2: Difference between the beginning and end of the montage chains RL and RP (Fp2 - O2).

These features represent specific spatial differences in brain activity across key electrode placements, potentially revealing meaningful insights into event prediction.

![](https://raw.githubusercontent.com/cdeotte/Kaggle_Images/main/Jan-2024/montage.png)

