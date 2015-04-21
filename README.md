# vagrant-jenkins
Vagrant VM (CentOS `6.5`) with latest stable Jenkins, provisioned via Puppet (`3.4.2`).

Also includes Git.

# Pre-requisites

* Vagrant
* VirtualBox
* Ruby

# Usage

Install required gems:

```bash
bundle install
```

Install required Puppet modules via `librarian-puppet`:

```bash
librarian-puppet install
```

Bring up the VM:

```bash
vagrant up
```

The Jenkins master will now be running at [http://33.33.33.10:8080/](http://33.33.33.10:8080/).
