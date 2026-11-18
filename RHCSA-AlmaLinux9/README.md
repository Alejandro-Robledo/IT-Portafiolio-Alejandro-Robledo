# RHCSA Lab — AlmaLinux 9

## Overview

This repository documents my practical training in Linux system administration using AlmaLinux 9 and a virtualized laboratory environment.

The main objective is to develop hands-on skills in Linux administration, system configuration, networking, storage management, security, troubleshooting and automation, following the Red Hat Enterprise Linux 9 administration objectives.

This project is part of my IT professional development and practical portfolio.

## Lab Environment

| Component | Configuration |
|---|---|
| Host OS | Windows |
| Virtualization | Oracle VirtualBox |
| Provisioning | Vagrant |
| Linux Distribution | AlmaLinux 9.9 |
| Server VM | RHCSA-server-lab-new |
| Client VM | RHCSA-client-lab-new |
| Server RAM | 2 GB |
| Client RAM | 1 GB |
| Server disk | 19.5 GB |
| Client disk | 19.5 GB |

## Network Configuration

The laboratory uses two network interfaces per virtual machine:

- NAT: Internet connectivity.
- Host-Only: Private communication between the host and virtual machines.

| Machine | Host-Only IP |
|---|---|
| Host | 192.168.56.1 |
| Server | 192.168.56.10 |
| Client | 192.168.56.11 |

## Initial System Verification

The initial inspection confirmed:

- Both virtual machines are running successfully.
- AlmaLinux 9.9 is installed on both machines.
- Both systems use the Linux 5.14 kernel.
- Network interfaces are active.
- Main disks are detected correctly.
- System resources are available.

### Initial observations

The following service was reported as failed on both virtual machines:

`NetworkManager-wait-online.service`

This issue is pending investigation and will be addressed during the networking module.

## Learning Roadmap

1. Linux Fundamentals and Filesystem Hierarchy
2. Users, Groups and Permissions
3. Process and Service Management
4. Storage and Filesystem Administration
5. Network Configuration and Troubleshooting
6. Package Management and System Services
7. Linux Security: SELinux and Firewalld
8. Bash Scripting and Automation
9. Integrated Administration Exercises and RHCSA Practice

## Documentation Methodology

Each practical exercise will include:

- Objectives and technical concepts.
- Commands and configuration procedures.
- Practical results and verification.
- Screenshots and supporting evidence.
- Troubleshooting notes.
- Conclusions and lessons learned.

All screenshots and results will come from actual laboratory exercises.

## Project Status

**Current stage:** Initial laboratory verification completed.  
**Next step:** Linux filesystem hierarchy and essential command-line tools.
