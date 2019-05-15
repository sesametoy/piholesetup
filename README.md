# pihole install
prepare
```
yum -y update
```
reboot
```
yum -y install epel-release
yum -y install wget mlocate git
```

```
sed -i "s/SELINUX=enforcing/SELINUX=permissive” /etc/sysconfig/selinux
```
install pihole
```
curl -sSL https://install.pi-hole.net | bash
```






# pihole setup

pihole setup file copy from https://github.com/jacyl4/de_GWD/

setup pihole setup file and DNS.

copy setup file to folder 

```
git clone https://github.com/sesametoy/piholesetup
```

```
cp savesetting.php /var/www/html/admin/scripts/pi-hole/php/savesettings.php
```

```
cp setupVars.conf /etc/pihole/setupVars.conf
```

```
cp 01-pihole.conf /etc/dnsmasq.d/01-pihole.conf
```
