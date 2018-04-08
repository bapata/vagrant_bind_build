# Vagrant file to build bind
# clone this repo and do a 'vagrant up' in the directory to bringup a centos7 VM
# Get BIND from ftp.isg.org
# Following packages required to build bind
# Centos7: yum install -y wget gcc-c++ json-c-devel perl net-tools bind-utils
# ./configure --without-openssl --enable-threads --with-libjson
# curl http://bind:8080/json to get json output
# Use jq to filter output
Vagrant.configure("2") do |config|

  # create mgmt node
  config.vm.define :bindjson do |bindjson|
      bindjson.vm.box = "centos/7"
      bindjson.vm.hostname = "bindjson"
      bindjson.vm.network :private_network, ip: "10.0.16.10"
      bindjson.vm.provider "virtualbox" do |vb|
        vb.memory = "256"
      end
  end
end

