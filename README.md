Project 3: Jailbreaking Deep Models (Tasks 1–5)

Overview

This deep learning project explores the robustness of pretrained image classification models under adversarial attacks. We evaluate and compare two models: ResNet-34 and DenseNet-121 across clean and adversarial settings using the ImageNet-1K subset.

The notebook is divided into five key tasks:

- Baseline Evaluation on Clean Data

- FGSM Attack (Fast Gradient Sign Method)

- I-FGSM Attack (Iterative FGSM)

- Patch Attack

- Transferability Analysis on DenseNet-121

Models Used

- ResNet-34: Pretrained on ImageNet-1K

- DenseNet-121: Pretrained on ImageNet-1K

Metrics Evaluated

- Top-1 Accuracy

- Top-5 Accuracy

- Attack Success Rate (ASR)

Transferability Study

Task 5 investigates how adversarial examples crafted for ResNet-34 affect DenseNet-121, measuring cross-model transferability.

Dataset

Subset of ImageNet-1K (100 classes × 5 images = 500 total samples)

Images are normalized using ImageNet mean and std. Folder structure follows PyTorch's ImageFolder format.

How to Run

Upload TestDataSet.zip and labels_list.json when prompted.

Run all cells in sequence. Ensure that a GPU runtime is enabled for faster evaluation.

Observations

- ResNet-34 shows higher top-1 accuracy on clean data, but DenseNet-121 achieves better top-5 results.

- FGSM reduces top-1 accuracy by ~30% for both models.

- I-FGSM and Patch attacks are more effective than FGSM.

- DenseNet demonstrates greater resilience in top-5 under adversarial conditions.

- Transferability results reveal DenseNet-121 is also vulnerable to attacks crafted on ResNet-34.
