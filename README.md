# vagrant-jenkins
Latest stable Jenkins running in a Vagrant VM (CentOS `7.0`), provisioned via Puppet (`4.2.1`).

A variety of Jenkins plugins are installed to provide `git` SCM support and the new Jenkins
[Workflow plugin](https://github.com/jenkinsci/workflow-plugin).

If you don't need any of these plugins, just comment them out.

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
