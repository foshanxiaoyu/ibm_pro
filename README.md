# ibm_pro
add test

#centos git version update

1.显示git版本
#git --version

2.命令显示当前系统Core
# cat /etc/redhat-release

3.源码安装和编译，需要的依赖，先用yum 安装 

# yum install curl-devel expat-devel gettext-devel openssl-devel zlib-devel asciidoc
# yum install  gcc perl-ExtUtils-MakeMaker

4.卸载旧版本
# yum remove git

5.编译安装Git
　Git软件包可在此获取：https://mirrors.edge.kernel.org/pub/software/scm/git/
 # cd /usr/local/src/
 # wget https://mirrors.edge.kernel.org/pub/software/scm/git/git-2.23.0.tar.xz# tar -xvf git-2.23.0.tar.xz
 # cd git-2.23.0/# make prefix=/usr/local/git all
 # make prefix=/usr/local/git install
 # echo "export PATH=$PATH:/usr/local/git/bin" >> /etc/profile
 # source /etc/profile
 
 6.验证版本
 [root@localhost ~]# git --version
 
 非root用户使用
 如果是非root用户使用git，则需要配置下该用户下的环境变量。
$ echo "export PATH=$PATH:/usr/local/git/bin" >> ~/.bashrc
$ source ~/.bashrc
