# Ansible Kubernetes Cluster Setup With Vagrant

This project contains Ansible playbooks and a Vagrantfile for setting up a small 3-node cluster.  This setup was based on a blog detailing how to set up one at https://kubernetes.io/blog/2019/03/15/kubernetes-setup-using-ansible-and-vagrant/.

There are some slight differences between the playbooks here and the code contained in the blog.  First, the Vagrantfile from the blog was missing an end keyword.  The Vagrantfile in this project corrects that.  Second, the playbook step to set up node ip addresses was failing on a missing /etc/default/kubelet file. Adding create: yes to the lineinfile task fixed that.
