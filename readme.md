## Softwares and Libraries needed to run the Program in Windows 10
1. Install Visual Studio :
* [How to install Visual Studio](https://docs.microsoft.com/en-us/visualstudio/install/install-visual-studio?view=vs-2019)

2. Install Anaconda with Python3

3. Make a new conda environment and activate it.

4. Install cmake
```
pip install cmake
```

5. Install Nvidia CUDA Toolkit :
* [Nvidia documentation for installing CUDA Toolkit](https://docs.nvidia.com/cuda/cuda-installation-guide-microsoft-windows/index.html)

6. Install Nvidia CUDA Deep Neural Network Library (cuDNN) for windows :
* [Nvidia documentation for installing cuDNN](https://docs.nvidia.com/deeplearning/cudnn/install-guide/index.html)

7. Install **dlib** library (with GPU support), which will be used to construct our face embeddings for actual recognition process.
```
$ workon <your env name here> # optional
$ git clone https://github.com/davisking/dlib.git
$ cd dlib
$ mkdir build
$ cd build
$ cmake .. -DDLIB_USE_CUDA=1 -DUSE_AVX_INSTRUCTIONS=1
$ cmake --build .
$ cd ..
$ python setup.py install --yes USE_AVX_INSTRUCTIONS --yes DLIB_USE_CUDA
```

8. Install the **face_recognition** package
```
pip install face_recognition
```

9. Install **imutils**
```
pip install imutils
```
