# PGM Image Editor - Python (COL100)

This repository contains a simple image editor implemented in Python. The image editor performs basic tasks on an input image in the PGM (Portable Graymap) format.

## Features

The image editor supports the following tasks:

1. **Averaging Filter:** Creates an output image by calculating the average of pixel values from the input image's neighborhood. The output pixel value at location (i, j) is the average of the pixel values at locations (i − 1, j − 1), (i − 1, j), (i − 1, j + 1), (i, j − 1), (i, j), (i, j + 1), (i + 1, j − 1), (i + 1, j), and (i + 1, j + 1).

2. **Edge Detection:** Detects edges in the input image by computing the horizontal and vertical gradients. The gradients are calculated using neighboring pixel values, and the edge detection result is saved as an output image named "edge.pgm".

3. **Path of Least Energy:** Implements an algorithm to find the path of least energy from the top to the bottom of the image. The energy image is derived from the edge image computed in the previous step. The algorithm computes the minimum energy path by considering the energy values and selecting the path with the lowest cumulative energy.

## Usage

To use the PGM Image Editor, follow these steps:

1. Clone the repository: `git clone https://github.com/AkshatGadhwal/PGM-Image_Editor_Python_COL100.git`
2. Navigate to the project directory: `cd PGM-Image_Editor_Python_COL100`
3. Run the Python script with the desired operation:

   - For the averaging filter: `python image_editor.py average <input_image.pgm> <output_image.pgm>`
   - For edge detection: `python image_editor.py edge_detect <input_image.pgm>`
   - For the path of least energy: `python image_editor.py path_energy <input_image.pgm> <output_image.pgm>`

   Replace `<input_image.pgm>` with the path to the input image file in PGM format, and `<output_image.pgm>` with the desired name for the output image file.

## File Format

The input images should be in the PGM format, which has the following specifications:

- The first line contains the identifier for the image, which for this assignment is "P2".
- The second line contains the dimensions of the image, indicating the width and height respectively.
- The next line specifies the maximum allowed pixel value for the image, which is 255 for this assignment.
- The subsequent lines contain the actual pixel values of the image in row-major order.

## Example

Here is an example of using the PGM Image Editor:

```shell
python image_editor.py average input.pgm output.pgm
```

This command applies the averaging filter to the input image `input.pgm` and saves the output image as `output.pgm`.

## Contributions

Contributions to this repository are welcome. If you find any issues or have improvements to suggest, please feel free to open a pull request.

## License

This repository is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.

## Acknowledgments

Special thanks to the COL100 course instructors and teaching assistants for providing the assignment and guidance throughout the course.

Happy image editing!
