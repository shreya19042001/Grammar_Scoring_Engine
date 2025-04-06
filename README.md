# Grammar Scoring Engine - SHL Research Intern Assignment

This repository contains a Jupyter Notebook for a **Grammar Scoring Engine** developed as part of the SHL Research Intern Assignment. The task is to evaluate spoken audio samples and assign a grammar proficiency score between 0 and 5 using machine learning techniques.

## 📁 Dataset
- `train.csv`, `test.csv`: Metadata files with filenames and scores.
- `audios_train/`, `audios_test/`: Folders containing `.wav` audio files for training and testing.

## 🔍 Approach
1. **Preprocessing**: Loaded audio data using `librosa`, handled sample rate consistency, and extracted relevant acoustic features.
2. **Feature Engineering**: Extracted MFCCs, chroma features, spectral contrast, zero crossing rate, and tonnetz.
3. **Modeling**: Trained a regression model to predict grammar scores from extracted features.
4. **Evaluation**: Used **Pearson Correlation** to evaluate performance.
5. **Submission**: Final predictions were clipped to [0, 5] and saved as `submit.csv`.

## 🧠 Tech Stack
- Python
- Jupyter Notebook
- librosa
- scikit-learn
- pandas
- numpy
- tqdm

## 📈 Metric
Performance is evaluated using **Pearson Correlation** between the predicted and true scores.

## 📊 Output
Generates a `submit.csv` file for leaderboard submission.

## 📎 Notes
- Make sure all `.wav` files are placed in the correct folders (`audios_train`, `audios_test`).
- The code uses `librosa`'s fallback (`audioread`) for files not supported by `soundfile`.

---

🛠️ **Made with care for SHL's Research Intern challenge.**

**Note:** Due to file size and privacy constraints, audio files and CSV datasets are not uploaded here. Please get in touch with me directly or use your local copies as shared in the assignment instructions.

