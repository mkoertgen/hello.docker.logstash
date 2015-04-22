# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "phusion/ubuntu-14.04-amd64"
  config.vm.network :forwarded_port, guest: 5601, host: 5601
  config.vm.network :forwarded_port, guest: 9200, host: 9200
  config.vm.network :forwarded_port, guest: 5000, host: 5000
  
  # pull docker image from https://registry.hub.docker.com/u/library/elasticsearch/
  config.vm.provision "docker" do |d|
    d.pull_images "sebp/elk"
    d.run "sebp/elk",
      args: "-p '5601:5601' -p '9200:9200' -p '5000:5000'"
  end  
   
end
