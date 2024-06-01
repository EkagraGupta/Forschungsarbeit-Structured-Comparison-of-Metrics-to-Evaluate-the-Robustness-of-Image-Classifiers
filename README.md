# Structured Comparison of Metrics to Evaluate the Robustness of Image Classification Models

## Abstract
This research evaluates the robustness of image classification models against adversarial attacks using two metrics: Adversarial Distance and CLEVER. The study uses variants of the WideResNet model trained on the CIFAR-10 dataset, including a standard and a corruption-trained robust model. Key findings include:

- __Adversarial Distance Metric__: Provides an upper-bound approximation of perturbations.
- __CLEVER Metric__: Offers a lower-bound estimation of perturbations.
The corruption-trained robust model exhibits greater resilience against adversarial examples compared to the standard model.

## Introduction
Advancements in deep learning have highlighted vulnerabilities in image classifiers to adversarial attacks. This project focuses on a systematic comparison of robustness metrics using the WideResNet architecture.

## Methodology
- __Dataset__: CIFAR-10
- __Models__: Standard WideResNet and corruption-trained WideResNet
- __Metrics__: Adversarial Distance (L∞ norm) and CLEVER score
- __Tools__: PyTorch and CleverHans library for implementing attacks and measuring robustness.

## Results

![Alt text](/result.png)

Using the CIFAR-10 test dataset as a benchmark, the metrics consistently proved effective. Notably, the CLEVER Score was smaller than the Adversarial Distance metric for approximately 86% of the images, serving as the lower boundary for perturbation magnitude in projected gradient attacks, while the Adversarial Distance metric established itself as the upper bound. Interestingly, the behavior of corruption-trained robust models deviates slightly from the standard model when faced with adversarial examples, indicating a higher degree of resilience in the robust models. The robust model showed a cleaner scatter plot of distances and scores, with adversarial distances aligning closely with CLEVER scores compared to the standard model. These findings advance our understanding of model behavior in adversarial scenarios, emphasizing the importance of the proposed metrics in evaluating and assessing model robustness. The study highlights that while the CLEVER score does not universally act as a lower bound, it does so for around 86% of images, making it relevant for assessing perturbation magnitude in adversarial attacks for both model variants. Simultaneously, the Adversarial Distance metric functions as the upper bound, revealing unexpected alignment in behavior between corruption-trained robust models and the standard model in response to adversarial examples. This research enhances our comprehension of model dynamics in adversarial contexts and underscores the significance of the proposed metrics in quantifying and evaluating model robustness.