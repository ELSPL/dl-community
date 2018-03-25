# Setting Up a Personal Deep Learning Computer
These are steps to replicate the AWS AMI setup on your own computer (assuming you have NVIDIA CUDA GPUs)  
Recommended hardware:  NVIDIA GTX-1080 Ti  


## Step 1: Install Anaconda Python 3.6
Python version should be 3.6+  
https://conda.io/docs/user-guide/tasks/manage-python.html

If you have two shells such as bash and zsh, and you are using zsh as default then to install python3.6 as default python. Install it in bash and using anaconda so just commenting bash.bashrc path it can be easily disabled as well.
```
sudo su
echo 'export PATH=/opt/conda/bin:$PATH' >> /etc/bash.bashrc && \
    wget --quiet https://repo.continuum.io/archive/Anaconda3-5.0.1-Linux-x86_64.sh -O ~/anaconda.sh && \
    /bin/bash ~/anaconda.sh -b -p /opt/conda && \
    rm ~/anaconda.sh
source /etc/bash.bashrc (or restart terminal)
```

## Step 2: Clone the fastai library
```git
git clone https://github.com/fastai/fastai.git
```

## Step 3: Go to directory where `environment.yml` file
- The environment.yml file is under this directory.  
- The environment file contains all the dependencies needed:  https://github.com/fastai/fastai/blob/master/environment.yml

```bash
cd fastai/ 
```


## Step 4:  Create the virtual environment
This step installs all of the dependencies.  
```bash
conda env create -f environment.yml
```

## Step 5:  Activate virtual environment 
Do this step every time you login. Or else put it in your `.bashrc` file.  
```bash
source activate fastai
```
