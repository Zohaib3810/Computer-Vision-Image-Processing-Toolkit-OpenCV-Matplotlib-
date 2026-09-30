# Computer Vision & Image Processing Toolkit (OpenCV & Matplotlib)

A comprehensive repository containing implementation, analysis, and visualization of classic image processing operations and computer vision algorithms. Developed using **Python, OpenCV, NumPy, and Matplotlib**.

---

##  Project Structure & Completed Tasks

### [Task 1: Basic Geometric Transformations](task1_composite.png)
- **Objective**: Translate, rotate, scale, and shear a single source image asset.
- **Techniques Used**: Homogeneous transform matrices, `cv2.getRotationMatrix2D`, and `cv2.warpAffine`.
- **Output**: `task1_composite.png` (2x2 grid containing the composite operations).

### [Task 2: Interpolation Comparison (Enlargement)](task2_interpolation_comparison.png)
- **Objective**: Zoom in on high-frequency details (e.g., textures or structural edges) using different interpolation methods.
- **Interpolation Methods Compared**:
  - **Nearest Neighbor**: Fast but introduces blocky, pixelated, and staircase artifacts.
  - **Bilinear**: Produces a softer image but introduces blurring at sharp boundaries.
  - **Bicubic**: Preserves sharp details and structural features with minimal distortion.
- **Output**: `task2_interpolation_comparison.png`.

### [Task 3: Four-Point Perspective Correction](task3_perspective_correction.png)
- **Objective**: Correct perspective projection from an angled photograph to a straight-on, orthographic view.
- **Techniques Used**: Finding homography via `cv2.getPerspectiveTransform` and warping coords via `cv2.warpPerspective`.
- **Output**: `task3_perspective_correction.png`.

### Task 4 & 5: Image Pyramids & Multi-Resolution Edge Detail
- **Objective**: Construct a 4-level Gaussian Pyramid downscaled progressively, and extract lost detail via Laplacian edge detail construction.
- **Mathematical Concept**: 
  $$\\text{Laplacian Detail} = G_k - \\text{pyrUp}(G_{k+1})$$

### Task 6: Aliasing Mitigation (Subsampling vs. Pre-filtering)
- **Objective**: Prove how proper low-pass filtering prevents aliasing (moiré patterns) on fine patterns.
- **Methodology**: Evaluates direct pixel decimation (`img[::factor, ::factor]`) against Gaussian pre-filtered downsampling (`cv2.GaussianBlur` followed by decimation).

### Task 7: Upscaling Quality & Interpolation Kernels
- **Objective**: Scale up a low-resolution asset using Nearest Neighbor, Bilinear, Bicubic, and Lanczos4 kernels, and evaluate unwanted ringing, blurring, and edge smoothness.

---

##  Generated Outputs
Your workspace automatically generates and saves the following assets upon running the notebook:
- `task1_composite.png` - Visual grid showing translation, rotation, scaling, and shear.
- `task2_interpolation_comparison.png` - Close-up comparison of interpolation methods.
- `task3_perspective_correction.png` - Warped, orthorectified view of the target facade/document.
- `task_comparison.png` - Global dashboard displaying intermediate pipeline states.

---

##  Getting Started

### Prerequisites
Install the required Python modules:
```bash
pip install opencv-python numpy matplotlib
```

### How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/computer-vision-toolkit.git
   ```
2. Run the notebook sequentially to recreate all figures and generate the output PNGs.
"""

with open('README.md', 'w') as f:
    f.write(github_readme)
print("A professional GitHub-ready README.md file has been generated successfully!")
