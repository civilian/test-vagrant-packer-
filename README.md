Instalation
------------
Install vagrant: http://www.vagrantup.com/downloads
install packer: https://docs.google.com/document/d/1fmamUqgf80tPGBMKH0xj80sdEJgrmWJ6yQbx45qTqAc/edit#bookmark=id.p1yx1sqflgs6

Run:
Add the debian/jessie64 box to be abble to modify it.
$ vagrant box add debian/jessie64 --provider virtualbox
https://atlas.hashicorp.com/debian/jessie64
Delete what we don't need
$ rm -rf output-virtualbox-ovf
Build the actual image:
$ packer build packer.json
And added with the name debian-vagrant-development to be able to use the Vagrantfile present.
$ vagrant box add --name debian-vagrant-development box/modified-debian-VAGRANTSLASH-jessie64 

Tutorial: http://stackoverflow.com/questions/31255737/create-a-vm-image-from-a-vagrant-box-using-packer
Adding the box: http://stackoverflow.com/questions/10859590/downloaded-vagrant-box-file-but-what-to-do-with-it