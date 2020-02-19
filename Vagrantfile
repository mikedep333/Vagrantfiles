#Vagrant.configure("2") do |config|
#  config.vm.box = "centos/7"
#end
Vagrant.configure("2") do |config|
  config.vm.provider "libvirt" do |v|
    v.memory = 2048
    v.cpus = 2
    v.volume_cache = "unsafe"
  end

  config.vm.define "fedora30" do |a|
    a.vm.box = "fedora/30-cloud-base"
    a.vm.provision "ansible" do |ansible|
      ansible.playbook = "pip-test.yml"
    end
  end

  config.vm.define "centos7" do |a|
    a.vm.box = "centos/7"
    a.vm.provision "ansible" do |ansible|
      ansible.playbook = "ansible-donothing.yml"
    end
  end

  config.vm.define "xenial" do |a|
    a.vm.box = "generic/ubuntu1604"
    a.vm.provision "ansible" do |ansible|
      ansible.playbook = "ansible-donothing.yml"
    end
    a.vm.provision "ansible"
  end

  config.vm.define "centos7-pulp-rpm" do |a|
    a.vm.box = "centos/7"
    a.vm.provision "ansible" do |ansible|
      ansible.playbook = "ansible-donothing.yml"
    end
  end
end
