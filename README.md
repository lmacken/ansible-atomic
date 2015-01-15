# Creating an Atomic fleet using Ansible

This is a blunt stick to create a set of Atomic hosts in a Kubernetes cluster from a Fedora 21 Server using Ansible.  Docker is configured to use Flannel for container networking.

## To use this playbook:

* Build an F21 Server, update it, create an ssh key, and install git and ansible
* Create the Atomic hosts, set up the fedora user with the ssh key
* Modify the inventory to reflect the IPs of the environment, master and etcd are the F21 server
* Run 'ansible -i inventory all -m ping' to make sure ansible can ssh to all the systems
* Run the playbook
* Run 'kubectl get minions'
* ???
* Profit!

At this point you can clone the Kubernetes git repo and run the playbook examples.