## **Ansible Installation**

- Ansible is designed to run on Unix/Linux systems, therefore windows systems aren’t
supported for the control node.
- Ansible is python based and therefore the control node and the managed nodes need to
have python2 or python3 installed on them.

- Ansible can be installed in three ways:
  . Using yum or apt
  . Using pip
  . Using compile file
https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html

## **Installing Ansible on Ubuntu**
#
  $ sudo adduser ansible \
  $ echo "ansible ALL=(ALL) NOPASSWD:ALL" | sudo tee /etc/sudoers.d/ansible \
  $ sudo su - ansible \
  $ sudo apt-add-repository ppa:ansible/ansible \
  $ sudo apt install ansible -y
----------------------------------------------------
From class28 
---------------------------------------------
## Install ansible in ubuntu using python3-pip
$sudo useradd ansible
sudo passwd ansible
 echo "ansible  ALL=(ALL) NOPASSWD:ALL" | sudo tee /etc/sudoers.d/ansible
sudo su - ansible
sudo apt install python3
sudo apt update
sudo apt install python3-pip
pip3 install ansible --user
sudo apt update
sudo apt install sshpass
sudo mkdir /etc/ansible
sudo chown -R ansible:ansible /etc/ansible/
vi  /etc/ansible/ansible.cfg
vi  /etc/ansible/hosts




## **Ansible installation on REDHAT EC2**
#
  ## Change server name to ansib (optional)
  $ sudo hostname ansib
  ## Add ansible user
  $ sudo useradd ansible 
  ## Set password for ansible user
  $ sudo passwd ansible
  ## Add ansible user to the sudoers group
  $ echo "ansible ALL=(ALL) NOPASSWD:ALL" | sudo tee /etc/sudoers.d/ansible 
  ## Switch to Ansible User
  $ sudo su - ansible
  ## Install Python
  $ sudo yum install python3 -y 
  ## Update python alternatives
  $ sudo alternatives --set python /usr/bin/python3 \
  ## Verify Python Version
  $ python --version
  ## Install PIP
  $ sudo yum -y install python3-pip 
  ## Install Ansible using PIP
  $ pip3 install ansible --user
  ## Verify Ansible Version
  $ ansible --version
  ## Create ansible foldder under /etc
  $sudo mkdir /etc/ansible 
  
  $sudo chown -R ansible:ansible /etc/ansible
  
  
