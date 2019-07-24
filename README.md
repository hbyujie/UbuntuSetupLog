# UbuntuSetupLog


一. 安装
  1. conda:  
    conda create -n name -p position python=(2.7/3.5/3.6...)

  2. apt:
    apt-cache search name
    sudo apt-get install name
    
  3. pip
    pip install name
    
  4. mysql:
    sudo apt-get install mysql-server
    sudo apt-get install mysql-client
    sudo apt-get install libmysqlclient-dev
    sudo apt-get install mysql-workbench
    测试是否成功: sudo netstat -tap | grep mysql

  5. opencv
    sudo apt-get install libcv-dev
    pkg-config opencv --modversion

  6. cmake 编译安装
    cmake install，需要安装gui时添加 --qt-gui
    ./configure --qt-gui

  7. conda pytoch
  
    conda create -n pytorch python=2.7
    conda activate pytorch
    conda install pytorch torchvision cudatoolkit=9.0 -c pytorch
         参考: https://pytorch.org/get-started/locally/
    download slow solver: https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/
    conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/
    conda install pytorch torchvision cudatoolkit=9.0
         
  8. 显卡驱动
  
    sudo apt-get purge nvidia*
    sudo add-apt-repository ppa:graphics-drivers
    sudo apt-get update
    sudo apt-cache search nvidia
    ubuntu-drivers devices
    sudo apt-get install nvidia-415 nvidia-settings nvidia-prime
    nvidia-smi

   9. cuda
  
    下载网址：
    cuda: https://developer.nvidia.com/cuda-toolkit-archive
    cudnn: https://developer.nvidia.com/rdp/cudnn-archive
  
    sudo sh cuda_9.0.176_384.81_linux.run
    sudo sh cuda_9.0.176.1_linux.run
    sudo sh cuda_9.0.176.2_linux.run

    export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/cuda/lib64
    export PATH=$PATH:/usr/local/cuda/bin
    export CUDA_HOME=$CUDA_HOME:/usr/local/cuda
    source ~/.bashrc

    nvcc --version
    cat /usr/local/cuda/version.txt

    sudo cp cuda/include/cudnn.h /usr/local/cuda/include/
    sudo cp cuda/lib64/libcudnn* /usr/local/cuda/lib64/
    sudo chmod a+r /usr/local/cuda/include/cudnn.h
    sudo chmod a+r /usr/local/cuda/lib64/libcudnn*
    cat /usr/local/cuda/include/cudnn.h | grep CUDNN_MAJOR -A 2


二. 删除
  1. conda:
    conda remove -n name --all
    
  2. apt:
    sudo apt-get remove name
    
  3. pip
    pip list
    pip uninstall name
    
  4. sys 删除文件及文件夹 ： https://blog.csdn.net/qq_33144323/article/details/80036970
  


三. 查看
  1. git: 查看仓库
    git remote -v
    git remote add name websit
    gitmodules usage : http://www.cnblogs.com/nicksheng/p/6201711.html
        
  2. git: 查看仓库
    git remote -v
    
  3. sys gpu and memory
    top: cpu memory
    watch -n 1 nvidia-smi: nvidia gpu
    
  比较软件: meld

  protoc --version

  jupyter notebook
    
    
    
