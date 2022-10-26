# olsap_lxd
LXD tweaks for the OLSAP project

snap install distrobuilder --classic
mkdir -p /root/ContainerImages/ubuntu

wget https://raw.githubusercontent.com/lxc/distrobuilder/master/doc/examples/ubuntu.yaml

Make copies and patch them to include necessary changes

cd /root/ContainerImages/ubuntu

ln -s ~/olsap_lxd/ubuntu_bionic.yaml .
ln -s ~/olsap_lxd/ubuntu_focal.yaml .

distrobuilder build-lxd ubuntu_bionic.yaml

