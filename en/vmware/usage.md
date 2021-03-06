
# Usage

The Vagrant VMware providers are used just like any other provider. Please read the general [basic usage][basic-usage] page for providers.

The value to use for the `--provider` flag is `vmware_fusion` for VMware Fusion, and `vmware_workstation` for VMware Workstation.

The Vagrant VMware provider does not support parallel execution at this time. Specifying the `--parallel` option will have no effect.

To get started, create a new `Vagrantfile` that points to a VMware box:
```
# vagrant init hashicorp/precise64
Vagrant.configure(2) do |config|
  config.vm.box = "hashicorp/precise64"
end
```
VMware Fusion users should then run:
```
$ vagrant up --provider vmware_fusion
```
VMware Workstation users should then run:
```
$ vagrant up --provider vmware_workstation
```
This will download and bring up a new VMware Fusion/Workstation virtual machine in Vagrant.

> **Note:** At some point in the future, the providers will probably be merged into a single `vagrant-vmware` plugin. For now, the Workstation and Fusion codebases are different enough that they are separate plugins.

[basic-usage]: https://docs.vagrantup.com/v2/providers/basic_usage.html