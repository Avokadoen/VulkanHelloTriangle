# avoid using this cmake

# TODO: fix | no abs path & build dependencies properly | mode files (like shaders into build)

cmake_minimum_required (VERSION 2.6)

# this might not work. I don't know... 
set(CMAKE_CXX_STANDARD 17)

add_executable(VulkanHelloTriangle VulkanHelloTriangle/source.cpp)

# Use FindVulkan module added with CMAKE 3.7
#if (NOT CMAKE_VERSION VERSION_LESS 3.7.0)
	#find_package(VULKAN REQUIRED)
#endif()

include_directories(VulkanHelloTriangle
	"./libraries/glfw-3.3.bin.WIN64/include"
	"./libraries/glm"
	"C:/VulkanSDK/1.1.106.0/Include"
)

target_link_libraries(VulkanHelloTriangle
	"C:/Users/Aksel/Documents/repositories/VulkanHelloTriangle/libraries/glfw-3.3.bin.WIN64/lib-vc2017/glfw3.lib"
	#"./libraries/glfw-3.3.bin.WIN64/lib-vc2017/glfw3"
	"C:/VulkanSDK/1.1.106.0/Lib/vulkan-1.lib"
)


project (VulkanHelloTriangle)