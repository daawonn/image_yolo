# dl_study_image

## image classification 
### example

## object detection 
### yolo v4
- 관련 자료
- https://webnautes.tistory.com/1417
- https://ropiens.tistory.com/33
- https://junyoung-jamong.github.io/deep/learning/2019/01/22/Darkflow%EB%A5%BC-%ED%99%9C%EC%9A%A9%ED%95%B4-YOLO%EB%AA%A8%EB%8D%B8-%EC%9D%B4%EB%AF%B8%EC%A7%80-%EB%94%94%ED%85%8D%EC%85%98-%EA%B5%AC%ED%98%84-in-windows.html

### opencv3.4.0버전 설치
https://stackoverflow.com/questions/36814673/installing-opencv-in-anaconda3-python-h-no-such-file-or-directory
- 컴파일오류
cmake -D CMAKE_BUILD_TYPE=RELEASE 
-D CMAKE_INSTALL_PREFIX=/usr/local 
-D WITH_TBB=OFF -D WITH_IPP=OFF 
-D WITH_1394=OFF 
-D BUILD_WITH_DEBUG_INFO=OFF
-D BUILD_DOCS=OFF 
-D INSTALL_C_EXAMPLES=ON 
-D INSTALL_PYTHON_EXAMPLES=ON 
-D BUILD_EXAMPLES=OFF 
-D BUILD_TESTS=OFF 
-D BUILD_PERF_TESTS=OFF 
-D WITH_QT=OFF 
-D WITH_GTK=ON 
-D WITH_OPENGL=ON 
-D OPENCV_EXTRA_MODULES_PATH=../../opencv_contrib-3.4.0/modules 
-D WITH_V4L=ON  
-D WITH_FFMPEG=ON 
-D WITH_XINE=ON 
-D BUILD_NEW_PYTHON_SUPPORT=ON 
-D PYTHON3_INCLUDE_DIR=anaconda3/include/python3.7m/ -> 이부분 고침
-D PYTHON3_NUMPY_INCLUDE_DIRS=/usr/lib/python3/dist-packages/numpy/core/include/  
-D PYTHON3_PACKAGES_PATH=/usr/lib/python3/dist-packages 
-D PYTHON3_LIBRARY=/usr/lib/x86_64-linux-gnu/libpython3.7m.so ../

- 6/19 (금) 
- darknet Makefile 오류 (make: *** [obj/convolutional_kernels.o] Error 127)
- 아마도 makefile의 gpu=1 이 설정이 안된듯 opencv=1 만 고치고 다시 make 하니 적용됨
- yolo3.weights 받아서 test파일 실행해보기


### frcnn

- 6/18 (목) 오류 목록

- unresolved import keras
- No module numpy ~~
- 해결 관련 모듈 uninstall / install 다시 함!

- h5py is running against HDF5 1.10.5 when it was built against 1.10.4, this may cause problems
- 해결 pip install h5py --upgrade --no-dependencies --force

- add_weight() got multiple values for argument 'name'
- keras 문제인듯..
