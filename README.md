## About this role

This role loads a Docker image tarball stored on the ansible control host into a Docker daemon on the target host. Docker images can be built for example by using [this](https://github.com/lars-tiede/role_build_and_save_container) role.

You must have root access to the target host, and docker must be installed.


### Role variables

The role uses the following _mandatory_ variables:

* *image_file_name*: name (before .tar.gz) of the image archive file.
* *image_storage_dir*: path to the local directoory (on the ansible control host) in which the image archive file is stored, relative to the playbook's directory.


## How to install

Clone the repository in your roles directory into an appropriately named directory.

```bash
you@your-role-dir$ git clone https://github.com/lars-tiede/role_install_container_from_archive.git install_container_from_archive
```

If your roles directory is itself in a git repository, you can't do the above. You have two options (that I know of) then, which are outlined [here](https://github.com/lars-tiede/role_has_docker-py/blob/master/README.md#include-in-another-git-repository). Just replace the repository and role name in the instructions. For the impatient, here is how you include the role into your git repository as a submodule (which is one of several ways you can do this):

```bash
you@your-project-dir$ git submodule add https://github.com/lars-tiede/role_install_container_from_archive.git roles/install_container_from_archive
```
