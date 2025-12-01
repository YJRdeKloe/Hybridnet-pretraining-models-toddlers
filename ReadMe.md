# Markerless 3D Posture Estimation Pipeline – HybridNet Pretraining Models

This repository provides pretrained HybridNet models for markerless 3D full-body posture estimation of toddlers, developed as part of a camera-based multi-view motion capture study. These pretrained weights allow researchers to fine-tune HybridNet more efficiently for their own datasets—especially datasets involving toddlers, or other populations that differ from standard adult training data.

The models in this repository were validated in:

**De Kloe, Y. J. R., Hunnius, S., & Stapel, J. S.**
*Markerless 3D Posture Estimation of Toddlers from Multi-View Video Recordings: Evaluating Accuracy, Precision, and Generalizability.* (Under review)

---

## Repository Structure

```
Hybridnet-pretraining-models-toddlers/
│
├── pretraining-set/
│   └── Lab_Toddlers/
│       ├── HybridNet-medium.pth
│       ├── EfficientTrack_Keypoints-medium.pth
│       └── EfficientTrack_Center-medium.pth
│
├── contributing/
│   └── how-do-I-contribute.md
│
└── README.md
```

---

## Purpose of This Repository

HybridNet is a powerful architecture, but training it from scratch requires many annotated frames. These toddler-specific pretrained models:

* Provide strong initial weights for child movement patterns
* Reduce training time and the number of frames needed
* Improve accuracy when fine-tuning on new child datasets
* Enable a community-driven improvement cycle: users can contribute their fine-tuned models back to help expand robustness across contexts

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

```
De Kloe, Y. J. R., Hunnius, S., & Stapel, J. S. (under review).
Markerless 3D Posture Estimation of Toddlers from Multi-View Video Recordings: Evaluating Accuracy, Precision, and Generalizability.
```

And the official JARVIS Toolkit documentation.

---

## Acknowledgments

These models are based on the JARVIS Toolkit and the HybridNet architecture developed at the Radboud University Baby & Child Research Center. Thank you to the participating families and children who made this work possible.
