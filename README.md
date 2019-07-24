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
    
    
    
