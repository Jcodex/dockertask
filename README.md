# dockertask
Ansible role which build multicontainer Wordpress aplication on Vagrant Ubuntu 18.04 machine

Git clone repository and run vagrant up command 

After machine started and provisioned, Jenkins is configured and ready to execute 2 jobs

Jenkins credentials "admin/admin"

Jenkins server: 127.0.0.1:8080

Wordpress site: 127.0.0.1:8000 (available after executing site deploying job) 

1 job: deploy wordpress site and configure database connection or update wordpress if it was already deployed

2 job: check every 5 minitues for any changes was made in docker configuration and update corresponding containers while keeping site data.

Jenkins configured with Groovy scripts and Ansible jenkins_job module

Containers check is perfomed by ansible playbook /home/mygit/dockertest/playcheck.yml
