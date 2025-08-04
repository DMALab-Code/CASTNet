# CASTNet
This is an implementation of "CASTNet: Computationally-Efficient Adaptive Spatio-Temporal Network for Urban Traffic Prediction".

# Environment
Python 3.11 + PyTorch 2.5.1 + CUDA 12.4 (Recommended)

```bash
# Install Python
conda create -n BasicTS python=3.11
conda activate BasicTS
# Install PyTorch
pip install torch==2.5.1 torchvision==0.20.1 torchaudio==2.5.1 --index-url https://download.pytorch.org/whl/cu124
# Install other dependencies
pip install -r requirements.txt
```

# Dataset
To facilitate the assessment of the experimental results and to ensure fairness in comparison with the baseline, we used the dataset from BasicTS.

Step 1:You can download the `all_data.zip` file from [Google Drive](https://drive.google.com/drive/folders/14EJVODCU48fGK0FkyeVom_9lETh80Yjp?usp=sharing) or [Baidu Netdisk](https://pan.baidu.com/s/1shA2scuMdZHlx6pj35Dl7A?pwd=s2xe). Unzip the files to the `datasets/` directory:

```bash
cd /path/to/BasicTS # not BasicTS/basicts
unzip /path/to/all_data.zip -d datasets/
```

These datasets have been preprocessed and are ready for use.


# Model Code
The core code of the model needs to be made public after the publication of the paper.
