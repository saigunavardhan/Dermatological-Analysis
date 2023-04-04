# SCED - Skin Cancer Early Diagnosis System

## Overview

This work proposes an integrated approach: SCED - Skin Cancer Early Diagnosis system. The proposed work is three-fold. First, to investigate the state-of-art classification architectures such as EfficientNet integration with CNN, INN and heuristic search based optimal parameter search. Second, to design an optimal architecture to not only classify the disease type, also perform early disease diagnosis with growth estimation computation application. Third, to provide a severity estimation from multi- criteria-based decision modelling and expert systems. Significantly, with the proposed approach SCED, the proposed heuristic search Involution block achieved 84.7% test accuracy. Further, the EfficientNet model is explored with CNN and a novel architecture is proposed with Involution blocks. Notably, the investigated INN architecture not only reduces overall parameters by 28.6% but also reduces overall training time by 45% per epoch. On other hand, novel EfficientNet-INN provided 93.71% test accuracy and 95.99% for EfficientNet-B0, reducing overall learning parameters during training by 92.59% which is essential for any real-time deployment and validation.

## Proposed Work

![Alt Text](https://user-images.githubusercontent.com/94104558/229706031-ce231f89-18b1-4a25-adcb-a47719ea3c0e.jpg)<br>
The input image is considered, followed with application of image processing and analysis for the calculation of area of the affected region and with the help of deep learning model (the proposed novel EfficientNet-INN architecture), the image is classified into one of two categories – malignant or benign, as a probability factor. Along with this, the pigmentation of the affection region is considered. Once all three factors are available, SCED model will make a calculation to estimate the severity of the condition, and thereby help in early diagnosis.

Worked on by: <a href="https://github.com/dawnorak">Sathi Vaigarai</a>, <a href="https://github.com/saigunavardhan">Sai Gunavardhan</a> and <a href="https://github.com/varunnaidu1802">K Varun Teja</a>.

Dataset used for the execution of the models was obtained from <a href="https://www.kaggle.com/datasets/fanconic/skin-cancer-malignant-vs-benign/">Kaggle</a>.
