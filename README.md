- name: Add Docker Repository
apt_repository:
repo: deb https://download.docker.com/linux/ubuntu bionic stable
state: present
- name: Update apt and install docker-ce
apt: update_cache=yes name=docker-ce state=latest
- name: Install Docker Module for Python
pip:
name: docker
