# VICIDIAL INSTALLATION SCRIPTS
# Centos vididial Install pre_requisites 

```
yum check-update
yum update -y
yum -y install epel-release
yum update -y
yum groupinstall 'Development Tools' -y
yum install git -y
yum install kernel*

#Disable SELINUX
sed -i 's/SELINUX=enforcing/SELINUX=disabled/g' /etc/selinux/config    
systemctl disable firewalld

reboot
````
  Reboot Before running this script

# Install VICIDIAL Now

```
git clone https://github.com/xceedconnections/vicidial.git
cd vicidial-install-vicidial
```

# Excute Centos vididial Install
```
chmod +x vicidial-install-centos7.sh
./vicidial-install-centos7.sh
```

# Excute Ubuntu vididial Install
```
chmod +x vicidial-install-ubuntu18.sh
./vicidial-install-ubuntu18.sh
```

# Install WEBRTC for VICIDIAL Now
# DO THIS IF YOU HAVE PUBLIC DOMAIN WITH PUBLIC IP ONLY

```
chmod +x vicidial-enable-webrtc.sh
./vicidial-enable-webrtc.sh 

echo "SELECT server_ip, UNIX_TIMESTAMP(last_update),UNIX_TIMESTAMP(db_time) from server_updater" | mysql -uroot asterisk && php -r "date_default_timezone_set('America/New_York'); echo 'php time: '.date('U');" && echo ""

cd /usr/src/astguiclient/trunk
perl install.pl

/usr/share/astguiclient/ADMIN_update_server_ip.pl --old-server_ip=10.10.10.15
```
