## Remote Access for the MICRO-54 Vortex GPGPU tutorial

We have set up some temporary accounts for you to use the Vortex toolchain on the CRNCH Rogues Gallery at Georgia Tech. If you are interested to work with Vortex longer-term, you can request an account via our [CRNCH RG webpage](https://crnch-rg.cc.gatech.edu/request-access/).


For this tutorial you will be assigned a tutorial user number 1-60, and you will use this to login. The password will be shared by the tutorial organizers for the tutorial.

To login to the CRNCH server you will use the username **dac21_user|yournumber|** to log in to **hawksbill.crnch.gatech.edu**.

```
$ ssh dac21_user2@notebook.crnch.gatech.edu
dac21_user2@notebook.crnch.gatech.edu's password:
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 5.4.0-88-generic x86_64)

  System information as of Mon 18 Oct 2021 01:52:33 AM UTC
...
...
dac21_user2@hawksbill:~$
```

### Setting up the tutorial environment

Each user account will have access to two scripts that they can use to set their paths. One of these will already be run for you as part of your .profile file. 

```
$ source ~/dac-tutorial-2021/set_vortex_env.sh
```

The other script will pull the latest copy of the Vortex repo and the tutorial repo into your home directory. 

```
dac21_user2@hawksbill:~$ ~/dac-tutorial-2021/update_riscv_tut_repos.sh
Updating a local copy of the DAC RISC-V repo and the tutorial repo

dac21_user2@hawksbill:~$ ls
<TBD>
```

Once you have run this script, you can proceed to the hands-on exercises for the tutorial.
