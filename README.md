# SSAM-Net Wood Mold HSI Dataset

This repository contains the pixel-level visible–near-infrared hyperspectral datasets used in the following study:

> **Innovative convolutional neural networks and high-quality hyperspectral datasets for non-destructive detection of early mold in wood**

## Files

- `SSAMNet_WoodMold_HSI_CalibrationSet.xlsx`  
  Calibration dataset used for model training and five-fold cross-validation.

- `SSAMNet_WoodMold_HSI_TestSet.xlsx`  
  Fixed pixel-level hold-out test dataset used for final model evaluation.

## Dataset description

The dataset contains pixel-level hyperspectral reflectance spectra collected from three wood species:

- *Cunninghamia lanceolata*
- *Pinus massoniana*
- *Ulmus pumila*

The spectra were classified into three mold-severity classes:

- No growth
- Mild growth
- Severe growth

Each row represents one individual-pixel spectrum. The first column is `label`, followed by the hyperspectral reflectance values.

The complete dataset contains 108,000 pixel spectra:

| Subset | Number of spectra |
|---|---:|
| Calibration set | 86,400 |
| Pixel-level hold-out test set | 21,600 |

## Label mapping

| Label | Wood species | Mold-severity class |
|---:|---|---|
| 0 | *Cunninghamia lanceolata* | No growth |
| 1 | *Cunninghamia lanceolata* | Mild growth |
| 2 | *Cunninghamia lanceolata* | Severe growth |
| 3 | *Pinus massoniana* | No growth |
| 4 | *Pinus massoniana* | Mild growth |
| 5 | *Pinus massoniana* | Severe growth |
| 6 | *Ulmus pumila* | No growth |
| 7 | *Ulmus pumila* | Mild growth |
| 8 | *Ulmus pumila* | Severe growth |

## Dataset partitioning

Each wood-species dataset was divided independently at the individual pixel-record level into an 80% calibration subset and a 20% hold-out test subset using stratified random sampling by mold-severity class with a fixed random seed of 42. The resulting species-specific calibration subsets and test subsets were then concatenated to create the released calibration and test files.


