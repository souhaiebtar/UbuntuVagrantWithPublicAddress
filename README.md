# Ubuntu Vagrant with public network

prepare a ubuntu Virtual machine (VM) via vagrant and Ansible.

the VM will appear on your network as a local machine.

## Dependencies

Make sure you have the following dependencies installed:

* [VirtualBox](https://www.virtualbox.org)
* [Vagrant](https://www.vagrantup.com)
* [Ansible](https://www.ansible.com)

## Usage

1. Clone this repository.

2. Switch to the repository directory.

3. In the directory, run:

        vagrant up
        
4. Vagrant will prompt you to choose an interface to bridge to the local network. In general, choose the ethernet connection if the host machine is wired, but WiFi is fine to. For example:

    ```
    ==> pihole: Available bridged network interfaces:
    1) enp0s25
    2) br-5a8f6827ab14
    3) docker0
    4) br-4ec60aaeb8fe
 
