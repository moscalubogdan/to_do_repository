# to_do_repository
Hi!
In this git repository you will find the ansible inventory that has been configured to install docker and its dependencies and to deploy todo-app 
in a docker container using docker compose. I have used centos as OS on both ansible host and target VM.

I have created 2 roles in ansible: install_docker, deploy_docker. Main playbook is install_and_deploy_docker.yml .
command to execute playbook: ansible-playbook install_and_deploy_docker.yml --limit "vm1" . vm1 has been added in hosts file and public key of the root
user from ansible host have been added on the target vm.

The port on which the application will be available on the target vm can be set in the file /etc/ansible/roles/deploy_docker/vars/main.yml by seeting
"set_port" variable.

In Screenshots directory you will find screenshots from my device that proves the playbook workd and the todo-application was reachable on the target VM.

PS: I find very useful this way to evaluate a canditate, but it would have been great to provide the playground for the assesment. I had some issues with
my device during the assesment. Anyway I have been able take the assesment even if I have never worked with docker compose before and even if I don't build
ansible playbooks every day (but this is something that I would like to do more in the future). I faced a lot of issues during the assesment related to
the software versions and docker compose mapping volumes, but my good friend google helped me each time.
