# Vulkan
![img.png](img.png)
1. Download latest VulkanSDK for macOS from https://vulkan.lunarg.com/sdk/home#mac
2. Install
3. Download VulkanTools from https://github.com/LunarG/VulkanTools
4.     git clone --recurse-submodules git@github.com:LunarG/VulkanTools.git
    cd VulkanTools
    mkdir build
    ./update_external_sources.sh
    cd build
    ../scripts/update_deps.py
    cmake -C helper.cmake ..
    cmake --build . --parallel

5. Download Vulkan-Tools from https://github.com/KhronosGroup/Vulkan-Tools

6. error happened, running .sh errors is because you need set environment in ./bash_profile
7. cmake error happened, need set some C++ compile environment in ./zshrc
8. run ./cube to validate your vulkan environment

