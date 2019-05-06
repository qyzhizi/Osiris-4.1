PKG_CONFIG_PATH=$PKG_CONFIG_PATH:/home/qy/opencv-2.4.9/build/installed-DWITH_CUDA=OFF/lib/pkgconfig/
export PKG_CONFIG_PATH

all : OsiMain.cpp OsiManager.cpp OsiEye.cpp OsiProcessings.cpp OsiCircle.cpp
	g++ OsiMain.cpp OsiManager.cpp OsiEye.cpp OsiProcessings.cpp OsiCircle.cpp -o osiris `pkg-config opencv --cflags --libs`
	
clean : osiris
	rm *[~o]
	
