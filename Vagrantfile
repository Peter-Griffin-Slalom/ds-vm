Vagrant.configure("2") do |config|

	# Vagrant VM name definition
	config.vm.box = "slalomdsvm"
	config.vm.box_url = "file:////vagrant/boxes/CentOS-8-Vagrant-8.2.2004-20200611.2.x86_64.vagrant-virtualbox.box"
	#config.vm.box_url = "https://cloud.centos.org/centos/8/x86_64/images/CentOS-8-Vagrant-8.2.2004-20200611.2.x86_64.vagrant-virtualbox.box"
	

	# Sync local home dir to /vagrant on the VM
	config.vm.synced_folder ".", "/vagrant", disabled: true
	config.vm.synced_folder "/vagrant/synchronized", "/synchronized"

	# Disk size
	config.disksize.size = "50GB"

	# Define VM:
	config.vm.define "slalomdsvm" do |slalomdsvm|
		slalomdsvm.vm.network "private_network", ip: "192.168.33.10"
		slalomdsvm.vm.provider "virtualbox" do |vb|
			vb.name = "slalomdsvm"
			vb.cpus = 4
			vb.memory = 12288

		end
	end
end
