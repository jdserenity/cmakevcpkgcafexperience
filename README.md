### to run:

clone this repo, then

#### in current working directory:

git clone https://github.com/microsoft/vcpkg.git

cd vcpkg && ./bootstrap-vcpkg.sh

export PATH=$VCPKG_ROOT:$PATH

cmake --preset=default

cmake --build build

./build/vcpkg2

if it doesn't work it's probably bc the paths in the CMakePreset files are not correct for your system

caf actors example is from their examples folder
