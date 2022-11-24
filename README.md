# Vulkan
##### Video games like Anime and Manga Games, it's more exciting to get the technical knowledge about how to implement these games through graphics

![This is my png](https://github.com/Lina-Liuna/Vulkan/raw/main/Succeed%20Running%20Vulkan%20Examples%20on%20my%20macOS.jpg)

### How to run Vulkan-Tools(cube/VulkanInfo)on macOS?
#### To check if you platform support Vulkan
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

### How to run Excellent Vulkan Examples from git@github.com:SaschaWillems/Vulkan.git:
1. git clone
2. git submodule init
3. git submodule update
4. python download_assets.py
5. git clone git@github.com:KhronosGroup/MoltenVK.git
6. cd MoltenVK
7. ./fetchDependencies --macos
8. make macos
9. cd xcode
10. prepare to copy MoltenVK which contained dylib to vulkan examples
11. cd macos
12. rm MoltenVK
13. ln -s /Users/linaliu/code/Sascha/MoltenVK/MoltenVK
14. open xcode project, press run
15. Amazing demo come out!
![This is my png](https://github.com/Lina-Liuna/Vulkan/raw/main/examples_results_screenshot/Elegant%20deer-MVK_tessellation.jpg)
![This is my png](https://github.com/Lina-Liuna/Vulkan/raw/main/examples_results_screenshot/fantasy_mountain_terraintessellation.jpg)
### How to run Vulkan-CTS on macOS? 
##### run Vulkan Comformance Test Suite to validate the application new features.
1. git clone git@github.com:KhronosGroup/VK-GL-CTS.git
2. python3 external/fetch_sources.py to download sources for zlib, libpng, jsoncpp, glslang, vulkan-docs, spirv-headers, and spirv-tools.
3. python3 -m pip install lxml to install lxml
4. mkdir build
5. cd build
6. cmake .. -DCMAKE_BUILD_TYPE=Debug -DDEQP_TARGET=osx -DCMAKE_C_FLAGS=-m64 -DCMAKE_CXX_FLAGS=-m64
7. make -j4, why not just make -j, because you compute may godie!!
8. build done!
9. Run automatically: python3 /Users/linaliu/code/Sascha/VK-GL-CTS/external/vulkancts/scripts/build_mustpass.py
10. cd /Users/linaliu/code/Sascha/VK-GL-CTS/ 
11. Run single Vulkan-CTS test case: ./deqp-vk --deqp-case=dEQP-VK.info.device 
![This is my png](https://github.com/Lina-Liuna/Vulkan/raw/main/examples_results_screenshot/Vulkan-CTS-100_build.jpg)
![This is my png](https://github.com/Lina-Liuna/Vulkan/raw/main/examples_results_screenshot/Run_SingleTestCase_VulkanCTS.jpg)