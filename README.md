# GPU Memory Tracer
It is implemented based on GPGPU-Sim simulator, which is a detailed cycle-accurate simulator that simulates GPU devices. If you need more information on this simulator, please check README.original.

## Installing, Building and Running this program
### CUDA Toolkit must be setup (it is recommended to use version 3.1 for normal PTX simulation and version 4.0 for cuobjdump)

### dependency settings for Ubuntu users
* sudo apt-get install build-essential xutils-dev bison zlib1g-dev flex libglu1-mesa-dev
* sudo apt-get install libxi-dev libxmu-dev libglu3-dev

make sure CUDA_INSTALL_PATH is set to the location where you installed the CUDA Toolkit (default, /usr/local/cuda)

	export CUDA_INSTALL_PATH=/usr/local/cuda

	export PATH=$PATH:/$CUDA_INSTALL_PATH/bin

### build
$cd CD_TO_REPOSITORY/

$source setup_environment

$make

### run
* copy the contents of v3.x/configs/GTX480/ or other devices to your applications' working directory.
* source setup_environment
* run as usual


###
xxxxxxxxxx
More detailed information you need can be found in README.original file.

Thank you.
