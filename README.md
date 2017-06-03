# vagrantcuda
Vagrant file and playbook to install ubuntu 16.04 vim + pci passthru nvidia gpu + tensorflow-gpu

## How to use

* Install vagrant, virtualbox and virtualbox extentions

* Edit PCI device id in Vagrantfile

* Download cudnn and copy it to repo dir

```
cp ~/Downloads/cudnn-8.0-linux-x64-v5.1.tgz vagrantcuda
```

* Run vagrant up
