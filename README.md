# Learning to write an OS

Ref: https://youtu.be/s_4tFz52jbc

## Getting started

Install RISC-V Toolchain from https://github.com/riscv-collab/riscv-gnu-toolchain

Install Qemu

Ref: https://www.qemu.org/docs/master/system/riscv/virt.html


Refer [riscv/virt.c](https://github.com/qemu/qemu/blob/master/hw/riscv/virt.c) for memory addresses


## Running qemu

```sh
qemu-system-riscv64 -M virt 
    -smp 4 \                                # 4 Hardware Cores
    -m 2G \                                 # RAM 2GB
    -display none \                         # No Graphics, mayebe hook something later
    -serial stdio \                         # Serial interface
    -kernel kernel.elf \                    # Kernel
    #-initrd /path/to/rootfs.cpio \          #
    #-append "root=/dev/ram"                 #
```