# Vulkan

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

How to run Excellent Vulkan Examples from git@github.com:SaschaWillems/Vulkan.git:
1. git clone
2. git submodule init
3. git submodule update
4. python download_assets.py
5. git clone git@github.com:KhronosGroup/MoltenVK.git
6. cd MoltenVK
7. ./fetchDependencies --macos
8. make macos
9. cd macos
10. cd xcode
11. rm MoltenVK
12. ln -s /Users/linaliu/code/Sascha/MoltenVK/MoltenVK
13. open xcode project, press run
14. Amazing demo come out!