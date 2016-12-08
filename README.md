# Packstack-install-openstack


[https://www.rdoproject.org/install/quickstart/](https://www.rdoproject.org/install/quickstart/)
```shell
sudo su -
yum install -y https://www.rdoproject.org/repos/rdo-release.rpm
yum update -y
yum install -y openstack-packstack
packstack --allinone
```

* These steps above will install OpenStack all in one, with default modules.

## Tips:
1. If it is installed on a VM, then should modify below config for packstack:
```
vi /root/packstack-answers-20161122-005249.txt
```
* CONFIG_NOVA_LIBVIRT_VIRT_TYPE=qemu

then run below command:
```
packstack --answer-file packstack-answers-20161122-005249.txt
```

2. If you want to enable non-default module of OpenStack:
```
vi /root/packstack-answers-20161122-005249.txt
```
* CONFIG_HEAT_INSTALL=y

then run below command:
```
packstack --answer-file packstack-answers-20161122-005249.txt
```

