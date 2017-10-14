# distributed-MXNet
distributed networks on MXNet

# enable cuda GPU
wget http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1404/x86_64/cuda-repo-ubuntu1404_7.5-18_amd64.deb

sudo dpkg -i cuda-repo-ubuntu1404_7.5-18_amd64.deb

echo "deb http://developer.download.nvidia.com/compute/machine-learning/repos/ubuntu1404/x86_64 /" | sudo tee 
/etc/apt/sources.list.d/nvidia-ml.list

sudo apt-get update

sudo apt-get install -y linux-image-extra-\`uname -r\` linux-headers-\`uname -r\` linux-image-\`uname -r\`

sudo apt-get install -y cuda libcudnn5-dev=5.0.5-1+cuda7.5

# install cuDNN:
Note that, the foregoing command will only install cuda for you. To install cuDNN, you need to download the package first from here (https://developer.nvidia.com/cudnn).

Then, follow the following code:
```
tar -xzvf cudnn-9.0-linux-x64-v7.tgz [or whatever version you downloaded]

sudo cp cuda/include/cudnn.h /usr/local/cuda(version)/include
sudo cp cuda/lib64/libcudnn* /usr/local/cuda(version)/lib64
sudo chmod a+r /usr/local/cuda(version)/include/cudnn.h
sudo chmod a+r /usr/local/cuda(version)/lib64/libcudnn*
```
# This command is super useful to run Linux command totally in backend
'''
screen -d -m command
'''
