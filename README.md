# dockertask
Ansible role which build multicontainer Wordpress aplication on Vagrant Ubuntu 18.04 machine

Git clone repository and run vagrant up command 

After machine started and provisioned, Jenkins is configured and ready to execute 2 jobs

Jenkins credentials "admin/admin"

1 job: deploy wordpress site and configure database connection

2 job: remove all docker containers and start them up again while keeping site data.

Jenkins configured with Groovy scripts and Ansible jenkins_job module
