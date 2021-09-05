#Steps:

       1. Download the source code:
                      $wget  https://cdn.kernel.org/pub/linux/kernel/v5.x/linux-5.13.13.tar.xz
                  
       2. Extract the kernel source
                      $ tar -xf linux-5.13.13.tar.xz
              Make the current directory to kernel source directory
                      $ cd linux-5.13.13/   
                      
       3. configure the kernel 
              A. copy the current kernel's config file
                      $ cp/boot/config-$(uname -r) .config
              B. Now configure
                      $ make menuconfig
                      
       4. Install the requirements
                      $ sudo apt-get install git fakeroot build-essential libncurses-dev xz-utils libssl-dev bc flex libelf-dev bison
                      
       5. Compile the kernel
                      $ make -j5
                     
       6. Install the modules
                      $ sude make modules_install
         
       7. Install the kernel
                      $ sude make install
                      
        8. Update GRUB and reboot
                      $ sudo update-grub
                      $ reboot
