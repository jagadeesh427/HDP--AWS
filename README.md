# HDP--AWS

ssh-add -K /Users/jagadeeshyadav/Desktop/demo_key.pem

ssh ec2-user@ec2-54-183-94-37.us-west-1.compute.amazonaws.com
sudo su -
service iptables stop
chkconfig iptables off
vi /etc/selinux/config
### disable selinux

cd /etc/yum.repos.d/

wget -nv http://public-repo-1.hortonworks.com/ambari/centos6/2.x/updates/2.4.3.0/ambari.repo -O /etc/yum.repos.d/ambari.repo

yum repolist

yum -y install ambari-agent ( on all nodes)

hostname -f ( on master node)
copy master hostname


got to this file and update 
below file with master node on all nodes

vi /etc/ambari-agent/conf/ambari-agent.ini 

ambari-server setup (on all nodes)
service ambari-server start (on all nodes)

service ambari-agent start ( on all nodes)
chkconfig ambari-agent on (do this on all nodes)
