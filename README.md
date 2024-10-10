### to run:

clone this repo, then

#### inside that folder:

git clone https://github.com/microsoft/vcpkg.git

cd vcpkg && ./bootstrap-vcpkg.sh

export PATH=$VCPKG_ROOT:$PATH

cmake --preset=default

cmake --build build

./build/vcpkg2

-
if it doesn't work it's probably bc the paths in the CMakePreset files are not correct for your system

caf actors example is from their examples folder

if you want this folder to be part of a larger git repo just delete the .git and .gitignore that's inside of this one
