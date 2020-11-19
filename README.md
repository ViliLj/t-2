# script.sh
yum -y install chrony
sed -i 's/pool/# pool/' /etc/chrony.conf
echo Server ntp.t-2.net >> /etc/chrony.conf
systemctl start chronyd
systemctl enable chronyd
