
- `clear/`: Contains test files.
- `deHaze_Eval.ipynb`: Jupyter notebook for evaluating the dehazing algorithm.
- `deHazing_Algo.ipynb`: Jupyter notebook for running the dehazing algorithm.
- `gf.py`: Python script containing the guided filter implementation.
- `HazeInput/`: Directory for input images.
- `HazeOutput/`: Directory for output images.

## Guided Filter Implementation

The guided filter is implemented in the [gf.py](gf.py) file. Key functions include:

- [`box`](gf.py): O(1) box filter.
- [`_gf_color`](gf.py): Color guided filter.
- [`_gf_gray`](gf.py): Grayscale guided filter.
- [`_gf_colorgray`](gf.py): Automatically chooses color or gray guided filter based on the guide image's shape.
- [`guided_filter`](gf.py): Runs a guided filter per-channel on the filtering input.
- [`test_gf`](gf.py): Function to test the guided filter with example images.

## Dehazing Algorithm

The dehazing algorithm is implemented in the [deHazing_Algo.ipynb](deHazing_Algo.ipynb) notebook. It includes the following steps:

1. Open the input image.
2. Compute the dark channel.
3. Estimate the air light.
4. Compute the transmission map.
5. Apply the guided filter to refine the transmission map.
6. Recover the dehazed image.

## Evaluation

The evaluation of the dehazing algorithm is performed in the [deHaze_Eval.ipynb](deHaze_Eval.ipynb) notebook. It includes loading the dehazed images and computing metrics to evaluate the performance.

## Usage

1. Place the input images in the `HazeInput/` directory.
2. Run the dehazing algorithm using the `deHazing_Algo.ipynb` notebook.
3. The dehazed images will be saved in the `HazeOutput/` directory.
4. Evaluate the results using the `deHaze_Eval.ipynb` notebook.

## Dependencies

- Python 3.x
- NumPy
- SciPy
- ImageIO
- OpenCV
- Jupyter Notebook

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/image-dehazing.git
    cd image-dehazing
    ```

2. Install the required dependencies:
    ```sh
    pip install numpy scipy imageio opencv-python jupyter
    ```

3. Run Jupyter Notebook:
    ```sh
    jupyter notebook
    ```

4. Open and run the `deHazing_Algo.ipynb` and `deHaze_Eval.ipynb` notebooks.

## Acknowledgments

- The guided filter implementation is based on the paper "Guided Image Filtering" by Kaiming He, Jian Sun, and Xiaoou Tang.
