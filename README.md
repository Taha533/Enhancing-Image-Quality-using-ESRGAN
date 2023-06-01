

# Enhancing Image Quality using ESRGAN

This project focuses on upscaling low-resolution images using ESRGAN (Enhanced Super-Resolution Generative Adversarial Networks). ESRGAN is a deep learning-based technique that leverages generative adversarial networks to enhance image resolution and quality.

## Table of Contents

- [Installation](#installation)
- [Output Results](#output-results)
- [Contact](#contact)


## Installation

1. Clone the repository:

```bash
!git clone https://github.com/xinntao/ESRGAN

```
2. To download the pretrained model from google drive directly from here, here i'm using a library called gdown. To install gdown, run this command:

```bash
!pip install gdown
```
3. Then download the pretrained model using this command:

```bash
import warnings
warnings.filterwarnings("ignore")
!gdown --id 1TPrz5QKd8DHHt1k8SRtm6tMiPjz_Qene
```

4. Now you need to install some necessary dependencies for ESRGAN:
```bash
!pip install opencv-python glob2

```
```bash
!pip3 install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu113
```
5. Now, ESRGAN requires to have the pre-trained model under the model folder of the github repository. So, we have to move the pretrained model which we download before from google drive, to the model folder. If you do this on your local machine, you can just, copy-paste the model, but if you do this on kaggle kernel or google collab, you need to do it through some code.

```bash
import os, shutil
source = "./RRDB_ESRGAN_x4.pth"
destination = "./ESRGAN/models/"
shutil.move(source,destination)
```

6. For testing, you need to add your images under the LR folder of the git repository.

7. Now, to test the model which is under the ESRGAN folder. You, need to go to this directory. So, first you need to shift your working directory then you need to run the script called test.py, which is going to test the model on your images.

```bash
%cd ESRGAN
!python test.py
```

## Output Results
1. Image 1\
![image 1](https://github.com/Taha533/Enhancing-Image-Quality-using-ESRGAN/blob/main/Output/result_1.png?raw=true)

2. Image 2\
![Image 2](https://github.com/Taha533/Enhancing-Image-Quality-using-ESRGAN/blob/main/Output/result_2.png?raw=true)

3. Image 3\
![image 3](https://github.com/Taha533/Enhancing-Image-Quality-using-ESRGAN/blob/main/Output/results_3.png?raw=true)

## Contact
If you have any questions or suggestions, feel free to reach out to me:\
E-mail: taha15@cse.pstu.ac.bd \
Linkedin: https://www.linkedin.com/in/bahauddin-taha-67617315b/










