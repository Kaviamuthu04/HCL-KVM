###  vm_setup_notes.txt 

#  Virtual Machine Setup Notes  

## 1. Install KVM & Virtual Machine Manager
To install KVM on Ubuntu, run:

sudo apt update  
sudo apt install qemu-kvm libvirt-daemon-system libvirt-clients bridge-utils virt-manager -y

Verify installation:

kvm-ok

If it returns **"KVM acceleration can be used"**, then KVM is working.

## 2. Creating a Virtual Machine (VM)
1️⃣ Open **Virtual Machine Manager** (`virt-manager`)  
2️⃣ Click **"Create a New Virtual Machine"**  
3️⃣ Choose **Ubuntu 24.04 ISO**  
4️⃣ Allocate **RAM (e.g., 4GB)** and **CPU Cores (e.g., 2)**  
5️⃣ Install and complete setup  

## 3. Setting Up Shared Memory
To enable shared memory:
1️⃣ Edit `/etc/libvirt/qemu.conf`  
2️⃣ Find and enable:  

memory_backing_dir = "/dev/shm"

3️⃣ Restart libvirt:

sudo systemctl restart libvirtd

4️⃣ Use **shared_memory.c** to test shared memory communication.


### **Common Errors & Fixes**
| Issue | Solution |
|-------|---------|
| KVM not detected | Check if virtualization is enabled in BIOS |
| VM not starting | Use `virt-manager` logs for debugging |
| Shared memory issue | Ensure permissions are correct with `ipcs -m` |
