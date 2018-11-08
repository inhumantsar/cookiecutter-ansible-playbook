# cookiecutter-ansible-playbook

Simple [cookiecutter](https://cookiecutter.readthedocs.io/en/latest/) template for Ansible playbook repos, including a Vagrant file for development and sample tests for GitLab CI and Travis.

## Usage

    $ cookiecutter gh:inhumantsar/cookiecutter-ansible-playbook
    year [2018]:
    playbook_name [dummyplay]:
    author [J. Doe]:
    author_github [jdoe]:
    company [Fake Co.]:
    description [This playbook does stuff to hosts.]:
    docker_test_image [inhumantsar/ansible]:
    Select license:
    1 - BSD
    2 - MIT
    3 - GPLv3
    Choose from 1, 2, 3 [1]:
    vagrant_provider [virtualbox]:
    vagrant_ram [1024]:
    vagrant_cpus [2]:
    vagrant_box [centos/7]:
    vagrant_play_path [/tmp/ansible-play]:
    
### Vagrantfile

This does *not* use the Ansible provisioner as it's not usable on all Windows hosts. While most Windows hosts can be *managed* by ANsible, it is not possible (or at least not feasible) to install Ansible tools themselves on Windows hosts. 

Instead, this Vagrantfile uses `shell` and `file` provisioners to install Ansible, copy the playbook to the path provided, and runs it with `ansible-playbook -v`. 

To create the VM and run the playbook, use `vagrant up`.

To re-provision (re-copy and re-run the playbook), use `vagrant provision`.
