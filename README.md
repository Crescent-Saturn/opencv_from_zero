# Learn and master OpenCV from zero to hero
---

## 1. Installation OpenCv summary (Ubuntu)		

### Install dependencies:		

- update sys:	
	```
	sudo apt update && sudo apt upgrade
	```
- developer tools:									
	```
	sudo apt install build-essential cmake unzip pkg-config
	```

- image and video libs:	
	```
	sudo apt install libjpeg-dev libpng-dev libtiff-dev 
	sudo apt install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev	
	sudo apt install libxvidcore-dev libx264-dev
	```
- GTK and mathematical optimizations:	
	```
	sudo apt install libgtk-3-dev
	sudo apt install libatlas-base-dev gfortran
	```


### Downoad OpenCV || OpenCV_contrib		

[*Latest: Git || Archive: zip*]	

- **opencv:**       		
	```
	git clone https://github.com/opencv/opencv.git 		
	```		    	

- **opecv_contrib:**    
	```
	git clone https://github.com/opencv/opencv_contrib.git	
	```

	```
	cd opencv && mkdir build && cd build    
	```    

> #### *Configure Conda environnement for Python*:     
  ```
	conda create -n your_env_name && conda activate your_env_name     
	conda install numpy python=3.x    
  ```

### Cmake and Compilation		 
  ```
	cmake -D CMAKE_BUILD_TYPE=RELEASE \    
		-D CMAKE_INSTALL_PREFIX=/usr/local \
		-D INSTALL_PYTHON_EXAMPLES=ON \
		-D INSTALL_C_EXAMPLES=ON \
		-D WITH_TBB=ON \
		-D WITH_V4L=ON \
		-D OPENCV_GENERATE_PKGCONFIG=ON \
		-D WITH_QT=ON \
        -D WITH_OPENGL=ON \
		-D OPENCV_ENABLE_NONFREE=ON \
		-D PYTHON_DEFAULT-EXECUTABLE= \
		-D OPENCV_EXTRA_MODULES_PATH=../../opencv_contrib/modules \
		-D ENABLE_CXX11=ON \
		-D BUILD_EXAMPLES=ON ..
  ```

### Completion		

 	 make -j{$}

  get {$} from:    

  	lscpu   # --> CPUs

Installation and Confirmation:       

	sudo make install
	sudo ldconfig  # confirmation
