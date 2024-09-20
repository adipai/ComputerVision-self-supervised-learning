## Self-supervised learning - Computer vision
Final project for ECE-763-Computer Vision at NCSU. We explore 2 self-supervised learning model architectures in computer vision:
- [SimCLR](https://arxiv.org/abs/2002.05709)
- [Barlow Twins](https://arxiv.org/abs/2103.03230)

## 🛠️ Installation

- Download and install [Anaconda](https://www.anaconda.com/download).

- Create a conda virtual environment with the name, e.g., `cv_ssl`, and activate it:

  ```bash
  # list existing env
  # conda env list
  # remove an env
  # conda env remove -n env_name

  conda create -n cv_ssl python=3.11.7 -y
  conda activate cv_ssl
  ```

  We will use ```python3.11 -m``` in running pip or other installations below.

- Put this code in a folder, e.g., `~/cv_ssl`

    ```bash
    cd ~/cv_ssl
    ```

- [**Linux and Windows w/ GPU**] Install PyTorch:

  For examples, to install `torch==2.1.2` with `CUDA==11.8`:

  ```bash
  conda install pytorch==2.1.2 torchvision==0.16.2 torchaudio==2.1.2 pytorch-cuda=11.8 -c pytorch -c nvidia
  ```
  Or

  ```bash
  python3.11 -m pip install torch==2.1.2 torchvision==0.16.2 torchaudio==2.1.2 --index-url https://download.pytorch.org/whl/cu118
  ```

- [**Linux and Windows w/ CPU Only**] Install PyTorch:

  ```bash
  conda install pytorch==2.1.2 torchvision==0.16.2 torchaudio==2.1.2 cpuonly -c pytorch
  ```
  Or

  ```bash
  python3.11 -m pip install torch==2.1.2 torchvision==0.16.2 torchaudio==2.1.2 --index-url https://download.pytorch.org/whl/cpu
  ```

- [**Mac OSX**] Install PyTorch:

  ```bash
  conda install pytorch==2.1.2 torchvision==0.16.2 torchaudio==2.1.2 -c pytorch
  ```
  Or

  ```bash
  python3.11 -m pip install torch==2.1.2 torchvision==0.16.2 torchaudio==2.1.2
  ```
It is highly recommended to use a GPU to train the SimCLR and Barlow twins models, given their complexity and depth. We used Nvidia's GeForce RTX 2080 Ti to train our models.
