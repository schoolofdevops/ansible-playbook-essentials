
# Ansible Playbook Essential Code 

This repository serves as a reference for the code associated with Ansible Playbook Essentials by Gourav Shah. 

## How to Setup 

To setup the environment to learn ansible, use the following references. 

[Hardware and Software Prerequisites](https://github.com/schoolofdevops/lab-setup/blob/master/common/hardware_software_requirements.md)

[Common Lab Setup Instructions](https://github.com/schoolofdevops/lab-setup/blob/master/common/common-lab-setup-instructions.md)


## To bring up the Control Node

Once you install Virtualbox, Vagrant etc, open a terminalwith bash shell (ConEMU, Gitbash, iterm), change into the directory where you have cloned this repository and start executing the following commands, 

```
vagrant up control

vagrant ssh control 
```

Once logged in to the control node, install ansible using [official installation instructions here](http://docs.ansible.com/ansible/intro_installation.html)


*Please note Ansible 1.9 was the latest version available at the time of writing of this book. If you have installed a later version, specially 2.0 onwards, there are changes which may be incompatible with the examples provided in the text. Please make changes accordingly. *


Open additional terminals to bring up rest of the nodes (Load Balancer, App and Database), You should at the least have 3 nodes setup e.g. 1 control, 1 app , 1db. 

In  each terminal, bring up one node and connect. 

```
vagrant up www
vagrant up www

```

```
vagrant up db 
vagrant ssh db
```

```
vagrant up lb
vagrant ssh lb
```


