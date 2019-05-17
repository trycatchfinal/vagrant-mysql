# -*- mode: ruby -*-
# vi: set ft=ruby :

# 2 为vagrant配置文件的版本
Vagrant.configure("2") do |config|

   config.vm.box = "ubuntu/trusty"

  # 网络配置参考：https://ninghao.net/blog/2079
  # 端口转发
  #config.vm.network "forwarded_port", guest: 3306, host: 5201
  
  # 公共网络
  # 在客户机使用ifconfig可以产科客户机的ip，主机可以访问
  # config.vm.network "public_network"
  
  # 私有网络
   config.vm.network "private_network", ip: "192.168.33.10"
  
  config.vm.provider "virtualbox" do |vb|
  # 参考 https://www.vagrantup.com/docs/virtualbox/configuration.html
  # 客户机名称
	vb.name = "ubuntu-mysql"
        
	# 是否显示虚拟机
        vb.gui = true

	# CPU和内存
        vb.memory = 1024
	vb.cpus = 2
  end

  config.vm.provision "shell", path: "bootstrap.sh"

end
