# xv6OS
xv6 modified for OS class

This repository includes my study on XV6 Operating System
1. Adding a System call
    $ git clone https://github.com/iam-ram/OS-XV6.git xv6
    $ cd xv6
   
   To test system call I used virtuabox(https://www.virtualbox.org/) and vagrant(https://www.vagrantup.com/) combination to run XV6
    $ vagrant up
    $ cd /vagrant
    $ make; make qemu-nox
    
   More options to run XV6 with 'make'
    make qemu     - Build everything and run xv6 with QEMU, with a VGA console in a new window and the serial console in the terminal where you                         typed this command. Close the VGA window or press Ctrl-C or Ctrl-A X to stop.
    make qemu-nox - Run xv6 without the VGA console.
    make qemu-gdb - Run xv6 with GDB port open. Refer to the GDB section.
    make qemu-nox-gdb - Run xv6 with GDB port open, without the VGA console.
   http://www.cs.columbia.edu/~junfeng/11sp-w4118/tools.html 

2. Add kernel-level threading to make concurrency within a single user-level process. Also add basic synchronization mechanism - Mutex Lock - to make it thread safe

3. Improving the file system of XV6
    XV6 has 12 direct data block pointer and 1 single indirect block pointer. In this code its modified to contain 10 direct block, 2 single indirect block and 1 double indirect block pointer
    To test : run bigtest after loadind into XV6
    
Links: http://moss.cs.iit.edu/cs450/