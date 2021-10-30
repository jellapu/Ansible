---
1st we will do manual steps afterthat do automation

Playbook:
Playbook represents collection of plays. Each play is collection of tasks. Each task represents a step to be automated (desired state)

In this format will converted into python code that python code will copied to ubuntunode and on the node it will be excuted when it executes what ansible do is since we r using apt module apache will be install when state is not present | when apche is presnt it willnot do anything

ssh -i .\ansible_key.pem ubuntu@34.220.243.144
mkdir apache
cd apache/
vi inventory # add ip
vi apache.yml #add format
ansible-playbook -i inventory apache.yml
sudo -i
su ansible
cd ~
