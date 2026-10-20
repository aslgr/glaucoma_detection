# Glaucoma Detection

A computer vision project focused on detecting glaucoma from retinal fundus images through a comparative study of **classical image processing, machine learning, and deep learning techniques**.

The project explores how handcrafted image features compare with representations learned by neural networks, investigating their performance in automated glaucoma classification.

## Dataset

This project uses the [RIM-ONE DL](https://github.com/miag-ull/rim-one-dl) dataset, containing **485 retinal fundus images** classified as normal or glaucomatous.

| Class | Training | Test | Total |
|---|---:|---:|---:|
| Normal | 219 | 94 | 313 |
| Glaucoma | 120 | 52 | 172 |
| **Total** | **339** | **146** | **485** |

The original random training/test partition is preserved. Dataset files are downloaded separately and are not included in this repository.

## Exploratory Data Analysis

The initial exploration is documented in [01_data_exploration.ipynb](notebooks/01_data_exploration.ipynb).

The analysis covers:

- **Class distribution:** examining dataset composition and class imbalance.
- **Image representation:** investigating pixel values, NumPy arrays, and RGB channels.
- **Intensity analysis:** comparing channel histograms, global intensity variation, and neighboring pixel differences.
- **Image properties:** analyzing resolutions, color modes, and file formats.
- **Visual inspection:** identifying variations in illumination, coloration, and anatomical appearance.
- **Data integrity:** checking image readability and exact file duplicates using SHA-256.

### Initial Findings

- All 485 images are square, RGB, and stored in PNG format, with resolutions ranging from 274 × 274 to 793 × 793 pixels.
- The dataset exhibits moderate class imbalance, with approximately 35.5% glaucomatous images.
- In the inspected sample, the green channel visually enhanced certain retinal structures, despite the red channel exhibiting greater global intensity variation.
- Global intensity statistics alone were insufficient to explain differences in anatomical visibility, highlighting the importance of spatial information.
- No corrupted images or byte-identical duplicate files were detected.

## Next Steps

- [x] Exploratory Data Analysis
- [ ] Image preprocessing and enhancement
- [ ] Feature extraction and classical machine learning
- [ ] Deep learning models
- [ ] Performance evaluation and comparison

## Technologies

**Python** · NumPy · Pandas · Matplotlib · Pillow · OpenCV · Scikit-learn · PyTorch (planned)

---

*This project is intended for research and educational purposes, not clinical diagnosis.*