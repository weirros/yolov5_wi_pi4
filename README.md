# Setup a YoloV5 on a pi 4

Get your os image from this site:
https://www.raspberrypi.org/software/raspberry-pi-desktop/
and flash it to a tf card;
when you booted up successful，you can follow with steps below；


------------

**update the system,and install some base package;**

1.  `sudo apt-get update`
2. `sudo apt-get dist-upgrade`
3. ` sudo apt-get install libopenblas-dev libblas-dev m4 cmake cython python3-dev python3-yaml python3-setuptools`

**install virtualenv for system python3;**
1. `sudo pip3 install virtualenv`

**get the yolov5 clone;**
1. `git clone https://github.com/ultralytics/yolov5`
2. `cd yolov5`

**create a virtual environment of python3 and active it；**
1. `virtualenv yolov5-venv`
2. `source ./yolov5-venv/bin/activate`

**update pip3 of the environment;**
1. `python3 -m pip install --upgrade pip`

**install some package for  the environment;**
**Do not use pip3 install -r requirements.txt,it leads errors;**
1. `pip3 install numpy`
2. `python3.7 -m pip install torch-1.7.0a0-cp37-cp37m-linux_armv7l.whl`
3. `python3.7 -m pip install torchvision-0.8.0a0+45f960c-cp37-cp37m-linux_armv7l.whl`
4. `python3.7 -m pip install matplotlib`
5. `python3.7 -m pip install opencv-python`
6. `python3.7 -m pip install pyyaml`
7. ` python3.7 -m pip install pandas`
8. `python3.7 -m pip install h5py`
9. `python3.7 -m pip install scipy`
10. `python3.7 -m pip install keras`
11. `python3.7 -m pip install tensorboard`
12. ` python3.7 -m pip install tqdm`
13. `python3.7 -m pip install seaborn`

**now you can try;**
1. `python3.7 detect.py`
usually you can see the running out；
[![runing](https://github.com/weirros/yolov5_wi_pi4/blob/main/running.jpg "runing")](https://github.com/weirros/yolov5_wi_pi4/blob/main/running.jpg "runing")


**but if you get some error ,like **
###### *getting ImportError: libopenblas.so.0: cannot open shared object file or directory
you may need install this lib of system;

1. `sudo apt-get install libjpeg8-dev -y`
2. `sudo apt-get install libatlas-base-dev gfortran -y`
3. `sudo apt-get install libgtk2.0-dev -y`
4. `sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev -y`
5. `sudo apt-get install libtiff5-dev -y`
6. `sudo apt-get install libjasper-dev -y`
7. `sudo apt-get install libpng12-dev -y`
8. `sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev -y`
9. ` sudo apt install libopenblas-dev libblas-dev m4 cmake cython python3-dev python3-yaml python3-setuptools`

