cmake_minimum_required (VERSION 3.5)

project (Osiris)

set(srcs
    src/OsiCircle.cpp
	src/OsiEye.cpp
	src/OsiMain.cpp
	src/OsiManager.cpp
	src/OsiProcessings.cpp
	)
set(incs
    src/OsiCircle.h
	src/OsiEye.h
	src/OsiManager.h
	src/OsiProcessings.h
	src/OsiStringUtils.h
	)
#opencv
set(OpenCV_DIR /home/qy/opencv-2.4.9/build/installed-DWITH_CUDA=OFF/share/OpenCV )
find_package(OpenCV REQUIRED)
message(STATUS "OpenCV library status:")
message(STATUS "    version: ${OpenCV_VERSION}")
message(STATUS "    libraries: ${OpenCV_LIBS}")
message(STATUS "    include path: ${OpenCV_INCLUDE_DIRS}")

include_directories(${OpenCV_INCLUDE_DIRS})

add_executable(Osiris ${srcs} ${incs})
target_link_libraries(Osiris ${OpenCV_LIBS} )


