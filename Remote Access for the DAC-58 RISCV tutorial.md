## Remote Access for the DAC 2021 tutorial

**NOTE:** These instructions are just provided for informational purposes. They will not work without an active testbed account!

We set up some temporary accounts for you to use the SystemArchitect CoreGen toolchain on the CRNCH Rogues Gallery at Georgia Tech. If you are interested to work with SystemArchitect longer-term, you can request an account via our [CRNCH RG webpage](https://crnch-rg.cc.gatech.edu/request-access/).

Users logged into the CRNCH server hawksbill for this tutorial. 

### Setting up the tutorial environment

Each user account will have access to a few different scripts. To start, run this update script to pull the other tools and repos into your home directory.

```
dac21_user2@hawksbill:~$ ~/dac-tutorial-2021/update_dac_tut_repos.sh  
Updating a local copy of the CoreGen repo and the tutorial repo

dac21_user2@hawksbill:~$ ls
build_coregen_from_repo.sh  //A script that runs cmake, make, and make install to create a local install of Coregen
CoreGen                     //A copy of the CoreGen repo
dac-tutorial-2021           //Symlink to the tutorial master folder; you should need to do anything with this!
riscv-tutorial-dac-21       //Use the .yaml file under Exercises for the hands-on portion.
set_tut_env_precompiled.sh  //source this script if you want to skip building CoreGen
```

Once you have run this script, you can proceed to the hands-on exercises for the tutorial.

#### Further scripts for remote access
If you'd like to build Coregen from source, you can run the following script which runs cmake and make:

```
dac21_user1@hawksbill:~$ ./build_coregen_from_repo.sh
Running cmake on the CoreGen repo                                                                                                                       
-- The C compiler identification is GNU 9.3.0
...
-- Build files have been written to: /home/dac21_user1/CoreGen/build
Running make -j4 to build in parallel
...
[ 98%] Built target cgcli
[100%] Linking CXX executable sccomp
[100%] Built target sccomp
```

If you have trouble with this step and just want to set your paths to a working version of the tools, source this script.
```
dac21_user1@hawksbill:~$ source set_tut_env_precompiled.sh
PATH=/netscratch/dac-tutorial-2021/coregen-install/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
LD_LIBRARY_PATH = /netscratch/dac-tutorial-2021/coregen-install/lib/

#Check to see that you have the right path to the cgcli tool
dac21_user1@hawksbill:~$ which cgcli
/netscratch/dac-tutorial-2021/coregen-install/bin/cgcli
```


### DAC Tutorial Exercises
We will be using the BasicRV32I.yaml file shared in the Exercises folder of this repo. On the remote server you can switch directories to a copy of this directory and then run the hands-on commands.

```
dac21_user1@hawksbill:~$cd ~/cd riscv-tutorial-dac-21/Exercises/
dac21_user1@hawksbill:~$ ls
BasicRV32I.yaml
#Proceed to run cgcli commands for the hands-on portion of the tutorial!
```

