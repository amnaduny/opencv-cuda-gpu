# opencv-cuda-gpu
Easy installation OpenCV Python and CUDA GPU

Sources :
opencv web : https://opencv.org/
opencv github : https://github.com/opencv
youtube tutorial : https://youtu.be/d8Jx6zO1yw0 (Nicolai Nielsen)

In my case, 
1. I have installed Python 3.9.12
2. Opencv 4.6.0
3. Opencv-contrib 4.6.0
4. cuda version 11.2
5. cudnn version 8.1

Follow this step carefully (this step installation is for windows) :
1. Install Cmake, you can download [here](https://cmake.org/download/) and choose windows x64 installer or you can just click [here](https://github.com/Kitware/CMake/releases/download/v3.26.3/cmake-3.26.3-windows-x86_64.msi) to download Cmake installation directly.
2. Download and extract opencv 4.6.0 source code [here](https://github.com/opencv/opencv/archive/refs/tags/4.6.0.zip) or you can try to download other version shown below.

![opencv version](https://github.com/amnaduny/opencv-cuda-gpu/assets/117987126/d2021d3e-c49b-4b9d-ab62-802b508b499b)

3. Download and extract opencv_contrib 4.6.0 [here](https://github.com/opencv/opencv_contrib/archive/refs/tags/4.6.0.zip), remember to download the same version in opencv source code and contrib file.
4. Create folder "opencvGPU" in your local computer, in my case I create it on local disk C:\opencvGPU. Put opencv-4.6.0 and opencv_contrib-4.6.0 in this folder and create 'build' folder. We have empty 'build' folder, this folder will be a place for cmake to build the binaries. Do the same as picture below.

![cmake dir](https://github.com/amnaduny/opencv-cuda-gpu/assets/117987126/0ecd0a13-df68-4716-9fb9-e26ac0fdcf20)

5. After it's done, click configure and pop up will show up. need to install Visual Studio 16 (or Visual Studio 2019), you can download it [here](https://visualstudio.microsoft.com/vs/older-downloads/). Put the same form as below then finish.

![configure cmake config](https://github.com/amnaduny/opencv-cuda-gpu/assets/117987126/d7b8b84e-1600-4149-adbb-9c004463c76b)

7. 
8. 
