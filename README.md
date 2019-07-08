# ansible-cloud-infra-provisioning
Using Ansible to provision cloud infra at various providers.

**DISCLAIMER** - Some of the hyperlinks which you click in this README document may contain my referal links to those providers.

## Version Compatibility

This playbook has been tested using

* ```ansible 2.8.1```
* ```python 3.7.3```
* Digital Ocean Modules of Ansible which at the time of writing uses API version 2

## Playbooks in this repository

This repository consists of playbooks to provision infrastructure using the following cloud providers - 

* [Digital Ocean](https://m.do.co/c/e3f393fabe90) 

## Variables

* DO_TOKEN - This is the Digital Ocean API token. Since this is confidential and should not be checked into the repositories, I define the token in an environment variable in the shell and then use that variable as an extra-vars on the command line. See the examples below.

## Roles

## Example Plays

The following is the simplest invocation. The mandatory requirement for this playbook to work - the API token has been supplied as an extra-vars on the commandline. Either you can directly put the API key there or we can take the help of the API key.

```ansible-playbook provision_do_infra.yml --extra-vars "DO_TOKEN=${do_token}"```
