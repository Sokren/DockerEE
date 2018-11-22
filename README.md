# DockerEE
Deploy UCP cluster with Docker EE.

You need to install your VM with the Linux OS you want (actually works with RHEL 7)

I use workflow on Ansible Tower to deploy UCP and DTR :
* Step 1 : Linux_DockerEEmanager.yml -> Install Docker EE and prepare the prerequisite for Manager (UCP Manager)
* Step 2 : Linux_DockerEEworker.yml -> Install Docker EE and prepare the prerequisite for Worker (UCP Worker)
* Step 3 : InstallUCP.yml -> Install UCP on the Manager
* Step 4 : JoinSwarm.yml -> Join the workers to the swarm cluster
* Step 5 : InstallDTR -> Install DTR
