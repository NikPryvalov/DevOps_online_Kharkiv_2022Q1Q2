## PART 1. HYPERVISORS
#### 1.Most popular hypervisors for infrastructure virtualization:
- VMware vSphere Hypervisor;
- Microsoft Hyper-V;
- Citrix XenServer;
- Oracle VirtualBox;
- Red Hat Enterprise Virtualization Hypervisor (REVH);
- KVM;
- Parallels;
- Qemu.

#### 2. The main differences of the most popular hypervisors:
  A hypervisor is a crucial piece of software that makes virtualization possible. It abstracts guest machines and the operating system they run on, from the actual hardware.
```  
- Type 1 Hypervisor (also called bare metal or native)
- Type 2 Hypervisor (also known as hosted hypervisors)

```
A bare-metal hypervisor (Type 1) is a layer of software we install directly on top of a physical server and its underlying hardware. There is no software or any operating system in between, hence the name bare-metal hypervisor.

Type 2 Hypervisor (also known as hosted hypervisors). This type of hypervisor runs inside of an operating system of a physical host machine.
This is why we call type 2 hypervisors – hosted hypervisors. As opposed to type 1 hypervisors that run directly on the hardware, hosted hypervisors have one software layer underneath. In this case we have:

- A physical machine.
- An operating system installed on the hardware (Windows, Linux, macOS).
- A type 2 hypervisor software within that operating system.
- The actual instances of guest virtual machines.

## PART 2. WORK WITH VIRTUALBOX
### 1.First run VirtualBox and Virtual Machine (VM).
- 1.1-1.4: 
![Снимок экрана (4)](https://user-images.githubusercontent.com/53264992/154538937-8f8e5bd4-ae07-4f22-bee9-ae8a777274ac.png)

