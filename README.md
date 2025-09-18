# comp3710-unet-oasis-seg

# COMP3710 — OASIS Brain MRI Segmentation with U-Net

This project trains a **U-Net** to segment preprocessed **OASIS** brain MRI slices.  
It provides a full pipeline in a single Colab notebook:

- ✅ Mount Drive & unzip dataset
- ✅ Build `OasisSegDataset` (images + segmentation masks)
- ✅ Define U-Net (skip connections; categorical output)
- ✅ Loss = 0.5 · CrossEntropy + 0.5 · Dice; metrics = Dice per class & mean
- ✅ Train with AMP + checkpoint the best model (val Dice)
- ✅ Evaluate on test set (per-class Dice + mean)
- ✅ Save 6 overlay examples (**Image | GT | Pred**)
- ✅ Export weights + metrics to Drive for submission
