# Roles

This document provides a short summary of the roles used.

### bosh
Bootstraps a new Micro BOSH instance using `bosh-init` and logs into it.

### bosh-cli
Installs the BOSH gem on the machine, providing a console client to access Micro BOSH.

### bosh-init
Installs the `bosh-init` console utility, allowing a Micro BOSH install.

### cf-cli
Installs the `cf` console utility, allowing access to Cloud Foundry from the host.

### cm-api
Installs the `cm-api` python package, allowing access to the Cloudera Manager REST API.

### common
Keeps all of the boilerplate tasks that need to be run on all TAP hosts. This includes:
* Turning off SELinux (CDH requirement)
* Turning off IPTables (CDH requirement)
* Installing packages needed on every host (example: `boto`)
* Enabling additional repositories (example: `EPEL`)

### consul
Installs consul and joins the machine to the cluster.

### jdauphant.nginx
Installs and configures Nginx on the platform load balancer.

### jdauphant.ssl-certs
Creates & install SSL certificates on the platform load balancer.

### resolver_fact
Installs a custom fact for discovering DNS servers.

### rvm_io.rvm1-ruby
Installs and configures RVM.

### tap
Installs TAP. This includes:
* Downloading BOSH stemcells
* Deploying Cloud Foundry
* Deploying the Cloud Foundry Docker service broker
* Adding UAA clients & groups
* Downloading, building & running necessary Docker images

### uaac
Installs the `uaac` console utility, allowing interacting with UAA.

### uaa-intel-boshrelease
Uploads the custom UAA BOSH release to the Micro BOSH instance.
