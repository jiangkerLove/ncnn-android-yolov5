project(yolov5ncnn)

cmake_minimum_required(VERSION 3.22.1)

set(ncnn_DIR ${CMAKE_SOURCE_DIR}/ncnn-20201218-android-vulkan/${ANDROID_ABI}/lib/cmake/ncnn)
find_package(ncnn REQUIRED)

add_library(yolov5ncnn SHARED yolov5ncnn_jni.cpp)

target_link_libraries(yolov5ncnn
    ncnn

    jnigraphics
)
