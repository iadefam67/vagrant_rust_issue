Vagrant.configure("2") do |config|
  config.vm.box = "hashicorp/precise64"
   config.vm.provision "shell", inline: <<~SHELL
     apt-get update
     apt-get install -y git vim curl
     echo 'curl https://sh.rustup.rs -sSf | sh -s -- -y;' | su vagrant
   SHELL
end
