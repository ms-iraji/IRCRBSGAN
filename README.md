# individual-relational consistency for bad semi-supervised generative adversarial networks (IRC-BSGAN)

This repository contains the implementation of the individual-relational consistency for bad semi-supervised generative adversarial networks (IRC-BSGAN). The IRC-BSGAN algorithm aims to improve the performance of semi-supervised learning by addressing issues such as incorrect decision boundaries and wrong pseudo-labels for unlabeled images.

## Table of Contents
- [Introduction](#introduction)
- [Authors](#authors)
- [Abstract](#abstract)
- [Key Features](#key-features)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Semi-supervised learning tackles the limitations posed by a scarcity of labeled images by
leveraging both labeled and unlabeled data. However, this approach presents challenges, such as
determining appropriate pseudo-labeling thresholds, effectively utilizing low-confidence
unlabeled images, lacking consistency regularization, and overlooking relationships among
images in low-density areas. The proposed method, IRC-BSGAN addresses these challenges by
introducing novel individual and relational consistency regularization losses on bad fake images
in low-density areas. It generates informative images that accurately estimate the decision
boundary of the classifier, ensuring diverse and stable labeling of the bad fake images through
consistency mechanisms. IRC-BSGAN particularly focuses on low-density areas, uncovering
additional semantic information by promoting local consistency and encouraging consistency
among the images. Its effectiveness lies in improving pseudo-labeling, especially for lowconfidence unlabeled images.
## Authors

- Mohammad Saber Iraji (iraji.ms@gmail.com)
- Jafar Tanha (Corresponding author: tanha@tabrizu.ac.ir, jafar.tanha.pnu@gmail.com)
- Mohammad-Ali Balafar
- Mohammad-Reza Feizi-Derakhshi

This work was conducted by researchers from the Department of Computer Engineering, Faculty of Electrical and Computer Engineering, University of Tabriz, Tabriz, Iran.

## Abstract

Semi-supervised learning leverages both labeled and unlabeled images for model training, addressing the scarcity of labeled data. However, challenges persist, including the determination of appropriate thresholds for pseudo-labeling, the effective utilization of uncertain unlabeled images, the absence of consistency regularization, and the oversight of inter-image relationships among images in low-density areas. This study introduces a novel approach named the Individual-Relational Consistency for Bad Semi-supervised Generative Adversarial Networks (IRC-BSGAN) to tackle these issues. IRC-BSGAN integrates bad adversarial training, consistency regularization, and pseudo-labeling to reduce error rates and enhance classifier performance. It includes various components, such as a bad generator network, a discriminator network, a classifier, and consistency regularization modules. IRC-BSGAN introduces new individual and relational consistency regularization losses on bad fake images in low-density areas, thereby generating informative images that precisely estimate the classifier's decision boundary. The proposed method ensures diversity and consistent labeling of bad fake images by integrating consistency mechanisms. It particularly focuses on low-density areas and extracts extra semantic details from these images by promoting local consistency and coherence among them. The effectiveness of IRC-BSGAN is realized by improving the pseudo-labeling of unlabeled images, especially for low-confidence unlabeled images. For the SVHN dataset with 1000 labeled training images and the CIFAR-10 dataset with 4000 labeled training images, the error rate reduced from 3.89 to 3.67 and from 7.29 to 6.17, respectively. Similarly, on the CINIC-10 dataset with 1000 labeled training images per class, IRC-BSGAN achieved a reduction in error rate from 19.38 to 15.45. On the COVID-19 dataset with 30 labeled training images, the error rate decreased from 7.41 to 5.55.

##The key contributions of our work are as follows:

1-	We present a novel semi-supervised model featuring a bad generator, integrating individual and relational consistency regularization between latent data and bad fake images in low-density regions.

2-	We introduce novel individual consistency regularization losses on bad fake images to improve their generation and accurately predict pseudo-labels for low-confidence unlabeled images.

3-	We propose novel (inversed) relational consistency regularization losses operating on the latent vectors of bad fake images in low-density areas. This regularization technique aims to improve coherence and consistency within the latent space and the bad generated images.


## Key Features
-Semi-supervised classification
-informative fake images 
-low-confidence images 
-individual consistency regularization
-relational consistency regularization

## Installation and Usage

To use the IRC-BSGAN algorithm, follow these steps:

1. Clone this repository to your local machine.
2. Install the required dependencies by running `pip install -r requirements.txt`.
3. Configure the training parameters and dataset paths in the provided configuration file.
4. Run `IRC-BSGAN.py`.


## Results

The CRBSGAN algorithm has been evaluated on several benchmark datasets, including SVHN, CIFAR-10, COVID-19, and CINIC-10. The experimental results demonstrate its effectiveness in reducing error rates compared to state-of-the-art methods. For detailed results, please refer to the [Results](#results) section in the paper.


## Contributing

Contributions to this project are welcome. If you have any suggestions, improvements, or bug fixes, please submit a pull request or open an issue on the GitHub repository.

## License

This project is licensed under the [MIT License](LICENSE).
