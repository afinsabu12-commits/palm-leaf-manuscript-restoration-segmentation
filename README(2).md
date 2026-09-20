# Palm-Leaf Manuscript Restoration and Writing Segmentation

## Digital Image Processing Mini Project

This project applies Digital Image Processing techniques to palm-leaf manuscript images for restoration/enhancement and manuscript-writing segmentation.

### Project Title

**Palm-Leaf Manuscript Restoration and Writing Segmentation Using Digital Image Processing**

### Dataset

- Number of images: 20
- Dataset: Student-provided palm-leaf manuscript image dataset
- Supported input formats: JPG, JPEG and PNG
- Execution environment: Python / Google Colab

### Objectives

1. Load and inspect palm-leaf manuscript images.
2. Convert manuscript images to grayscale.
3. Reduce noise using median filtering.
4. Correct uneven illumination.
5. Improve local contrast using CLAHE.
6. Segment manuscript writing using Otsu thresholding.
7. Compare Otsu and adaptive thresholding.
8. Improve the binary result using morphological operations.
9. Detect connected components.
10. Generate a final segmentation mask and overlay.
11. Save the processed outputs.

### Processing Pipeline

```text
Input Image
    ↓
Grayscale Conversion
    ↓
Median Filtering
    ↓
Illumination Correction
    ↓
CLAHE Contrast Enhancement
    ↓
Otsu Thresholding
    ↓
Adaptive Thresholding
    ↓
Morphological Opening and Closing
    ↓
Connected Component Analysis
    ↓
Final Segmentation Mask
    ↓
Segmentation Overlay
```

### Techniques Used

- **Grayscale Conversion:** Converts the input image into a single-channel intensity image.
- **Median Filtering:** Reduces small noise while preserving important edges.
- **Illumination Correction:** Uses a blurred background estimate and division-based correction to reduce uneven brightness.
- **CLAHE:** Improves local contrast and visibility of manuscript details.
- **Otsu Thresholding:** Automatically selects a global threshold for binary segmentation.
- **Adaptive Thresholding:** Computes local thresholds and can handle non-uniform illumination.
- **Morphological Opening and Closing:** Cleans small unwanted regions and improves the binary mask.
- **Connected Components:** Identifies separate foreground regions.

### Technologies

- Python
- OpenCV
- NumPy
- Matplotlib
- Google Colab

### Installation

```bash
pip install -r requirements.txt
```

### Run

For Google Colab, keep the dataset in:

```text
/content/data_set
```

and run:

```python
%run "source_code.py"
```

### Output

The program saves processed images in:

```text
results/
├── original.jpg
├── restored.jpg
├── segmentation_mask.jpg
└── segmentation_overlay.jpg
```

### Repository Structure

```text
palm-leaf-manuscript-restoration-segmentation/
│
├── README.md
├── source_code.py
├── requirements.txt
├── images/
├── screenshots/
├── results/
└── report/
```

### Limitations

- The supplied dataset contains 20 images.
- Manuscripts can contain faded characters, uneven backgrounds and physical damage.
- Thresholding results may depend on parameter selection.
- Ground-truth segmentation masks are not part of the supplied dataset, so numerical IoU/Dice evaluation requires manually created masks.
- The supplied source demonstrates the processing pipeline on a selected image; it can be extended to batch-process all 20 images.

### Future Scope

- Batch processing of all dataset images.
- Manual ground-truth mask creation and IoU/Dice evaluation.
- Improved restoration for heavily degraded manuscripts.
- OCR integration after segmentation.
- Deep-learning-based restoration and segmentation.
- Web or real-time deployment.

### Author

**Afin Sabu**  
BCA  
Marian College Kuttikanam Autonomous
