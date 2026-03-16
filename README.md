
# Custom Linux Hardware Integration Masters class

This repo provides the manifest file for openembedded, required meta-layers and source code

## Install repo and prerequisites

    sudo apt install gawk wget git-core git-lfs diffstat unzip texinfo gcc-multilib \
     build-essential chrpath socat cpio python3 python3-pip python3-pexpect \
     xz-utils debianutils iputils-ping python3-git python3-jinja2 libegl1-mesa-dev libsdl1.2-dev \
     pylint xterm repo

## Fetch all required components

    repo init -u https://github.com/MicrochipTech/custom-linux-hardware-integration.git -b main
    repo sync

## Build the yocto image
    
    source openembedded-core/oe-init-build-env
    MACHINE=my-custom-sama7d65 bitbake my-sama7d65-image
