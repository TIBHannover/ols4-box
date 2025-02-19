# EBISPOT OLS4

Configuration of the EBISPOT OLS4 via ansible.

Documentation see also
* https://github.com/TIBHannover/ols4
* https://www.ebi.ac.uk/ols4/downloads

## Installation on local system for testing

Prerequisites
* [Git](https://git-scm.com/downloads)
* [Vagrant](https://www.vagrantup.com/downloads.html)
* [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

Perform the following steps in the terminal (Linux / macOS) or in the GitBash (Windows).
```
git clone git@github.com:TIBHannover/ols4-box.git
cd ols4-box
vagrant up
```
At the first start the script aborts with an error message, because vagrant is not able to reset the ssh connection. Then simply run ansible again with
```
vagrant reload --provision
```

When the installation is complete (a few minutes, depending on the download speed), the index can be opened in the browser

<http://192.168.98.116:8081/>

## Installation with Ansible in CI/CD
Use playbook.yml for server installation and variables in [ansible/group_vars/all.yml](./ansible/group_vars/all.yml) to further configure which ontologies will be loaded.

