# HybridNet Pretrained Models for Markerless 3D Toddler Posture Estimation

This repository provides pretrained HybridNet model weights for markerless 3D full-body posture estimation of toddlers from synchronized multi-view video recordings.

The current release contains pretrained weights derived from toddler home-recording data, intended to support fine-tuning on new multi-view datasets.

---

## Included Model Set

### Toddlers_At_Home

Pretrained weights derived from a multi-view toddler home-recording dataset.

#### Dataset summary
- 4 toddlers
- 3 synchronized cameras
- ~15-minute free-play recordings per child
- 2000 annotated framesets in total
- 500 annotated framesets per toddler
- 22 body keypoints per frameset
- 1600 framesets used for model training
- 400 framesets held out for evaluation

#### Body keypoints

The following 22 anatomical keypoints were annotated:

- Nose
- Top of sternum
- Left eye, Right eye
- Left ear, Right ear
- Left shoulder, Right shoulder
- Left elbow, Right elbow
- Left wrist, Right wrist
- Left hip, Right hip
- Left knee, Right knee
- Left ankle, Right ankle
- Left heel, Right heel
- Left big toe, Right big toe

Keypoints were annotated in all camera views. Only visible keypoints (i.e., not subject to occlusion) were annotated.

#### Files
- `HybridNet-medium.pth`
- `EfficientTrack_Keypoints-medium.pth`
- `EfficientTrack_Center-medium.pth`

---

## Repository Structure

```text
hybridnet-pretrained-models-toddlers/
├── pretraining-sets/
│   └── Toddlers_At_Home/
│       ├── HybridNet-medium.pth
│       ├── EfficientTrack_Keypoints-medium.pth
│       └── EfficientTrack_Center-medium.pth
├── contributing/
│   └── how-do-I-contribute.md
└── README.md
```
---

## Purpose of This Repository

HybridNet is a Convolutional Neural Network architecture, but training it from scratch requires many annotated framesets. These toddler-specific pretrained models:

* Reduce training time and the number of frames needed
* Improve accuracy when fine-tuning on new child datasets
* Facilitate reproducible and comparable use of markerless 3D posture estimation in developmental research

---

## How to Use These Pretrained Models

1. **Download the three `.pth` files** from the `pretraining-set/Lab_Toddlers` folder.
2. **Place them inside the `pretrained` folder of your HYBRIDNet directory**, for example:

```
your-project/
└── JARVIS-HYBRIDNet/
    └── pretrained/
        ├── HybridNet-medium.pth
        ├── EfficientTrack_Keypoints-medium.pth
        └── EfficientTrack_Center-medium.pth
```

3. When running HYBRIDNet training through the JARVIS toolkit, set `pretrained = True` in the configuration.
4. Fine-tune the network on your own annotated frames.

---

## Contributing Your Fine-Tuned Model

To help improve the generalizability of the toddler HybridNet model:

1. Fine-tune the model on your dataset.
2. Export the updated `.pth` files.
3. Open a pull request including:

   * The updated model files
   * A short description of your dataset (e.g., number of frames, age group, environment)
   * Any observed improvements or limitations

This helps the model become increasingly robust across different labs, home environments, camera arrangements, and child movement styles.

---

## Citation

If you use these pretrained weights, please cite:

-This repository

-The official JARVIS Toolkit documentation.

-(Article references will be made public here upon publication)

---

## Notes

-The original video data are not shared due to privacy and ethical considerations.

-These models were trained on multi-view recordings of young children and may not generalize to adult datasets without additional fine-tuning.

-Additional pretrained model sets will be released in future updates.

## Acknowledgments

These models are based on the JARVIS Toolkit and the HybridNet architecture developed at the Radboud University Baby & Child Research Center. Thank you to the participating families and children who made this work possible.
