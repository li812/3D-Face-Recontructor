# 3D Face Reconstruction

## Overview
This project involves creating a 3D model of a human face from a 2D image. It uses several libraries including Open3D, PyVista, MTCNN, and the Dense Prediction Transformer (DPT) model from Intel. The goal is to take a 2D image of a face and transform it into a 3D model that can be used for various applications.

## Use Cases

This project can be used for a variety of applications, including but not limited to:

- **Facial Recognition**: The 3D models generated can be used to improve the accuracy of facial recognition systems by providing more detailed facial features than 2D images. This can be particularly useful in security systems or any application where accurate identification is crucial.

- **Animation**: The 3D models can be used in animation, allowing for more realistic and detailed characters. This can enhance the viewer's experience and make the animation more lifelike.

- **Medical Imaging**: This can be used in medical imaging to create 3D models of patients' faces for surgical planning or diagnosis. This can provide doctors with a better understanding of the patient's facial structure, leading to more accurate and effective treatment plans.

- **Virtual Reality**: The 3D models can be used in virtual reality applications, allowing users to see a more realistic version of their face in the virtual world. This can enhance the user's immersion and make the virtual experience more engaging.

## Setup

To set up this project, you need to clone the repository to your local machine. You can do this by running the following command in your terminal:

```bash
git clone https://github.com/li812/3D-Face-Recontructor.git
```

This will create a copy of the project on your local machine which you can then navigate to using your terminal.

## Installation

This project requires several Python libraries. You can install these libraries using pip, which is a package manager for Python. Here are the commands to install each library:

```bash
pip install os
pip install matplotlib
pip install opencv-python
pip install numpy
pip install mtcnn
pip install torch
pip install pymesh-fix
pip install pillow
pip install transformers
pip install open3d
pip install pyvista
pip install trame
```

Run each command in your terminal to install the libraries. Make sure you have pip installed on your machine. If not, you can install it by following the instructions on the [official pip installation guide](https://pip.pypa.io/en/stable/installing/).

## Steps Involved

The project involves several steps, each of which plays a crucial role in the 3D face reconstruction process:

1. **Import Libraries**: This step imports all the necessary libraries for the project. These libraries provide the functions and methods needed to implement the project.

2. **Face Alignment and Cropping**: This function `align_and_crop_face(image)` uses the MTCNN detector to detect faces in the image. It then aligns the detected face and crops it. The function returns the aligned face and the cropped face. This is important as it isolates the face from the rest of the image, allowing for more accurate depth estimation and 3D reconstruction.

3. **Align and Crop**: This step reads an image from the specified image path. It then applies the `align_and_crop_face(image)` function to it, and saves the aligned and cropped face images in the specified directories. This prepares the image for depth estimation.

4. **Estimate Depth**: This step uses the DPT model from Intel to estimate the depth of the aligned face image. The DPT model is a transformer-based model that is designed for depth estimation tasks. This step is crucial as it provides the depth information needed for 3D reconstruction.

5. **3D Reconstruction**: This step creates a point cloud from the depth map using Open3D. It uses the intrinsic parameters of the camera to create an RGB-D image from the color and depth images. The RGB-D image is then used to create a point cloud. This is the main step where the 3D model of the face is created.

6. **Create and Save Point Cloud**: This step creates a point cloud from the RGB-D image and saves it as a .ply file. The .ply file can be used for further processing or visualization.

7. **Plot**: This step uses PyVista to plot the point cloud. PyVista is a 3D visualization and analysis library that is built on top of VTK and PyVista. This allows you to visualize the 3D model.

8. **View in Open3D**: This step uses Open3D to visualize the point cloud. Open3D is a modern library for 3D data processing. This provides another way to visualize the 3D model.

## Usage

To use this project, run the main.ipynb Jupyter notebook. Make sure to install all the dependencies listed in the requirements.txt file. The notebook contains all the code for the project and is designed to be run from top to bottom.

## Contributing

Contributions are welcome. Please open an issue to discuss your ideas or open a pull request with your changes. When opening a pull request, please make sure to update the corresponding documentation and tests.

## License

This project is licensed under the terms of the MIT license. This means you are free to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the software, provided that you include the above copyright notice and this permission notice in all copies or substantial portions of the software.
