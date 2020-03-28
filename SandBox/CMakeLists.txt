cmake_minimum_required(VERSION 3.16)
project(SandBox)

find_package(OpenCV REQUIRED)

add_executable(main src/main.cpp)
target_include_directories(main
    PRIVATE
    ${OpenCV_INCLUDE_DIRS}
    ${PROJECT_SOURCE_DIR}/src
    ${LIBRARY_PATH}
)
target_link_libraries(main 
    ${OpenCV_LIBS}
    ${PROJECT_SOURCE_DIR}
)


