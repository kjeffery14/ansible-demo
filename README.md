# Ansible Demo Companion Files

## Build Suggestions

Operating System: Rocky, Alma Linux or CentOS 8

| Component | Ansible only | Ansible and AWX |
|:----|:----:|:----:|
| vCPU | 2 | 4 |
| Memory | 4GB | 8GB |
| HD | 40GB | 100GB |
| CDROM1 | AlmaLinux-8.3-x86_64-minimal.iso |
| CDROM2 | ansible.sample.com.iso |

## Kickstart Image

The kickstart ISO image contains a single file: ks.conf

This file tells the installer how to install and configure the Linux operating system.

## Installing Ansible

1.  Create an SSH key (or use an existing one)
    ```shell
    ssh-keygen -b 4096 -C ansible.sample.com
    ```
2.  Update the system
    ```shell
    sudo dnf update -y
    ```
3.  Install Python and Ansible
    ```shell
    sudo dnf install -y python3 ansible git
    ```
4.  Verify installation
    ```shell
    ansible --version
    ```
5.  Create a working directory for Ansible components and clone the ansible-demo repository
    ```shell
    sudo mkdir /ansible
    sudo chown ansible:ansible /ansible
    cd /ansible
    git clone https://github.com/kjeffery14/ansible-demo.git
    ```


## License

The contents of this repository are open-source under the Apache 2.0 licence.

```
Copyright 2019-2021 Kevin Jeffery

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
