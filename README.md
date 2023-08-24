
---

# Polycrystalline Microstructure Analysis

## Description

This repository contains an image processing technique designed for analyzing polycrystalline microstructures. The technique involves several steps, including converting microstructure images into binary format, removing noise and unwanted features, identifying grain boundaries and triple point junctions, and calculating dihedral angles at these junctions.

The process can be summarized as follows:

1. **Image Preprocessing:**
   - Convert the microstructure image into a binary format using a cumulative distribution function-based thresholding.
   - Apply morphological operations (dilation and erosion) to remove noise, pits, and precipitates from the image.

2. **Skeletonization:**
   - Convert grain boundaries into single-pixel lines using skeletonization techniques.
   - Apply a reconstruction operation to further refine the skeletonized image and remove residual noise.

3. **Triple Junction Detection:**
   - Employ Hit and Miss transformation with various structuring elements and orientations to identify triple point junctions.
   - Combine results from different orientations to obtain a final image with accurate triple point locations.

4. **Grain Boundary Coordinate Determination:**
   - Scan neighboring pixels around each triple point to identify grain boundary coordinates.
   - Remove dangling branches and false triple points based on a threshold criterion.

5. **Angle Calculation:**
   - Fit third-order polynomials to grain boundaries starting from each triple point.
   - Calculate derivatives of the polynomials to determine tangent angles between grain boundaries at triple point junctions.

## Repository Contents

- `code/`: Contains the Python scripts for implementing the image processing technique.
- `images/`: Includes example input microstructure images and the intermediate/output images at various processing stages.
- `results/`: Stores the results obtained, including triple point locations, grain boundary coordinates, and calculated dihedral angles.
- `README.md`: The document you are reading right now, providing an overview of the technique, its steps, and the repository's structure.

## Getting Started

1. Clone the repository to your local machine.
2. Navigate to the `code/` directory and run the provided Python scripts in sequential order.
3. Follow the instructions in the scripts to provide input images and parameters.
4. Examine the generated results in the `results/` directory, including processed images and calculated dihedral angles.

## Dependencies

- Python 
- OpenCV 
- Numpy 
- Matplotlib 

## Contributors

- [NIDHI](https://github.com/nidhiyadav2003)

## License


---
