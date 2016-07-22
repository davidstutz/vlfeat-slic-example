include_directories(../lib_vlfeat/)

find_package(OpenCV REQUIRED)
find_package(Threads)
add_executable(vlfeat_slic_example main.cpp)
target_link_libraries(vlfeat_slic_example ${OpenCV_LIBS} vlfeat_slic pthread)
