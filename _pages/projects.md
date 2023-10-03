---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true

---

My work focuses on system behavior understanding, testing, and debugging:

* Non-Volatile Memories
![Non-Volatile Memories](/images/nvm.jpg)
    Non-volatile memory (NVM) technologies, such as flash-based solid-state drives (SSD) and byte-addressable persistent memories (PM), wield significant influence over contemporary storage systems. Regrettably, constructing a resilient modern system incorporating these innovative devices is a time-consuming endeavor due to the radical changes in the software stack and the complexity of accurately comprehending system behavior. To address these challenges, our approach entails the aggregation of kernel bug cases, along with the utilization of cutting-edge technologies like virtual machines and static analysis for system analysis:
    1. We automated the collection of patches related to persistent memory within the Linux kernel tree and subjected these patches to in-depth analysis. This comprehensive study allowed us to extract various insights into persistent memory bugs, subsequently contributing to the development of multiple persistent memory system bug detection methodologies.
    2. We leveraged virtual machine (QEMU) to reproduce persistent memory-related bug cases and provided extra plugins to improve debugging support.
    3. Employing a static analyzer based on LLVM, we conducted both inter and intra function analyses to scrutinize persistent memory drivers, thereby uncovering several potential vulnerabilities.
    4. Leveraging pre-existing persistent memory bug cases, we evaluated various methods of emulating persistent memory and identified potential emulation-related challenges.
    5. Employing virtual machines, we simulated power failures to examine crash consistency issues within non-volatile memory systems. This investigation led to the identification of multiple vulnerabilities in this context.

* Local File System (e.g, EXT4 and XFS) & Utilities
![Local File System](/images/local.jpg)
    Local file systems remain a pivotal component of storage systems. To align with the demands of modern systems and applications, local file systems have undergone significant evolution, introducing numerous features. However, these changes have given rise to multiple vulnerabilities and the potential for unforeseen consequences, such as data loss, server downtime, and system crashes. Our comprehensive approach encompasses studies and testing across various dimensions:
   1. We initiated our efforts by amassing instances of local file system issues from Bugzilla and the Linux kernel source tree. Subsequently, we recreated select real-world system failures. Our experiments, coupled with detailed analyses, culminated in the identification of several pivotal reproducibility patterns within these issue cases.
   2. To gain insights at the kernel level, we harnessed established tracers like Strace, FTrace, SystemTap, and perf to capture relevant system data. Additionally, we employed scsi-tool to record device commands. This dual-source information allowed us to introduce a novel cross-layer diagnostic method.
   3. Our innovation extended to modifying the virtual machine structure to capture device commands and instructions. This led to the development of a comprehensive, cross-layer diagnostic approach that covers the entire stack. Our experiments corroborated the effectiveness of this method, as it streamlines the process of comprehending system behavior and isolating root causes.
   4. Leveraging static analysis by LLVM, we systematically extracted dependencies within file system configurations. Subsequently, we conducted testing using five different adapted existing tools. These experiments were instrumental in uncovering various local file system issues.

* Parallel File System (e.g., BeeGFS)
![Parallel File System](/images/pfs.jpg)
    Parallel storage systems find extensive deployment in data centers and national laboratories, facilitating data-intensive computing tasks. Nonetheless, issues related to correctness and scalability can lead to unforeseen problems, such as data loss and system unresponsiveness. To address these concerns, we have developed a framework for conducting a taxonomy of parallel file systems:
    1. Our initial step involved a thorough examination of the structures and documented bug cases within parallel file systems. This analysis allowed us to pinpoint several potential scenarios of concern.
    2. Subsequently, we devised a series of experiments aimed at generating inconsistency scenarios and assessing the ability of parallel file systems to respond appropriately and execute correct recovery procedures.
   


