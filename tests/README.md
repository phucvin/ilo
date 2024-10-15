sudo apt-get update
sudo apt-get install nasm ninja-build

build/ilo tests/add.ilo > tests/add.asm
nasm -felf64 tests/add.asm
ld tests/add.o -o tests/add
./add
echo $?