Vagrant.configure("2") do |config|
  config.vm.box = "hashicorp/precise64"
   config.vm.provision "shell", inline: <<-SHELL
     apt-get update
     apt-get install -y git
     apt-get install -y vim
     apt-get install -y curl
     su vagrant << 'EOF'
     cd ~
     curl https://sh.rustup.rs -sSf | sh -s -- -y;
     EOF
   SHELL
end
