# Mandarin Tone Classifier (Mel Spectrograms · CNN vs MLP)

Classifies Mandarin tones (1–4) from MP3 audio using Mel spectrograms.
The notebook trains **two models** (CNN and Feed-Forward) and compares them by **validation accuracy** and **average per-class recall**.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/<YOUR_GH_USER>/<REPO_NAME>/blob/main/tone_classifier.ipynb)

## Highlights
- MP3 → `torchaudio.load` → Mel Spectrogram (`n_mels=64` by default)
- Two baselines: **CNN** (conv blocks + GAP + Linear) and **MLP** (flatten + 2 Linear)
- Saves best checkpoints; plots loss/accuracy; builds confusion matrices
- Simple model comparison: **val accuracy** + **average recall**

## Quickstart
1. Open the notebook (link above) or clone locally.
2. Put audio under `content/tones/` (or edit the path in the first cell).
3. Run all cells. Artifacts (plots/CMs/checkpoints) are saved under `runs/<timestamp>/`.

## Results (example)
- CNN: accuracy = `0.XX`, avg recall = `0.XX`
- MLP: accuracy = `0.XX`, avg recall = `0.XX`
(Your numbers will vary with data.)

## Data
Dataset path is not included in the repo. Use your own MP3s or point to a public dataset.

## License
MIT © <Your Name>
