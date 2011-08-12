# Overview
This is just some test asm files to try out booting off them.

You require a virtual machine to boot these images.

## Setup
1. install virtualbox
2. install nasm

## Building an image from an assembly file
1. First assemble the image using nasm:
	nasm -o img/helloworld.img src/helloworld.asm	
2. Add the img as a virtual floppy disk in VirtualBox
3. Start the virtual machine

## Troubleshooting
I didn't find this necessary, but to compile as a complete disk file, use dd:
	dd if=bootsectorprog.img of=bootdisk.raw bs=1440k
