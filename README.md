# Overview
This is just some test files to try out booting off them.

You require a virtual machine to boot these images.

## Setup
1. install virtualbox
2. for asm demos, install nasm

## Building an image from an assembly file
1. First assemble the image using nasm:
	nasm -o img/helloworld.img asm/helloworld.asm	
2. Add the img as a virtual floppy disk in VirtualBox
3. Start the virtual machine

## Troubleshooting
I didn't find this necessary, but to compile as a complete disk file, use dd:
	dd if=bootdisk.img of=bootdisk.raw bs=1440k

