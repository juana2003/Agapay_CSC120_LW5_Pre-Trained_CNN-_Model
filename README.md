[Gdrive google collab link] (https://colab.research.google.com/drive/1ONjwU2jk9FORK5_uRhDICddaJxSjyhJO?usp=sharing)

PART 12: Performance Comparison Table

| Model            | Train Accuracy | Train Loss | Validation Accuracy | Validation Loss |
|------------------|----------------|-------------|---------------------|-----------------|
| MobileNetV2      | 0.7160         | 0.9841      | 0.7616              | 0.8369          |
| InceptionV3      | 0.6911         | 1.0337      | 0.7525              | 0.9228          |
| DenseNet121      | 0.6409         | 1.2335      | 0.7374              | 1.0096          |
| Xception         | 0.6929         | 1.0593      | 0.7354              | 1.0086          |
| NASNetMobile     | 0.6112         | 1.3417      | 0.6791              | 1.2095          |
| VGG16            | 0.3194         | 2.3316      | 0.4738              | 2.2236          |
| ResNet101        | 0.1201         | 2.8444      | 0.1439              | 2.8110          |
| ResNet50         | 0.1096         | 2.8828      | 0.1388              | 2.8522          |
| EfficientNetB3   | 0.0540         | 2.9876      | 0.0533              | 2.9807          |
| EfficientNetB0   | 0.0553         | 2.9957      | 0.0342              | 2.9960          |
```
PART 13: GitHub Submission

A. Model Performance

1. Which pre-trained model achieved the highest accuracy? Why?
(To be filled after code execution) The model with the highest validation accuracy is MobileNetV2 with 0.7610.
The why usually depends on the architecture's ability to extract relevant features for the given dataset. MobileNetV2 performs well because it is efficient, lightweight, and still powerful enough to capture important image features without overfitting or being too complex for the dataset.

2. Which model had the lowest performance? What could be the reason?
(To be filled after code execution) The model with the lowest validation accuracy is EfficientNetB0 with 0.0342.
Possible reasons include: the model not being well-suited for the dataset, insufficient fine-tuning, or inability to extract strong discriminative features compared to other models.

3. How did loss values compare across models?
(To be filled after code execution) Loss values generally correlate inversely with accuracy. MobileNetV2 had the lowest loss of 0.8369, while EfficientNetB0 had the highest loss of 2.9960.

B. Evaluation Metrics

4. Why is accuracy not enough to evaluate a model?
Accuracy alone is not sufficient because it can be misleading in imbalanced datasets. A model may perform well on majority classes while ignoring minority classes. Precision, Recall, and F1-score provide a better evaluation.

5. Which model had the best F1-score? What does it indicate?
(To be filled after code execution) MobileNetV2 achieved the best macro average F1-score of 0.72, indicating a good balance between precision and recall.

6. How did Precision and Recall differ across models?
Precision measures correctness of positive predictions, while Recall measures how many actual positives are correctly identified. MobileNetV2 performs well in some classes but weaker in others, while ResNet50 and EfficientNetB0 show consistently low performance.

C. Confusion Matrix Analysis

7. Which classes were frequently misclassified?
This cannot be determined without analyzing the confusion matrices.

8. What patterns did you observe in the confusion matrix?
Patterns cannot be fully determined without visualization, but commonly include confusion between similar classes.

D. ROC and AUC

9. Which model had the highest AUC score?
This cannot be determined without running ROC-AUC evaluation.

10. What does AUC tell us about model performance?
AUC measures how well the model separates classes. Higher values (closer to 1.0) indicate better performance.

E. Explainability (Grad-CAM)

11. What did Grad-CAM reveal about model decision-making?
Grad-CAM shows which parts of an image influenced the model’s prediction, such as focusing on the object rather than the background.

12. Did the model focus on relevant image regions?
Yes, based on available heatmaps, the model focuses on meaningful regions relevant to classification.

13. Which model produced the most meaningful heatmaps?
This cannot be determined because Grad-CAM outputs were not compared across models.

F. Model Comparison & Improvement

14. Which model would you recommend for deployment? Why?
MobileNetV2 is recommended due to its highest accuracy (0.7616), lowest loss (0.8369), and strong generalization performance.

15. How can you further improve your best-performing model?

Fine-tune more layers
Improve data augmentation
Hyperparameter tuning
Use ensemble methods
Increase dataset size
Apply regularization techniques

G. Real-World Application

16. How can your model be applied in real-world scenarios?
It can be used in agriculture, plant classification, environmental monitoring, product recognition, and quality control systems.

17. What are the risks of deploying an inaccurate model?
Risks include incorrect predictions, loss of trust, financial losses, ethical concerns, and reputational damage.

18. How can this system be integrated into a mobile/web app?
By exporting the model, building a backend API, creating a frontend interface, deploying on the cloud, and optionally using on-device inference with TensorFlow Lite.
