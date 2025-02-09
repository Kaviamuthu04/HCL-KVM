# 🖥️ HCL-KVM-Virtualization  

## 🔥 Project Overview  
This project focuses on setting up **KVM-based Virtual Machines** with **shared memory communication** between guest OS instances. It is part of my **HCL Internship**, where I explored Linux virtualization and system performance testing using LTP (Linux Test Project).  

## ⚙️ **Key Features**  
- ✅ **Guest OS Installation** using KVM  
- ✅ **Shared Memory Setup** between guest and host  
- ✅ **Inter-VM Communication** using IPC mechanisms  
- ✅ **Performance Benchmarking** with LTP
  
## 🚀 **Installation & Setup**  
### 1️⃣ **Install KVM on Linux**  

sudo apt update
sudo apt install qemu-kvm libvirt-daemon-system virt-manager -y

2️⃣ Verify KVM Installation

kvm-ok

If you see:

KVM acceleration can be used

It means KVM is successfully installed! 

3️⃣ Launch Virtual Machine (VM) Manager

virt-manager

    Click "Create New Virtual Machine"
    Choose ISO file for the guest OS
    Allocate CPU & RAM
    Finish the setup and start the VM 🎯
