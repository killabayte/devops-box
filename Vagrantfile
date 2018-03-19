Vagrant.configure(2) do |config|
    config.vm.define "devops-box" do |devopsbox|
        devopsbox.vm.box = "ubuntu/xenial64"
        devopsbox.vm.provision "shell", path: "scripts/install.sh"
        devopsbox.vm.provider "virtualbox" do |v|
            v.memory = 4096
            v.cpus = 2
        end
    config.vm.network :forwarded_port, guest: 80, host: 80
    config.vm.network :forwarded_port, guest: 8080, host: 8080
    config.vm.network :forwarded_port, guest: 50000, host: 50000
    config.vm.network :forwarded_port, guest: 3000, host: 3000
    end
end
