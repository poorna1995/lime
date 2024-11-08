## Project Overview

This project uses LIME (Local Interpretable Model-Agnostic Explanations) to explain how a text classification model makes predictions. The goal is to help people understand why the model predicted a certain result for a specific text.

### Why LIME?
Before we dive into LIME, it's important to understand Explainable AI **(XAI)**.

XAI is a set of techniques that helps us understand how machine learning models make decisions. This is especially important for complex models that are hard to interpret, like deep learning models, which are often viewed as "black boxes."

![XAI](https://github.com/user-attachments/assets/232f5f4f-db73-4ce7-879e-67060b3a6710)

### XAI Methods Categorization

- **Agnostic**: Does the explanation method work with any machine learning model or is it specific to a type of model?
- **Data Type**: What types of data does the method apply to (e.g., text, images, tabular data)?
- **Scope**: Does the method explain the model locally (individual predictions) or globally (overall model behavior)?
- **Explanation Type**: What form do the explanations take? Are they visual, textual, or numeric?

### Agnosticity:

**Model Agnostic Methods**: These methods are not tied to any specific model and can be applied to a wide range of machine learning models. Examples include:
- LIME
- SHAP
- Partial Dependence Plots (PDPs)

#### What is LIME?
- **Local**: LIME creates a localized neighborhood around each instance to generate explanations specific to that instance.
- **Interpretable**: The explanations are designed to be easily understandable by humans.
- **Model-Agnostic**: LIME can be applied to any model, regardless of its underlying structure.
- **Explanations**: LIME provides insights that help in understanding model behavior and interpreting predictions.

### Text Classification:

LIME is useful for explaining classification models. For example, when a model is classifying text as "sincere" or "insincere," LIME can show which words in the message were most important for the model’s decision.

#### Example of LIME in Text Classification:
For a message, LIME might show that words like "thanks" and "appreciate" were the most important for the model to classify the message as "sincere."

![Example of Text Classification](https://github.com/user-attachments/assets/fcbf3b5b-89da-4ddc-b678-8a59a7185e94)
![Example Image](https://github.com/user-attachments/assets/40f093e3-3175-472a-8e50-2bc400837ac1)

### Limitation of LIME:

- **Local vs. Global Interpretability**: LIME explains individual predictions but doesn’t provide insights into the overall model behavior.
- **Linear Assumption**: LIME uses a linear model to approximate complex decision boundaries, which can oversimplify the model's true behavior.
- **Stability and Consistency**: Random sampling can lead to different explanations for the same input, making results less reliable.
- **Sampling Bias**: LIME’s synthetic data may not reflect real-world distributions, leading to biased or misleading explanations.

This project is based on the reference from the paper [Link](https://arxiv.org/abs/1602.04938).
