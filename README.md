# Openvpn
实现用户名/密码登录验证，有web管理端的openvpn服务搭建  
一、部署  
1、服务器选购  
https://my.hosteons.com/aff.php?aff=1390  
$5.00 USD/mo,1vCore,1GB RAM,15GB Disk Space,1IPv4,30TBANDWIDTH,1Gbps Port Speed

2、Openvpn安装  

服务器证书生成忽略  

yum安装openvpn  
curl -o /etc/yum.repos.d/epel.repo http://mirrors.aliyun.com/repo/epel-7.repo  
yum clean all && yum makecache    
yum install -y openvpn  

mysql安装（5.7）  
cd /etc/yum.repos.d/  
yum localinstall mysql80-community-release-el7-3.noarch.rpm  
yum repolist enabled | grep "mysql.*-community.*"  
修改repos文件中内容  
--disable mysql56-community  
--enable mysql57-community  
--disable mysql80-community  
yum install mysql-community-server  

openvpn-admin安装  
https://github.com/Chocobozzz/OpenVPN-Admin  

3、启动后服务  
https://www.fairyhome.top/openvpn-admin/  
