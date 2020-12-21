#Vagrant.configure("2") do |config|
#  config.vm.box = "centos/7"
#end
Vagrant.configure("2") do |config|
  config.vm.provider "libvirt" do |v|
    v.memory = 2048
    v.cpus = 2
  end

  config.vm.define "fedora30" do |a|
    a.vm.box = "fedora/30-cloud-base"
  end

  config.vm.define "centos7" do |a|
    a.vm.box = "centos/7"
  end

  config.vm.define "centos8" do |a|
    a.vm.box = "centos/8"
  end

  config.vm.define "generic-centos8" do |a|
    a.vm.box = "generic/centos8"
  end

  config.vm.define "centos8-stream" do |a|
    a.vm.box = "centos/8-stream"
    a.vm.box_url= "https://cloud.centos.org/centos/8-stream/x86_64/images/CentOS-Stream-Vagrant-8-20200113.0.x86_64.vagrant-libvirt.box"
  end

  config.vm.define "xenial" do |a|
    a.vm.box = "generic/ubuntu1604"
  end

  config.vm.define "focal" do |a|
    a.vm.box = "generic/ubuntu2004"
  end
end
