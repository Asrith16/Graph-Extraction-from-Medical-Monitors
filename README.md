# Object Detection with Detectron2 and Open-Set Recognition (ORE)

This repository contains the implementation of a project that explores object detection using Detectron2 and integrates Open-Set Recognition (ORE) to identify unrecognized objects. The project utilizes a Detectron2 model pre-trained on the **COCO 2017** dataset to perform object detection across diverse object categories. It further extends this by marking unrecognized or misclassified objects as "unknown," allowing for iterative refinement and learning.

## Project Overview

The goal of this project was to leverage a powerful pre-trained object detection model, **Detectron2**, while introducing an adaptive approach that helps identify objects that the model fails to classify. By marking these objects as "unknown," we can later annotate them and retrain the model to improve its recognition accuracy over time.

### Key Steps:

1. **Detectron2 Model**: 
   - The project starts with Detectron2, trained on the **COCO 2017 dataset**, performing object detection on various images. The model accurately detects and classifies multiple objects like vehicles, animals, and household items.

2. **Unrecognized Object Identification**: 
   - After running the object detection model, the next step involves analyzing the detected objects. If any object is misclassified or cannot be identified with high confidence, it is labeled as "unknown." This step ensures that the system does not ignore or misinterpret potentially important objects.

3. **Focused Evaluation with Balloon Dataset**: 
   - A specialized balloon dataset is used to evaluate the model's capacity to adapt to new categories of objects. By testing the model’s ability to detect and classify balloons, we assess its performance on objects that were not previously recognized in the COCO dataset.

4. **Adaptive Learning and Annotation**: 
   - Once the "unknown" objects are identified, they are annotated and labeled as balloons. This process highlights the model's adaptability and its potential to continuously learn and expand its knowledge base to include new objects.

### Results

Through this iterative process, the model evolves to more accurately detect previously unrecognized objects and improves its object detection capabilities. By the end of the project, the model not only recognizes the objects initially found in the COCO dataset but also accurately identifies balloons, showing how it can be adapted for specific domains.

### Conclusion

This project demonstrates the power of combining **Detectron2** with **Open-Set Recognition** techniques to improve object detection beyond the pre-trained dataset. By marking and refining previously unrecognized objects, the model evolves, improving its detection accuracy and versatility in real-world scenarios.
