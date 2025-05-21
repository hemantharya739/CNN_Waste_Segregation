
# CNN Waste Classification Project

## Project Overview
This project demonstrates the application of Convolutional Neural Networks (CNNs) for automated waste classification. The model is trained to classify images into 7 distinct waste categories: Plastic, Glass, Metal, Paper, Cardboard, Organic, and Other. The goal is to assist in automated sorting and improve recycling efficiency.

## Dataset
The dataset used for this project consists of 1,525 labeled images across 7 waste categories. The images were preprocessed and split into training, validation, and test sets to ensure robust model evaluation.

## Model Architecture
The model architecture includes:
- Custom Convolutional Layers
- InceptionV3 base model (pre-trained on ImageNet)
- Additional custom layers on top of InceptionV3

### Layers:
1. **Input Layer**: (256, 256, 3)
2. **Custom Conv Layers**: 3 layers with Conv2D, BatchNormalization, MaxPooling2D, Dropout
3. **InceptionV3 Base Model**: Pre-trained on ImageNet, layers frozen
4. **Additional Conv Layers**: Conv2D, BatchNormalization, MaxPooling2D, Dropout
5. **GlobalAveragePooling2D**
6. **Dense Layers**: 1024 units, Dropout
7. **Output Layer**: 7 units (softmax activation)

## Training Results
The model was trained over 10 epochs with the following results:
- **Initial Accuracy (Epoch 1)**: 68.90% (Training), 82.36% (Validation)
- **Final Accuracy (Epoch 10)**: 88.10% (Training), 88.07% (Validation)
- **Final Loss**: 0.3362 (Training), 0.3535 (Validation)

## Evaluation
- **Test Accuracy**: 88.07%
- **Test Loss**: 0.3535

## Sample Predictions
The model confidently classified several test images:
- `hero1.jpg` → **Glass** (97.34%)
- `hero2.jpg` → **Metal** (73.93%)
- `hero3.jpg` → **Food_Waste** (97.13%)
- `charan.jpg` → **Other** (100.00%)

## Key Insights
- The model achieved strong performance with relatively few epochs, suggesting a well-prepared dataset and effective architecture.
- Classes like **Plastic**, **Glass**, and **Metal** were among the most confidently predicted.
- Further improvements could be achieved through additional data augmentation, fine-tuning the model, and addressing edge cases or ambiguous images.

## Conclusion
This project successfully demonstrates the application of deep learning for automated waste classification. The trained model can be integrated into real-world recycling systems to assist in automated sorting, thereby enhancing efficiency and promoting sustainability.
