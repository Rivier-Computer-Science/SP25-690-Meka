# Road Accident Detection Using Deep Learning from Traffic Camera Images

## Project Overview
This project detects road accidents from traffic camera images using deep learning. The task is binary image classification: Accident vs No Accident.

## Problem Statement
The goal is to classify a traffic image as either Accident or No Accident. This is useful because faster accident detection can help emergency response and traffic monitoring.

## Dataset
The dataset contains two folders:

- Accident
- No_Accident

The sample images are stored in:

```text
data/sample/Accident/
data/sample/No_Accident/
```

## Models Used

This project includes:

- Logistic Regression baseline
- Simple CNN
- ResNet-18 transfer learning model

## Evaluation Metrics

The model is evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

Recall and F1-score are important because missing an accident is risky.

## Project Structure

```text
data/sample/Accident/       accident images
data/sample/No_Accident/    no accident images
notebooks/                  Google Colab notebook
outputs/results/            metrics.csv
outputs/figures/            confusion matrix and loss curve
models/                     saved model
reports/                    final report
requirements.txt            dependencies
README.md                   project instructions
```

## How to Run

1. Open the notebook in Google Colab.
2. Upload the dataset folders.
3. Run all notebook cells.
4. Download the output files.
5. Upload results to GitHub under outputs.

## Output Files

The final output files are:

```text
outputs/results/metrics.csv
outputs/figures/confusion_matrix.png
outputs/figures/loss_curve.png
```

## Limitations

This quick version uses a small sample dataset. A stronger final version should use more images, compare Logistic Regression, CNN, and ResNet-18, and include failure analysis.
