# One Pixel Attack for Fooling Deep Neural Networks

This is a recreation of the [One Pixel Attack](https://arxiv.org/abs/1710.08864) paper. The paper proposed Differential Evolution (DE) as a tool to optimise the population into to solve multimodal problems. This was used to support the aim of the algorithm in influencing the model to change its predictions and misclassify an image after refined perturbations have been applied.

## Requirements
Install python on your computer: https://www.python.org/downloads/, this implementation uses **Python 3.14.4**.

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install required dependencies from the `requirements.txt` file.

```bash
pip install -r requirements.txt
```

## Features
- Custom perturbation counts
- Untargeted and targeted attacks
- 3 different models
- Visualise accuracies for each model

## How to use
- All you need to do is run the `code.ipynb` file
- The CIFAR-10 dataset will install and cache on your device
- It will then train each of the 3 models, producing a `.keras` file of each
- It will then select 500 images from the CIFAR-10 sample
- It will then compute accuracies of each models on the sample over perturbation counts
- It will then produce visualisations
    - bar charts
    - heat maps

## File Layout
```
📦project
 ┣ 📂plots           <- (generated) holds visualisations of accuracies from the models
 ┣ 📜code.ipynb      <- the file to be run
 ┣ 🧾*.keras         <- (generated) pre-trained models adapted tothe dataset
 ┣ 🧾*_results.txt   <- (generated) outputs of performance metrics across untargeted/targeted atacks
 ┗📙requirements.txt <- python dependencies
```

