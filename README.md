# 创建带有 GPU 支持的 PyTorch 虚拟环境

[查看pytorch 、torchvison、python版本对应关系](https://github.com/pytorch/vision)
## 步骤 1：创建虚拟环境

1. **创建一个新的虚拟环境：**
   你可以使用以下命令来创建一个名为 `pytorch_env` 的虚拟环境，并指定使用 Python 版本。例如，创建一个 Python 3.8 的环境：

   ```bash
   conda create --name pytorch_env python=3.8
   ```

2. **激活虚拟环境：**
    ```bash
    conda activate pytorch_env
    ```

3. **进入 Python 环境：**
    验证 PyTorch 是否成功安装，并检查是否支持 CUDA：
    ```python
    import torch
    print(torch.__version__)
    print(torch.cuda.is_available())
    ```

## 步骤 2：安装pytorch、torchvision
1. **查看对应cuda安装命令：**
    [查看pytorch 、torchvison、python版本对应关系](https://github.com/pytorch/vision)
    [之前的版本的安装命令](https://pytorch.org/get-started/previous-versions/)
    [最新版本命令](https://pytorch.org/get-started/locally/)
    [直接下载文件进行安装的仓库](https://download.pytorch.org/whl/cu118/torch_stable.html)

2. **使用 Pip 安装 PyTorch：**
    
    PyTorch 官方提供了安装命令，可以通过选择 CUDA 版本和所需的包来生成适合你的命令。这里是使用 CUDA 11.8 的安装命令：
    ```bash
    pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
    ```

3. **替换安装镜像源命令：** 
    -阿里云conda： `conda install -c  https://mirrors.aliyun.com/anaconda/pkgs/main  `  
    -中科大 conda：`conda install -c  https://mirrors.ustc.edu.cn/anaconda/pkgs/main  ` 
    -中科大 pip：`pip install -i  https://pypi.mirrors.ustc.edu.cn/simple  `                
    -阿里云 pip：            `pip install -i  https://mirrors.aliyun.com/pypi/simple  `       
    -豆 瓣   pip：           `pip install -i  https://pypi.douban.com/simple  `             

