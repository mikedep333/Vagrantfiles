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

  config.vm.define "xenial" do |a|
    a.vm.box = "generic/ubuntu1604"
  end
end
