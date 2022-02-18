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
#### - 1.1-1.4: 
![Снимок экрана (5)](https://user-images.githubusercontent.com/53264992/154542040-edee4e42-b62f-4fe4-a108-d8e8637e0e25.png)
![Screenshot from 2022-02-18 12-00-59](https://user-images.githubusercontent.com/53264992/154661685-5b363d84-2afa-49c1-bddc-baf021aad838.png)

#### - 1.5:
![Снимок экрана (8)](https://user-images.githubusercontent.com/53264992/154558339-4aa92891-d571-40b8-8e18-78e1fa31db14.png)

#### - 1.6:
![Screenshot from 2022-02-18 12-11-42](https://user-images.githubusercontent.com/53264992/154662589-05347fb4-50bf-403a-87c9-f554fcb822ac.png)

#### - 1.7:
![Screenshot from 2022-02-18 12-15-02](https://user-images.githubusercontent.com/53264992/154663100-d6fd9302-160b-4421-ac4a-23527106f2d4.png)

#### - 1.8:
![Screenshot from 2022-02-18 13-50-25](https://user-images.githubusercontent.com/53264992/154678104-114b5e5a-7ee3-428f-8b45-bb21cfeb2b14.png)

#### - 1.9:
![Screenshot from 2022-02-18 13-57-37](https://user-images.githubusercontent.com/53264992/154679703-79475862-6d27-420f-af2a-dff9542986c7.png)
![Screenshot from 2022-02-18 13-59-02](https://user-images.githubusercontent.com/53264992/154679717-657feb17-0a95-45a9-80e8-b8af4bd75cf9.png)
![Screenshot from 2022-02-18 13-59-19](https://user-images.githubusercontent.com/53264992/154679733-f88fb626-ca60-4369-827e-3f2bd402fcba.png)
![Screenshot from 2022-02-18 14-03-01](https://user-images.githubusercontent.com/53264992/154679741-51453b04-1728-4930-9f6c-07af26535ab7.png)
![Screenshot from 2022-02-18 14-06-04](https://user-images.githubusercontent.com/53264992/154680586-5622246a-42de-40f0-a5d1-95f18b628dc0.png)
![Screenshot from 2022-02-18 14-06-16](https://user-images.githubusercontent.com/53264992/154680594-873d72f4-9a07-4c88-bde2-27d438a897de.png)
![Screenshot from 2022-02-18 14-07-11](https://user-images.githubusercontent.com/53264992/154680608-979a84a6-3268-4034-b1cf-d8ae0c9ad8e1.png)
![Screenshot from 2022-02-18 14-07-34](https://user-images.githubusercontent.com/53264992/154680621-2eca8f4d-f70c-4782-88b3-9e429fbb4422.png)

### 2.Configuration of virtual machines
#### 2.1:
![Screenshot from 2022-02-18 14-13-36](https://user-images.githubusercontent.com/53264992/154681213-d5abcec5-f291-4a8e-a563-be6873f6e7b8.png)
![Screenshot from 2022-02-18 14-13-51](https://user-images.githubusercontent.com/53264992/154681246-81b82750-5d93-461e-b999-e049530cfdea.png)
![Screenshot from 2022-02-18 14-14-04](https://user-images.githubusercontent.com/53264992/154681254-f0c5c6f4-6e68-4954-85cf-e56889cdde3e.png)
![Screenshot from 2022-02-18 14-14-15](https://user-images.githubusercontent.com/53264992/154681270-7002d151-b628-48ca-a95c-151bafe192e4.png)
![Screenshot from 2022-02-18 14-14-24](https://user-images.githubusercontent.com/53264992/154681295-354082f6-6047-405c-88a5-559ef28061dd.png)
![Screenshot from 2022-02-18 14-14-33](https://user-images.githubusercontent.com/53264992/154681304-d28bf982-9eb0-4431-bbc9-57a194455c89.png)

#### 2.2:
![Screenshot from 2022-02-18 14-45-31](https://user-images.githubusercontent.com/53264992/154686815-a62a1039-4ba4-46f1-8239-12c50584bfe7.png)
 
#### 2.3:

#### 2.4:
![Screenshot from 2022-02-18 15-52-03](https://user-images.githubusercontent.com/53264992/154695372-d5083c1b-5bd6-4946-9a16-87681cf4cdff.png)
![Screenshot from 2022-02-18 15-52-17](https://user-images.githubusercontent.com/53264992/154695382-612dee48-43cc-4d9c-9732-3264c0e9c015.png)



![Screenshot from 2022-02-18 15-52-03](https://user-images.githubusercontent.com/53264992/154695420-4ab87ed0-cef9-41e7-8de2-eaa1a1c6a60b.png)
![Screenshot from 2022-02-18 15-52-28](https://user-images.githubusercontent.com/53264992/154695430-020059de-24c7-479b-9bbd-c74ee13f29ab.png)



![Screenshot from 2022-02-18 15-52-03](https://user-images.githubusercontent.com/53264992/154695453-1c41e3e2-1bd2-4ee3-a155-7e5a5f619bfa.png)
![Screenshot from 2022-02-18 15-52-36](https://user-images.githubusercontent.com/53264992/154695485-fa4b0081-2164-4c13-976c-e00af1702afd.png)



![Screenshot from 2022-02-18 15-52-03](https://user-images.githubusercontent.com/53264992/154695502-b7aa9a65-cbc1-4c7e-8289-dcc68235c752.png)
![Screenshot from 2022-02-18 15-52-47](https://user-images.githubusercontent.com/53264992/154695517-47512211-f868-43d1-907f-d0bdb04f06b1.png)



![Screenshot from 2022-02-18 15-52-03](https://user-images.githubusercontent.com/53264992/154695532-699879f5-aa32-4b56-9369-ae8070e7d387.png)
![Screenshot from 2022-02-18 15-52-56](https://user-images.githubusercontent.com/53264992/154695563-8e98a521-af75-43ac-8a36-64ee6f77cde4.png)



### 3.Work with CLI through VBoxManage.
#### 3.1:
![Screenshot from 2022-02-18 16-27-07](https://user-images.githubusercontent.com/53264992/154701097-a7803cc6-d9e5-4a5c-9fc2-c867d1cbc8e0.png)



