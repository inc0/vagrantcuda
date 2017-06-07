# vagrantcuda
Vagrant file and playbook to install ubuntu 16.04 vim + pci passthru nvidia gpu + tensorflow-gpu

## How to use

* Install vagrant, vagrant-libvirt and libvirt stack

* Edit PCI device id in Vagrantfile
```
    domain.pcis = [{
        bus: 2,
        slot: 0,
        function: 0,
    }]
```

* Download cuDNN v5.1 for Linux (you need to create account there)
```
https://developer.nvidia.com/rdp/cudnn-download
```

* Copy downloaded file to repo dir
```
cp ~/Downloads/cudnn-8.0-linux-x64-v5.1.tgz vagrantcuda
```

* Run
```
vagrant up
```
