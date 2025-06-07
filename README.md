# OpenCCA
>
> OpenCCA: An Open Framework to Enable Arm CCA Research  
> (SysTEX '25)  
> https://opencca.github.io/

### Overview
Confidential computing has gained traction across major architectures with Intel TDX, AMD SEV-SNP, and Arm CCA. Unlike TDX and SEV-SNP, a key challenge in researching Arm CCA is the absence of hardware support, forcing researchers to develop ad-hoc performance prototypes on non-CCA Arm boards. This approach leads to duplicated efforts, inconsistent performance comparisons, and high barriers to entry. 

To address this, we present **OpenCCA**, an open research platform that enables the execution of CCA-bound code on commodity Armv8.2 hardware. By systematically adapting the software stack -- including bootloader, firmware, hypervisor, and kernel -- OpenCCA emulates CCA operations for performance evaluation while preserving functional correctness.

We demonstrate its effectiveness with typical life-cycle measurements and case-studies inspired by prior CCA-based papers on a easily available Armv8.2 Rockchip board that costs $250.

```bibtex
@inproceedings{opencca,
  title     = {{OpenCCA}: An Open Framework to Enable Arm CCA Research},
  author    = {Andrin Bertschi and Shweta Shinde},
  year      = 2025,
  booktitle = {8th Workshop on System Software for Trusted Execution (SysTEX 2025)},
}
```

### Repositories
> ⚠️ **Open sourcing our artifacts is currently work in progress**

The [OpenCCA Github Organization](https://github.com/opencca) hosts all of our source repositories.



**Setup and Build**:
| Repository                                                            | Description                                  |
|-----------------------------------------------------------------------|----------------------------------------------|
|[opencca-manifest](https://github.com/opencca/opencca-manifest)        | Repo Manifest with all repositories          |
|[opencca-build](https://github.com/opencca/opencca-build)              | Setup to build all firmware components       |
|[opencca-flash](https://github.com/opencca/opencca-flash)              | Setup to flash firmware onto RK3588 SoC      |
|[opencca-assets](https://github.com/opencca/opencca-assets)            | Static Assets RK3588                         |
|[debian-image-recipes](https://github.com/opencca/debian-image-recipes)| Tools to build root filesystem for RK3588    |

**Software Components**:
| Repository                                                            | Description                                  |
|-----------------------------------------------------------------------|----------------------------------------------|
|[arm-trusted-firmware](https://github.com/opencca/arm-trusted-firmware)| Arm TF-A                                     |
|[tf-rmm](https://github.com/opencca/tf-rmm)                            | Realm Management Monitor (TF-RMM)            |
|[kvmtool](https://github.com/opencca/kvmtool)                          | Kvmtool VMM                                  |
|[linux](https://github.com/opencca/linux)                              | CCA Enlightened Host/Guest Kernels           |
|[u-boot](https://github.com/opencca/u-boot)                            | Second Stage Loader UBoot                    |


### Getting Started

This project is currently in early development. Documentation and build instructions are evolving rapidly. Please be patient and check back regularly for updates.

For initial setup and build instructions, please refer to the [opencca-build](https://github.com/opencca/opencca-build) repository README.
