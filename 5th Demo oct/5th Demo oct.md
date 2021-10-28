---
Story of an Enterprise:
  apache webserver is a sever which can serve webpages 
  when user send request it could be in the form of http understandable format mostly on html pages 
and in the tomcat it is intelligence java basically have example hrms-erecruit, hrms-payroll business logic will be execute 
and all of the information will be stored in database
Dev Team is working on building new features across all the server components
test should executed at 11:00 PM
Every weekend we need to create an environment and deploy the work of the complete week run the whole tests and make this version available for demo & customer usage (beta)
So, this organization is looking out for a solution to handle deployments (daily, weekly) effectively
Configuration Management:
  We use the declarative approach (We specify what has to be done/what we want)
When we use CM the script is readable.
When we run CM n times we always get the same result (idempotence)

PULL VS PUSH:

 CHEF: is pull based configuaration management
nodes are ask to cm server there any work for me to do

Pull based CM needs node to install agents which are responsible for communication

Ansible: is push based configuration management

Our cm server basically speak with ur nodes and tries to tell can u do this 

Push based CM needs node information such as Hostnames/ip addresses and credentials to login
