# SCED - Skin Cancer Early Diagnosis System

The published version of this work can be found <a href="https://ieeexplore.ieee.org/document/10112364">here</a> in IEEE Explore.

## Overview

This work proposes an integrated approach: SCED - Skin Cancer Early Diagnosis system. The proposed work is three-fold. First, to investigate the state-of-art classification architectures such as EfficientNet integration with CNN, INN and heuristic search based optimal parameter search. Second, to design an optimal architecture to not only classify the disease type, also perform early disease diagnosis with growth estimation computation application. Third, to provide a severity estimation from multi- criteria-based decision modelling and expert systems. Significantly, with the proposed approach SCED, the proposed heuristic search Involution block achieved 84.7% test accuracy. Further, the EfficientNet model is explored with CNN and a novel architecture is proposed with Involution blocks. Notably, the investigated INN architecture not only reduces overall parameters by 28.6% but also reduces overall training time by 45% per epoch. On other hand, novel EfficientNet-INN provided 93.71% test accuracy and 95.99% for EfficientNet-B0, reducing overall learning parameters during training by 92.59% which is essential for any real-time deployment and validation.

## Proposed Work

<div style="text-align:center">
  <img src="https://user-images.githubusercontent.com/94104558/229706031-ce231f89-18b1-4a25-adcb-a47719ea3c0e.jpg" alt="Image" />
</div>
<em>Proposed SCED Integrated Approach</em>
<br>
<br>
The input image is considered, followed with application of image processing and analysis for the calculation of area of the affected region and with the help of deep learning model (the proposed novel EfficientNet-INN architecture), the image is classified into one of two categories – malignant or benign, as a probability factor. Along with this, the pigmentation of the affection region is considered. Once all three factors are available, SCED model will make a calculation to estimate the severity of the condition, and thereby help in early diagnosis.

### Methodology

Notably, the optimal hyper-parameter search for efficient design and improved generalization of the CNN, INN, EfficientNet-INN models are investigated. Further, these deep learning models are evaluated on the current dataset. The 2D-CNN is used as a feature extractor, image classifier, category predictor, and spread calculator for skin cancer images. After user inputting image, it is fed layer by layer to be learned by model deeply and thereby extract features from the image at various levels of granularity. However, the observed limitation of this model is it being spatial agnostic and channel specific which may result in the non-recognition of some patterns in the image.  The custom CNN model is implemented, further investigating the impact of various activation functions, number and depth of filters, layers in 2D-CNN.

The Involution Neural Network (INN) is implemented to achieve maximum test accuracy with fewer parameters, and since it is spatial-specific and channel-agnostic, it can adapt to various visual patterns in an image. Consequently, 2D-INN layers have been used in place of 2D-CNN layers, and the implementation was done after investigating the effects of changes in various hyper-parameters. The proposed 2D-INN model is investigated to analyze the impact of various activation functions, number and depth of filters, variations in convolution layers in 2D-INN for optimal design of deeper architectures and deployments.

Additionally, an EfficientNet model, a predetermined number of layers and channels and provides a good accuracy in a principled manner is explored. However, the original model still has an observed limitations in terms of more learnable parameters resulting in complex operations and increased time. Hence, in this work, an integration of INN with EfficientNet has been proposed to make EfficientNet more efficient, optimal. Improved generalization for real-time. Importantly, integration of both results in a higher model quality level combining the best features of INN (channel-agnostic operation) and EfficientNet (layered Inverted and Squeeze Excitation blocks). The resultant model is expected to be on par with traditional EfficientNet’s accuracy levels while decreasing trainable parameters by a huge extent while also decreasing computational time. Utilizing an effective network architecture CNN, but with a predetermined number of and channels. Combining INN's best features with EfficientNet design to increase accuracy.

## Results
The EfficientNet-B0 is implemented, and it achieved an average accuracy of 95.98%, with trainable parameters of 14,037,118, and an execution time of 3,060 seconds (for 100 epochs). However, the trainable parameters are high which is not suitable for real-time deployments. Hence, a new model EfficientNet with a 3-layered INN (i3) is proposed, implemented, and achieved an improved accuracy of 93.70%, with less trainable parameters of 1,039,758 and an execution time of 2770 seconds (for 100 epochs).

![Alt Text](https://user-images.githubusercontent.com/94104558/229709934-e2d1925a-273e-4d55-a2dd-97b41058c9f4.jpg "Accuracy Plots for Various Models")
![Alt Text](https://user-images.githubusercontent.com/94104558/229710284-1f41f4e6-80c6-47c4-a9ab-23e09d7eda39.jpg "Loss Plots for Various Models")

## Conclusion
The proposed work focuses on designing an AI enabled system for SGD-3, health and well-being. Notably, in the investigation analysis, the CNN model shows some good results with activation function ReLU and optimizer SGD (Stochastic gradient descent) with peak test accuracy of 97.57% and test loss of 0.16, although it showed immense bias. To address this challenge, INN - a channel agnostic model is examined, and achieves the test accuracy 84.1% and test loss of 0.445. Subsequently, the EfficientNet B0 with CNN, showed an accuracy of 95.98 % compared to CNN, and has lesser parameters and execution time. In comparison to INN, EfficientNet B0 with lesser parameters gave more accuracy than CNN and INN which also shows it as a better model than INN and CNN. However, there is still a scope to work on optimization. Hence, a novel EfficientNet with 3-layered INN (i3) is proposed and it achieved 97.62% test accuracy while decreasing trainable overall parameters by 92.59% and execution time by 9.48% per epoch which shows a huge significance. Further, as part of decision modelling the multi-criterion-based severity estimation is carried out which not only helps in early and precise diagnosis, but also provides the spread severity recommendation. As a next step and possible extension, the proposed work would be extended in a 2-fold manner. First, the models would be post-processed to deploy and validate various skin cancer types in real-time. Secondly, to explore the scope of quantum (Q-bits) initiated deeper design for light-weight models.



Worked on by: <a href="https://github.com/dawnorak">Sathi Vaigarai</a>, <a href="https://github.com/saigunavardhan">Sai Gunavardhan</a> and <a href="https://github.com/varunnaidu1802">K Varun Teja</a>.

Dataset used for the execution of the models was obtained from <a href="https://www.kaggle.com/datasets/fanconic/skin-cancer-malignant-vs-benign/">Kaggle</a>.
