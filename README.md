# Experimental performance records

## Params
**Pre-trained weights**: imagenet - resnet50<br>
**Input shape**: (224, 224, 3)<br>
**Encoder trainable**: False<br>
**Batch size**: 32<br>
**Epochs**: 150

## Model
**Input Image (224, 224, 3)** → resnet50 (224, 224, 32) → **Result (4)**

**Total params**: 49,725,436<br>
**Trainable params**: 40,912,012<br>
**Non-trainable params**: 8,813,424<br>

## Dataset

- [Medial Images for Gastric Cancer Diagnosis (Korean)](https://aihub.or.kr/aidata/33988)

### Preprocessing

- [Preprocessors](https://github.com/Basars/preprocessors)

1. Remove malformed images from entire dataset.
2. Fill missing polygons from label data using [CVAT](https://github.com/openvinotoolkit/cvat).
3. Exports its ROI, binary masks and transformed original images.
4. Select pixel from binary masks.

## Compile options

### Loss
- categorical_crossentropy

### Metrics
- categorical_accuracy

### Optimizer
- Adam

## Results


### Evaluation
