---
layout: post
title: Force processes to use swap in memory
date: 2020-03-31 22:30:00 +0100
author: Bart Cox
description: Limit memory for a process to force it to be swapped
img: memory_monitor.png # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [cgroups, linux, memory, swap]
---
# Force processes to swap memory (Ubuntu 18.04)

When benchmarking processes, looking how a process perform when swapping memory can be useful. Since the operating system determines the memory allocation policy, testing with limited memory can be cumbersome. One could try to fill the virtual memory with other processes to limit the available memory but since the operating system tries to swap inactive processes, our benchmarked process will probably remain in virtual memory. In any case, we cannot know this for certain.

## Cgroups

Cgroups (control groups) let us control limit and control the resource usage of a group of processes in Linux.

To enable cgroups the cgroup-bin package has to be installed.

```bash
sudo apt-get install cgroup-bin
```

Some distributions (Ubuntu e.g.) has the `memsw` property of cgroups not enabled by default. To enable this we need to change the grub configuration. Alter the grub file in `/etc/default/grub` so the `GRUB_CMDLINE_LINUX_DEFAULT` is set to `GRUB_CMDLINE_LINUX_DEFAULT="cgroup_enable=memory swapaccount=1"`. Make sure to run `sudo update-grub` and reboot the machine.

## Create swap file

If necessary, you can increase the size of the swap file. To check the current size of the swap file `grep SwapTotal /proc/meminfo`.

* Turn off swapping `sudo swapoff -a`
* Resize the swap file `sudo dd if=/dev/zero of=/swapfile bs=1G count=8`. This example creates a file of 8GB.
* Mark file as swapfile `sudo mkswap /swapfile`
* Activate the swapfile `sudo swapon /swapfile`
* Enable swapping `sudo swapon -a`

## Run process with limited memory

To constrain the process in its resources we create a new cgroup and set the memory limits for both the virtual memory and the swap memory. 

<script src="https://gist.github.com/bacox/e2d15cd8453e32f66aeed4507699e032.js"></script>

The system monitor can be used the check if the cgroup is working correctly and actually is forcing the program to use swap memory.

When a program tries to allocate more memory than is available in the swap file, the OOM killer (if enabled) will still send a SIGKILL and ends the program.