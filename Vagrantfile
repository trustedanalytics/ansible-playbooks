# Copyright (c) 2015 Intel Corporation
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#    http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.provision "shell", inline: <<-SHELL
    set -e

    export DEBIAN_FRONTEND=noninteractive

    apt-get -y install software-properties-common
    apt-add-repository -y ppa:ansible/ansible 2>/dev/null
    apt-get -y update
    apt-get -y install ansible
  SHELL
end

# vi:et:sw=2 ts=2 sts=2 ft=ruby
