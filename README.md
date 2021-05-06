# packer-ubuntu-20.04

## About

A Packer template to create Ubuntu 20.04 "Focal Fossa" Server boxes for Vagrant.

## Usage

Install ansible requirements.

```sh
pip3 install -r requirements.txt
```

To create VirtualBox virtual machine.

```bash
packer build -on-error=ask ubuntu-vbox.json
```

To create Hyper-V virtual machine. (Not updated probably won't work)

```sh
packer build ubuntu-hyperv.json
```

## Create Password for cloud-init autoinstall

```sh
docker run -it --rm alpine mkpasswd --method=sha512 ubuntu
```
