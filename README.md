Environment info:
--------------

2 AWS instances:
-  [ua-vn-bob01]  ec2-35-158-221-211.eu-central-1.compute.amazonaws.com:8080 - Jenkins,Ansible
-  [ua-vn-bob02]  ec2-3-123-154-104.eu-central-1.compute.amazonaws.com:8333 - Nginx

Jenkins port: 8080

Credentials: root/root

Nginx update test results( if you modify index.html in templates): 
- ec2-35-158-221-211.eu-central-1.compute.amazonaws.com:8333

Ansible connecting via lan interface to avoid problems after restarting instances.

Tasks:
-------------
- Create ansible playbook for redeployment nginx configurations. 
- Playbook should be started from Jenkins and deploy changes to nginx host. 
- Nginx configuration should be stored in git repository ( store config file in ansible templates as well acceptable) 
- Playbook and pipeline should be stored in the public git repository
- Create playbook using Ansible best practices ( folder structure, variables using, inventory organization). Use vault for sensitive info
- Check nginx installation and install latest version if needed. ( using playbook)
- Restart nginx after configuration was updated. (using playbook)
- Create declarative or scripted Jenkins pipeline to download configuration changes and run playbook.
- Check ansible connectivity and syntax from Jenkins before starting playbook is always a good idea. (using pipeline)
- Try to minimalize UI steps and parameters in Jenkins pipeline. 

Tasks time limit : 7 days from 06.09.2019

Results:
---------------
In my opinion, all tasks are 100% accomplished :)
Except ansible vault. (No data to work with it)
