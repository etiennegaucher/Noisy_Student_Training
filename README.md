# Implementation of the Noisy Student Training method on MNIST dataset #

This project aims to implement the Noisy Student Training method on MNIST dataset using PyTorch. Although all the 50 000 images of the MNIST training dataset have labels, we assume that only 100 of them are labeled and we treat the other ones as unlabeled images. When adding dropout and data augmentation during the training of the student model, Noisy Student Training improves the accuracy by over 10 %.

Noisy Student Training is a semi-supervised learning method that has 3 main steps:
1. train a teacher model on the labeled images and use it to generate pseudo labels for unlabeled images
2. train a noised student model on the combination of labeled and unlabeled images
3. iterate the process a few times by putting back the student as a teacher to generate new pseudo labels

During the training of the student, we inject noise such as dropout and data augmentation.

This folder contains the following files:
- Article.pdf: paper presenting the method, also available here: https://arxiv.org/pdf/1911.04252v4.pdf
- Noisy_Student_Training.ipynb: implementation of the method in Python using PyTorch
- Report.pdf: report of my work (in French)
- Slides.pdf: slides I used for my oral presentation (in French)
