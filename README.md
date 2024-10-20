<!-- This was Created By Oumayma Guizeni  -->
<!-- Date : july 19, 2024 -->

<div align="center">

  <h3><b>Embedded Linux Development</b></h3>

</div>

---

[![C](https://img.shields.io/badge/C-%2300599C.svg?style=flat&logo=c&logoColor=white)](https://www.learn-c.org/)
[![Buildroot](https://img.shields.io/badge/Buildroot-%23orange.svg?style=flat&logo=buildroot&logoColor=white)](https://buildroot.org/)
[![Kernel](https://img.shields.io/badge/Kernel-%23000.svg?style=flat&logo=linux&logoColor=white)](https://www.kernel.org/)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://GitHub.com/Naereen/StrapDown.js/graphs/commit-activity)

---

<br>
<br>

# 📗 Table of Contents

- [Overview](#overview)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Tasks](#tasks)
- [FAQ](#faq)
- [License](#license)

<br>
<br>

---

# 📖  Overview <a name="overview"></a>

<p>This project encompasses various tasks related to embedded Linux development, including native and cross-compilation, adding system calls, writing kernel modules, and creating a minimal Linux distribution for BeagleBone using Buildroot.</p>

<br>
<br>

## 💻 Requirements <a name="requirements"></a>

List of dependencies and requirements needed to run the scripts:

- GCC (g++)
- Linux kernel headers
- Buildroot

<br>
<br>

## 🛠 Installation <a name="installation"></a>

Ensure you have the necessary dependencies installed:

1. **Install Buildroot**:
   Follow the [Buildroot documentation](https://buildroot.org/downloads.html) to download and set it up.

2. **Clone the repository**:

```bash
git clone https://github.com/OumaymaGuizeni/embedded-linux-development.git
cd embedded-linux-development
```

<br>
<br>

## 💻  Usage <a name="usage"></a>

1. **Native Compilation:** To compile native applications, use:

```bash
gcc prog.c -o prog
```
<!-- See Task 1: Native Compilation -->

2. **Cross-Compilation:** To compile applications for BeagleBone, use the cross-compiler toolchain:

```bash
arm-linux-gnueabi-gcc prog.c -o helloarm
```
<!-- See Task 2: Cross-Compilation -->

3. **Adding a System Call to the Linux Kernel:** To add a system call, follow these steps:
   
   a) Modify the kernel source code to add the new system call. Update the necessary files in the kernel, like syscalls.h and the architecture-specific syscall table.
   
   b) Recompile the kernel:
   ```bash
   make -j$(nproc)
   ```
   c) Install the new kernel and reboot:
   ```bash
   sudo make modules_install
   sudo make install
   sudo reboot
   ```
   d) Verify the new system call by writing a user program that calls the new syscall.
<!-- See Task 3: Adding a System Call to Linux Kernel -->

5. **Building the Kernel Module:** To build a kernel module, use:

```bash
make -C /lib/modules/$(uname -r)/build M=$(pwd) modules
```
<!-- See Task 4: Building the Kernel Module -->

6. **Creating a Minimal Linux with Buildroot:** Use the provided Buildroot configuration to create a minimal Linux image:

```bash
make menuconfig
make
```
<!-- See Task 5: Creating Minimal Linux with Buildroot -->

<br>
<br>

## 🔍 Tasks <a name="tasks"></a>

**Task 1:** Usage of native compiler

**Task 2:** Usage of cross-compiler

**Task 3:** Add a system call to the Linux kernel

**Task 4:** Write and build a kernel module

**Task 5:** Usage of Buildroot to create a minimal Linux distribution for BeagleBone

<br>
<br>

## ❓ FAQ <a name="faq"></a>

<p>If you have any questions, please feel free to reach out or create an issue in the repository.</p> 

<br> 
<br>

## 📝 License <a name="license"></a>

This project is proprietary, and all rights are reserved.

### Key Changes:
- **Task 3**: The steps for adding a system call to the Linux kernel are now detailed in the usage section. For more information, refer to the report, which includes all steps along with screenshots.

Feel free to make any additional adjustments or let me know if you need further modifications!
