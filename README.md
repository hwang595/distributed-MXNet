# distributed-MXNet
distributed networks on MXNet

# enable cuda GPU
wget http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1404/x86_64/cuda-repo-ubuntu1404_7.5-18_amd64.deb

sudo dpkg -i cuda-repo-ubuntu1404_7.5-18_amd64.deb

echo "deb http://developer.download.nvidia.com/compute/machine-learning/repos/ubuntu1404/x86_64 /" | sudo tee 
/etc/apt/sources.list.d/nvidia-ml.list

sudo apt-get update

sudo apt-get install -y linux-image-extra-`uname -r` linux-headers-`uname -r` linux-image-`uname -r`

sudo apt-get install -y cuda libcudnn5-dev=5.0.5-1+cuda7.5

