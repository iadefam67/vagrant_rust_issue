Vagrant.configure("2") do |config|
  config.vm.box = "hashicorp/precise64"
   config.vm.provision "shell", inline: <<~SHELL
     add-apt-repository ppa:git-core/ppa -y
     apt-get update
     apt-get install -y git vim curl
     echo 'curl https://sh.rustup.rs -sSf | sh -s -- -y;' | su vagrant
     git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
     rustup component add rustfmt-preview
   SHELL
end


# CONFIGURATION NOTES
# ppa:git-core -- added because vanilla git install installed version 1.7.9.2, which is very old
# Vundle -- vim bundle plugin manager, run :PluginInstall from vim to complete install
# rustfmt -- Rust formatting tool
