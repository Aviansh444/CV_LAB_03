# CVision-LAB---03

## Computer Vision Lab – Experiment 3

### Title

**Mean Filtering using 3×3, 5×5 and 7×7 Filters**

---

## Aim

To implement **Mean Filtering** on a grayscale image using different filter sizes (3×3, 5×5, and 7×7) and observe their effect on image smoothing.

---

## Objective

The objective of this experiment is to understand the working of a Mean Filter and analyze how increasing the filter size affects the smoothness and details of an image.

---

## Technologies Used

- Python
- OpenCV
- NumPy
- Matplotlib
- Google Colab
- Jupyter Notebook

---

## Repository Contents

```text
CVision-LAB---03/
│
├── CV_LAB_3.ipynb
├── Mean_Filter_Output.png
└── README.md
```

| File | Description |
|---|---|
| `CV_LAB_3.ipynb` | Jupyter Notebook containing the Python implementation |
| `Mean_Filter_Output.png` | Output image showing the results of different mean filters |
| `README.md` | Documentation of the experiment |

---

## Theory

A **Mean Filter** is a spatial filtering technique used for image smoothing.

It replaces the value of each pixel with the average of the pixel values in its neighborhood.

The general formula is:

```text
Mean = Sum of neighboring pixel values / Number of neighboring pixels
```

### 3×3 Mean Filter

A 3×3 filter contains **9 pixels**:

```text
Mean = Sum of 9 pixels / 9
```

### 5×5 Mean Filter

A 5×5 filter contains **25 pixels**:

```text
Mean = Sum of 25 pixels / 25
```

### 7×7 Mean Filter

A 7×7 filter contains **49 pixels**:

```text
Mean = Sum of 49 pixels / 49
```

As the filter size increases, more neighboring pixels are considered, resulting in stronger smoothing.

---

## Methodology

The program performs the following steps:

1. Read the input image using OpenCV.
2. Convert the image from BGR to grayscale.
3. Create output arrays for 3×3, 5×5, and 7×7 filters.
4. Calculate the average of neighboring pixels using nested loops.
5. Generate the filtered images.
6. Display the original grayscale image and filtered images.
7. Save the combined output as `Mean_Filter_Output.png`.
8. Display the image dimensions.

---

## Implementation

The mean filters are implemented manually using nested loops.

### 3×3 Filter

For every pixel, the program considers a 3×3 neighborhood and calculates:

```python
total // 9
```

### 5×5 Filter

For every pixel, a 5×5 neighborhood is considered:

```python
total // 25
```

### 7×7 Filter

For every pixel, a 7×7 neighborhood is considered:

```python
total // 49
```

The use of `//` performs integer division to obtain the average pixel value.

---

## How to Run

### Google Colab

1. Open `CV_LAB_3.ipynb` in Google Colab.
2. Upload the required input image.
3. Update the image path if required.
4. Run all the cells.
5. The program generates `Mean_Filter_Output.png`.
6. Upload the generated output image to this GitHub repository.

### Required Libraries

```bash
pip install opencv-python numpy matplotlib
```

---

## Output

The output contains:

- Original grayscale image
- Mean Filter using 3×3 kernel
- Mean Filter using 5×5 kernel
- Mean Filter using 7×7 kernel

### Mean Filtering Results

![Mean Filter Output](Mean_Filter_Output.png)

---

## Observation

| Filter | Kernel Size | Smoothing Effect |
|---|---:|---|
| Mean Filter | 3×3 | Low smoothing |
| Mean Filter | 5×5 | Moderate smoothing |
| Mean Filter | 7×7 | High smoothing |

### 3×3 Filter

- Produces slight smoothing.
- Preserves more fine details.
- Removes a small amount of noise.

### 5×5 Filter

- Produces moderate smoothing.
- Removes more fine details.
- Image becomes noticeably smoother.

### 7×7 Filter

- Produces the strongest smoothing.
- Removes more fine details.
- Image becomes more blurred.

Overall, increasing the kernel size increases the smoothing effect but can result in loss of fine image details.

---

## Output Size

Since the program does not use padding, the output image becomes smaller depending on the filter size.

For an input image of size:

```text
rows × cols
```

the output dimensions are:

### 3×3

```text
(rows - 2) × (cols - 2)
```

### 5×5

```text
(rows - 4) × (cols - 4)
```

### 7×7

```text
(rows - 6) × (cols - 6)
```

---

## Mathematical Representation

For a kernel of size `K × K`:

```text
Mean = Sum of Pixel Values / K²
```

Therefore:

```text
3×3 → Mean = Sum / 9
```

```text
5×5 → Mean = Sum / 25
```

```text
7×7 → Mean = Sum / 49
```

---

## Effect of Kernel Size

```text
Kernel Size ↑
      ↓
Number of Neighboring Pixels ↑
      ↓
Smoothing Effect ↑
      ↓
Fine Details ↓
```

Therefore:

```text
3×3 → Less Smoothing
5×5 → Moderate Smoothing
7×7 → More Smoothing
```

---

## Conclusion

Mean Filtering was successfully implemented using **3×3, 5×5, and 7×7 kernels**.

The experiment demonstrates that increasing the kernel size increases the smoothing effect. However, larger filters can also remove fine image details.

The **3×3 filter** preserves more details, while the **5×5 filter** provides moderate smoothing. The **7×7 filter** provides the strongest smoothing but results in greater loss of fine details.

Thus, the choice of filter size depends on the required level of image smoothing and detail preservation.

---

## Author

**Aviansh042**

**Computer Vision Lab – Experiment 3**
