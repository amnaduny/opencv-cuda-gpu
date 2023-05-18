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
4. CUDA version 11.2

Follow this step carefully (this step installation is for windows) :
1. Download and install NVIDIA-CUDA [here](https://developer.nvidia.com/cuda-downloads?target_os=Windows&target_arch=x86_64&target_version=10&target_type=exe_local)
2. Install Cmake, you can download [here](https://cmake.org/download/) and choose windows x64 installer or you can just click [here](https://github.com/Kitware/CMake/releases/download/v3.26.3/cmake-3.26.3-windows-x86_64.msi) to download Cmake installation directly.
3. Download and extract opencv 4.6.0 source code [here](https://github.com/opencv/opencv/archive/refs/tags/4.6.0.zip) or you can try to download other version shown below.

![opencv version](https://github.com/amnaduny/opencv-cuda-gpu/assets/117987126/d2021d3e-c49b-4b9d-ab62-802b508b499b)

4. Download and extract opencv_contrib 4.6.0 [here](https://github.com/opencv/opencv_contrib/archive/refs/tags/4.6.0.zip), remember to download the same version in opencv source code and contrib file.
5. Create folder "opencvGPU" in your local computer, in my case I create it on local disk C:\opencvGPU. Put opencv-4.6.0 and opencv_contrib-4.6.0 in this folder and create 'build' folder. We have empty 'build' folder, this folder will be a place for cmake to build the binaries. Do the same as picture below.

![cmake dir](https://github.com/amnaduny/opencv-cuda-gpu/assets/117987126/0ecd0a13-df68-4716-9fb9-e26ac0fdcf20)

6. After it's done, click configure and pop up will show up. need to install Visual Studio 16 (or Visual Studio 2019), you can download it [here](https://visualstudio.microsoft.com/vs/older-downloads/). Put the same form as below then finish.

![configure cmake config](https://github.com/amnaduny/opencv-cuda-gpu/assets/117987126/d7b8b84e-1600-4149-adbb-9c004463c76b)

7. After that wait untill finish the configuration for the first time. And then set different kind of flags (type on search to find it quick) such as :
- WITH_CUDA (checklist)
- ENABLE_FAST_MATH (checklist)
- BUILD_opencv_world (checklist)
- OPENCV_EXTRA_MODULES_PATH (select directory of opencv-contrib modules, C:\opencvGPU\opencv_contrib-4.6.0\modules
- And then click configure again and wait in several minutes.
- After that, set several flags again.
- CUDA_FAST_MATH (checklist)
- CUDA_ARCH_BIN (6.1), you can check compute capability of NVIDIA GPU [here](https://developer.nvidia.com/cuda-gpus) and click CUDA-Enabled GeForce and TITAN Products, in this case I'm using NVIDIA GeForce GTX 1050 so the compute capability is 6.1, if you have more than 1 GPU so put more than 1 value for CUDA_ARCH_BIN e.g (6.1;8.6:and soon).
- CMAKE_CONFIGURATION_TYPES (Release)
- Then click Configure for the last time, wait till done.

8. After that, open "command prompt" and type command to install : cmake --build "C:\your_path\build" --target INSTALL --config Release, example : Command to Install: cmake --build "C:\opencvGPU\build" --target INSTALL --config Release, press ENTER and the command will run the program to build the binaries files into build directory. It takes 1-2 hours depend on your laptop. Maybe you will face some error and warning but as long as the installation is still working so don't worry about it just continue it.

9. After finish building the binaries, open cmd again and type the same as below :
![cmd cudadeviceinfo](https://github.com/amnaduny/opencv-cuda-gpu/assets/117987126/7a180e14-b9a8-43b3-b81a-86c708353d07)


