# Fresco_Classification
This repository showcases different implementations using CNN of style classification for frescoes from Pompeii, Italy. 
 The goal of this project, guided by proffesor ohad ben shahar is to develop accurate models that can classify frescoes into their respective artistic styles. The repository contains various architectures and approaches, along with a comparative analysis of their results.
we tried 3 different architecures and attitudes to solve this problem.

# Preview
At the end of the 19th century, August Mau divided Pompeian art into four categories, each representing the era from which they came and containing different visual features (Lorenz, 2015; Strocka, 2009). Each fresco is associated with only one style, hence the identification of the style of a fragment may constitute the first level of clustering. The first style (third–second centuries BC), called the ‘Structural’ or ‘Incrustation’ style (Lorenz, 2015; Strocka, 2009), is characterized by faux marble combined with other decorative elements depicted in bright colors. The second one (c.100–20 BC), called the "Illusionist" or “Architectural” style, includes architectural components such as ionic columns, doors, and windows, which give the 2D wall a 3D look, making the room look larger than it is, creating a kind of illusion for the viewer. The third style (c.20 BC–AD 40/50), called the “Ornamental style”, is simple and monochromatic and it is characterized by the disappearance of the illusionist elements in the second style. The fourth one (c.AD 40/50–79/100), called “Intricate style, “combines the three previous styles. It involves marble patterns evocating the first style and illusionary elements impacted by the second style. Something unique to the fourth style not found in the other styles is that the scenes are presented in a frame (The Roman Life Forum, 2018).

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
