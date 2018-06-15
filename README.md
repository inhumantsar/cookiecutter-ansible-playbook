# cookiecutter-ansible-playbook

Simple [cookiecutter](https://cookiecutter.readthedocs.io/en/latest/) template for Ansible playbook repos, including sample tests for GitLab CI and Travis.

## Usage

`cookiecutter gh:inhumantsar/cookiecutter-ansible-playbook`

* `playbook_name` - "ansible-play-" will be prepended to form the repo and directory names.
* `author_github` - Only used in the README.
* `docker_test_image` - Used in `.gitlab-ci.yml` and `.travis.yml`. See [the repo](https://github.com/inhumantsar/docker-ansible).
