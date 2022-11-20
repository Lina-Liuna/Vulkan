# Vulkan
![alt text](https://github.com/Lina-Liuna/Vulkan/commit/ff4ce1495e1722b132b12874398d6fabcaf4a7d6#diff-1c8852012a9a4bd0800f931e7178a209bd9e69c2ec9d0174420aa8bbf566e03d)
![Screenshot](Succeed Running Vulkan Examples on my macOS.jpg)
2. Download latest VulkanSDK for macOS from https://vulkan.lunarg.com/sdk/home#mac
3. Install
4. Download VulkanTools from https://github.com/LunarG/VulkanTools
5.     git clone --recurse-submodules git@github.com:LunarG/VulkanTools.git
    cd VulkanTools
    mkdir build
    ./update_external_sources.sh
    cd build
    ../scripts/update_deps.py
    cmake -C helper.cmake ..
    cmake --build . --parallel

6. Download Vulkan-Tools from https://github.com/KhronosGroup/Vulkan-Tools

7. error happened, running .sh errors is because you need set environment in ./bash_profile
8. cmake error happened, need set some C++ compile environment in ./zshrc
9. run ./cube to validate your vulkan environment

