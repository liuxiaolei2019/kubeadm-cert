# kubeadm-cert
1.解决kubeadm安装k8s下证书1年到期问题
2.以下延长证书过期的方法适合kubernetes1.14、1.15、1.16、1.17、1.18版本
3.把update-kubeadm-cert.sh文件上传到master1、master2、master3节点
4.给update-kubeadm-cert.sh证书授权可执行权限
5.chmod +x update-kubeadm-cert.sh
6.执行下面命令，修改证书过期时间，把时间延长到10年
7. ./update-kubeadm-cert.sh all
8.openssl x509 -in /etc/kubernetes/pki/ca.crt -noout -text  |grep Not
9.openssl x509 -in /etc/kubernetes/pki/apiserver.crt -noout -text  |grep Not
