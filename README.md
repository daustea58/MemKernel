MemKernel

MemKernel is a kernel driver for Android. Originally created by "Jiang-Night" (https://github.com/Jiang-Night/Kernel_driver_hack), it has been modified and fixed according to my personal needs.

Integration

There are 2 ways to integrate this driver into your kernel source using the setup script:

Y — Built-in Kernel

Build the driver as part of the kernel (statically built into the kernel).

curl -LSs "https://raw.githubusercontent.com/Poko-Apps/MemKernel/main/kernel/setup.sh" | bash -s Y

M — Loadable Kernel Module (LKM)

Build the driver as a loadable kernel module.

curl -LSs "https://raw.githubusercontent.com/Poko-Apps/MemKernel/main/kernel/setup.sh" | bash -s M

Custom Driver Name

TIP: By default, the setup script generates a random name for the driver ("/dev/*randomname*") and the LKM ("*randomname*_memk.ko").

You can override this behavior by providing a second argument to the setup script:

curl -LSs "https://raw.githubusercontent.com/Poko-Apps/MemKernel/main/kernel/setup.sh" | bash -s M myname
