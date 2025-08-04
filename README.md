# CASTNet
This is an implementation of "CASTNet: Computationally-Efficient Adaptive Spatio-Temporal Network for Urban Traffic Prediction".

# Table of Contents

```text
basicts   --> The BasicTS, which provides standard pipelines for training MTS forecasting models. Don't worry if you don't know it, because it doesn't prevent you from understanding CASTNet's code.

datasets  --> Raw datasets and preprocessed data

experiments  --> Training scripts.

scripts   --> Data preprocessing scripts.

CASTNet/arch      --> The implementation of CASTNet.

CASTNet/${DATASET_NAME}.py    --> Training configs.
```

Replace `${DATASET_NAME}` with one of  `PEMS04`,  `PEMS08`, `METR-LA`, `PEMS-BAY`, or any other dataset you want to use.

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

You can download the `all_data.zip` file from [Google Drive](https://drive.google.com/drive/folders/14EJVODCU48fGK0FkyeVom_9lETh80Yjp?usp=sharing) or [Baidu Netdisk](https://pan.baidu.com/s/1shA2scuMdZHlx6pj35Dl7A?pwd=s2xe). Unzip the files to the `datasets/` directory:

```bash
cd /path/to/BasicTS # not BasicTS/basicts
unzip /path/to/all_data.zip -d datasets/
```

These datasets have been preprocessed and are ready for use.

# Train CASTNet
```bash
python experiments/train.py --cfg CASTNet/${DATASET_NAME}.py --gpus '0'
```

Replace `${DATASET_NAME}` with one of  `PEMS04`,  `PEMS08`, `METR-LA`, `PEMS-BAY`, or any other dataset you want to use.

# Acknowledgement
We thank the authors of the following repository for code reference:[BasicTS](https://github.com/zezhishao/BasicTS)
