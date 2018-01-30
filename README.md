### vagrant的安装
>官网： https://www.vagrantup.com/
>vagrant需求vm软件，建议virtualbox
>virtualbox官网: https://www.virtualbox.org/

### 下载box到本地
> 网址: http://cloud.centos.org/centos/7/vagrant/x86_64/images/CentOS-7-x86_64-Vagrant-1602_02.VirtualBox.box


### 添加box至本地box库
```
vagrant box add CentOS7 CentOS-7-x86_64-Vagrant-1602_02.VirtualBox.box
```

### 根据你的IP修改IP


### 启动虚拟机
```
vagrant up
```

### 安装Ansible
> 需要python2.7
> 建议采用apt安装而不是pip安装，apt安装有配置文件(划掉)
> 请用pip安装,apt的源版本太老了,先卸载apt安装的ansible

### 分发ssh公钥
> requiresment安装
```
> sudo pip3 install sh docopt
> sudo apt-get install -y sshpass
```
> distribute_pubkey 工具地址
> https://github.com/ncuwaln/little-tools/tree/master/distribute-ssh-pubkey
> 分发公钥
```
> distribute_pubkey -f hosts
```
### ansible部署
```
ansible-playbook -i inventory.cfg zabbix.yml
```
### 验证数据库
> 进入从数据库
> ```
> show slave status
> ```
> 出现一下项说明主从成功
> ```
>
             Slave_IO_Running: Yes
            Slave_SQL_Running: Yes
> ```
