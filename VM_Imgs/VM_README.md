
## Virtual Machine Instructions
For this tutorial, we provide access to a remote server with the tools as well as a virtual machine
image that contains the prebuilt version of the tools as well as the Coregen git repo. This VM is
built using Vagrant with a VirtualBox Provider, which means that it should be easy to run on most platforms.

We also provide the base Vagrantfile we use if you would want to try and build your own image from scratch.

### Important note for Apple Macbook M1 users
VirtualBox is not supported on M1 laptops and systems due to the switch from an x86 to aarch64 processor.
You can technically use a Vagrantfile with Docker, but we haven't tested this and can't confirm that it
works as expected. Success would depend on whether all the required packages can be installed for aarch64 
in the underlying Docker container. [Here](https://app.vagrantup.com/jeffnoxon/boxes/ubuntu-20.04-arm64) 
is one possible Vagrant setup that could be investigated if you are interested.

For this tutorial, we recommend using the remote server rather than the local VM if you only have local
access to an M1 or similar device.

## VM Usage Instructions

**First** you will need to install [Vagrant](https://www.vagrantup.com) and [VirtualBox](). We have tested
on Linux and Windows 10 with Vagrant 2.2.18 and VirtualBox 6.1.26.

### Vagrant set up and initialization

* [Vagrant Box with prebuilt toolchains and Coregen repo (1.1 GB)](https://gatech.box.com/s/7cb39gs0jlokg8mh29khsnbteefhpqy7)
* [Vagrantfile - place in the same folder as your .box file](Vagrantfile)

#### Tutorial Setup - All Platforms
Once you have booted your VM from the instructions below, you should follow these steps to prepare for the hands-on portion of the tutorial:

* Source the `set_riscv_env.sh` script to set your paths
* Proceed to the Exercises section of this repo.

#### Windows Setup

1) Download the tutorial Vagrant Box image ([from Box](https://gatech.box.com/s/7cb39gs0jlokg8mh29khsnbteefhpqy7)) and the updated Vagrantfile ([from this repo](Vagrantfile)) to your computer
    * Note that the VM box image is **1.1 GB**, and it requires **4 GB of local disk space** and 2 CPU cores. 
    * The VagrantFile includes some tweaks to disable serial adapters which can cause a boot error.
    * If you need to increase/decrease the number of cores used by the VM, you can also make this change in the Vagrantfile. 

2) Import the Vagrant Box image using the command-line and start the VM

```
# We create a new local VM image from the riscv-coregen-ubuntu2004 .box file and 
# then initialize a Vagrantfile with `vagrant init`

v
vagrant up
```

Once it completes booting and returns back to the command prompt you can ssh into the VM. Note that the images here are from a slightly different tutorial but the steps should be the same.

![Successful Boot Screen Win10](screenshots/windows/vagrant_tutorial_windows10_2.png)

```
vagrant ssh
```

3) When you are finished working with the VM, make sure to exit your session and run `vagrant halt` to power
the VM down. It is preferred to halt the VM with Vagrant than using the VirtualBox manager to power down the VM 
due to the additional setup steps that Vagrant performs.

![Successful Exit Win10](screenshots/windows/vagrant_tutorial_windows10_3.png)

Note that you can see and log into the VM using the VirtualBox Manager GUI. Just remember to start/stop the image with
Vagrant, if possible.

![VirtualBox Example Win10](screenshots/windows/vagrant_tutorial_windows10_4.png)

#### Linux Setup (Ubuntu 18)

Install Vagrant and Virtualbox using either the downloads above or by using apt.

```
apt install vagrant virtualbox
```

Then you will follow the same steps as above for the Windows setup.

2) Import the Vagrant Box image using the command-line and start the VM

```
# We create a new local VM image from the vortex-ubuntu18 .box file and 
# then initialize a Vagrantfile with `vagrant init`

vagrant box add riscv-dac21 riscv-coregen-ubuntu2004.box
vagrant init riscv-dac21
vagrant up
```
