# Multi-Style Generative Network (MSG-Net) for Real-Time Style Transfer

## Overview
This repository implements a **Multi-Style Generative Network (MSG-Net)** for real-time image style transfer. The model leverages an **Inspiration Layer** to efficiently transform images while balancing the quality of optimization-based approaches and the speed of feed-forward networks.

## Features
- **Real-time style transfer** using deep learning.
- **Supports multiple styles** within a single model.
- **Lightweight architecture** for efficient processing.
- **Optimized for high-resolution images** with residual bottleneck blocks.

## Installation
Ensure you have Python and PyTorch installed. Then, clone the repository and install dependencies:

```bash
# Clone the repository
git clone https://github.com/shashwatt-git/Neural_ImageTransfer.git
cd Neural_ImageTransfer

# Install dependencies
pip install -r requirements.txt
```

## Usage
### 1. Prepare Input Images
Place your **content images** in the `input/content/` directory and **style images** in `input/style/`.

### 2. Run Style Transfer
Execute the following command to apply style transfer:
```bash
python run_style_transfer.py --content input/content/image.jpg --style input/style/style.jpg --output output/stylized.jpg
```

### 3. Visualize Results
Processed images will be saved in the `output/` directory.

## Model Architecture
MSG-Net consists of:
- **Encoder:** Extracts features from the input image.
- **Inspiration Layer:** Adapts feature maps based on the target style’s Gram Matrix.
- **Residual Bottleneck Blocks:** Enhances feature extraction efficiency.
- **Decoder:** Generates the stylized output image.

## Training
To train MSG-Net on custom datasets:
```bash
python train.py --dataset /path/to/dataset --epochs 10 --batch_size 16
```

## Technologies Used
- Python, PyTorch
- Neural Networks (Conv, BatchNorm, ReLU)
- Image Processing (PIL, NumPy)

## Future Improvements
- Extend to **higher-resolution image support**.
- Implement **video style transfer**.
- Improve generalization across **diverse artistic styles**.



