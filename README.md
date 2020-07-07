# Update_gonet
An Ansible Pull Playbook to clone the gonet repo and ensure all of the needed packages and libraries are installed. 

Tested on Raspberry Pi Zero with Buster-lite

Updated and upgraded
sudo apt-get update  -y &&  sudo apt-get upgrade  -y

With Ansible and Git Installed
sudo apt-get install ansible git -y

To run the ansible-pull command
ansible-pull -d /home/pi/pull -i 'localhost,'  -U https://github.com/Wied58/Update_gonet pull_gonet.yml

Dissecting the parameters:

-d  /home/pi/pull  - is the path on your machine where the GitHub the repository will get cloned to. 

-i 'localhost,' -  tells Ansible that the cloned playbook will be executed here on the localmachine. Yes, The trailing comma is important!

-U https://github.com/Wied58/Update_gonet  - is the URL of the repository that we are cloning.

pull_gonet.yml -  Is the playbook to run 
