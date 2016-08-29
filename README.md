# GPU Memory Tracer
It is implemented based on GPGPU-Sim simulator, which is a detailed cycle-accurate simulator that simulates GPU devices. If you need more information on this simulator, please check README.original.

## Installing, Building and Running this program
CUDA Toolkit must be setup (it is recommended to use version 3.1 for normal PTX simulation and version 4.0 for cuobjdump)

### dependency settings for Ubuntu users

	sudo apt-get install build-essential xutils-dev bison zlib1g-dev flex libglu1-mesa-dev

	sudo apt-get install libxi-dev libxmu-dev libglu3-dev

make sure CUDA_INSTALL_PATH is set to the location where you installed the CUDA Toolkit (default, /usr/local/cuda)

	export CUDA_INSTALL_PATH=/usr/local/cuda

	export PATH=$PATH:/$CUDA_INSTALL_PATH/bin

### build
	$cd GO_TO_ROOT_REPOSITORY/

	$source setup_environment

	$make

### run
	* copy the contents of v3.x/configs/GTX480/ or other devices to your applications' working directory.
	
	* in the configure.ocelot
		* trace: { memoryChecker: { enabled: true, checkInitialization: false, cta: 0}}, must be defined
		* "cta: 0" will print all traces made by CTA0
		* "cta: 9999" will print all traces made by all the CTAs

	source setup_environment

	run as usual
	
	* memory trace will be created and written to AppName_trace.txt


More detailed information you need can be found in README.original file.

Thank you.
