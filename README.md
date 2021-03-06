# TensorFlow and scikit-learn with Python3.6 via Docker

This contains `Dockerfile`s to make it easy to get up and running with
TensorFlow and scikit-learn via [Docker](http://www.docker.com/).


## 1. Installing Docker
General installation instructions are
[on the Docker site](https://docs.docker.com/installation/), but we give some
quick links here:

* [OSX](https://www.docker.com/docker-mac)
* [Windows](https://www.docker.com/docker-windows)
* [CentOS](https://docs.docker.com/engine/install/centos/)
* [Ubuntu](https://docs.docker.com/engine/install/ubuntu)

## 2. Running the container

### 2.1 create a new Data directory at local
Linux/MacOS:

    $ mkdir /notebooks
    
Windows:

    $ mkdir c:\notebooks


>**[Note]**
>if you are useing 'Docker for Windows',you need to configuring [Shared Drives](https://blogs.msdn.microsoft.com/stevelasker/2016/06/14/configuring-docker-for-windows-volumes/)


### 2.2 run a new Docker container
Linux/MacOS:

    $ docker run -p 8888:8888 -v /notebooks:/notebooks -it --rm tennisky/data-analysis-environment-by-docker

Windows:

    $ docker run -p 8888:8888 -v /c/notebooks:/notebooks -it --rm tennisky/data-analysis-environment-by-docker



>This container setup:
>- Python 3.6
>- TensorFlow 1.2.1
>- scikit-learn 
>- keras
>- sklearn
>- jupyter
>- scipy
>- simpy
>- matplotlib
>- numpy
>- pandas
>- seaborn
>- plotly
>- sympy
>- mecab-python3
>- librosa
>- Pillow
>- h5py
>- xgboost
>- lightgbm
>- tqdm
>- google-api-python-client


This container is CPU Only.If you want to use GPU, rebuilding GPU images requires [nvidia-docker](https://github.com/NVIDIA/nvidia-docker).


## 3. How To Use Jupyter Notebooks
Copy/paste this URL into your browser when you connect for the first time,


    to login with a token:
        http://localhost:8888/?token=<your token>


