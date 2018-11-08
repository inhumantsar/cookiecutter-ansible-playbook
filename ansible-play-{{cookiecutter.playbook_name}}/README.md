# {{cookiecutter.playbook_name}}

[![Build Status](https://travis-ci.org/{{cookiecutter.author_github}}/ansible-role-{{cookiecutter.playbook_name}}.svg?branch=master)](https://travis-ci.org/{{cookiecutter.author_github}}/ansible-role-{{cookiecutter.playbook_name}})

{{cookiecutter.description}}

## Using this Cookiecutter Template
The repo is ready to go for development after answering the cookiecutter questions. There are a few things you will want to tailor before going too far with it:

* Rewrite this README
* [`.travis.yml`](.travis.yml) and/or [`.gitlab-ci.yml`](.gitlab-ci.yml): Add any additional setup or testing tasks.
* Use [`bumpversion`](https://github.com/peritus/bumpversion) to tag releases and keep your playbook tidily versioned.

## Requirements

Add Ansible roles to [`roles/requirements.yml`](roles/requirements.yml) and describe them here.

Also outline any additional setup required to run the playbook.

## Variables & Defaults

Use this space to describe the must-change and should-change variables.

See [`group_vars/all.yml`](group_vars/all.yml) for more information.

## Usage

Provide an example of the playbook in action.

### Vagrantfile

This does *not* use the Ansible provisioner as it's not usable on all Windows hosts. While most Windows hosts can be *managed* by ANsible, it is not possible (or at least not feasible) to install Ansible tools themselves on Windows hosts. 

Instead, this Vagrantfile uses `shell` and `file` provisioners to install Ansible, copy the playbook to the path provided, and runs it with `ansible-playbook -v`. 

To create the VM and run the playbook, use `vagrant up`.

To re-provision (re-copy and re-run the playbook), use `vagrant provision`.

## Dependencies

List any roles which this playbook depends on. Briefly explain why if not self-evident.

## License
[{{cookiecutter.license}}](LICENSE)

## Authors
[{{cookiecutter.author}}](https://github.com/{{cookiecutter.author_github}})
