# Fresco_Classification
This repository showcases different implementations using CNN of style classification for frescoes from Pompeii, Italy. 
 The goal of this project, guided by proffesor ohad ben shahar is to develop accurate models that can classify frescoes into their respective artistic styles. The repository contains various architectures and approaches, along with a comparative analysis of their results.
we tried 3 different architecures and attitudes to solve this problem - 

# ResNet Transfer learning Architecture
ResNet (Residual Network) is a deep architecture designed to address the vanishing gradient problem in deep neural networks. The pre-trained ResNet18 architecture is employed with customized classifier layers to adapt to the style classification task.

The ResNet architecture demonstrates consistent improvement in validation loss and accuracy over epochs. However, there is room for further enhancement, particularly in recognizing certain styles such as Style 0 and Style 1. The architecture's capability to capture intricate features is evident, but it might require fine-tuning for optimal performance in this specific classification task.

# VGGNet Transfer learning Architecture
VGGNet, renowned for its depth and uniformity, is another chosen architecture. Transfer learning is employed, leveraging the pre-trained vgg16 model from PyTorch's models module.

The VGGNet architecture adapts well to the style classification task. The custom classifier layers and freezing of convolutional layers allow the model to effectively classify different styles. Adaptive average pooling ensures compatibility with variable input sizes. The architecture demonstrates competitive accuracy, particularly for Style 1, while also showing potential for improvement in recognizing Style 2.

# Combined Style Network
The Combined Style Network is a unique approach that leverages outputs from Binary Style Networks to classify fragments into the four identified styles, accounting for the complexities of the fourth style.

The Combined Style Network showcases the most promising results among the three architectures. The model's ability to combine features from different styles, particularly Style 2 and Style 3, aligns well with the historical understanding of the evolution of Pompeian art. The accuracy of the fourth style demonstrates the effectiveness of this approach, highlighting its potential for capturing complex features and transitions between styles.

# Conclusion
While all three architectures show merit, the Combined Style Network demonstrates the highest improvement and accuracy. This approach's ability to blend features aligns with the historical context and unique attributes of Pompeian art styles. Further refinements and optimizations could potentially enhance the accuracy and robustness of the model's performance across all styles.
