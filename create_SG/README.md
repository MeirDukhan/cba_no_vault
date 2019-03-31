Role Name
=========

Create a Security Group (on the existing VPC) which only allows access from the following:
- Inbound - Your IP address (SSH, HTTP); Ansible server IP address (SSH)
- Outbound – HTTPS & HTTP to any IP address


Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

- my_ip: the IP address of your personal workstation/laptop. 

The following are the default values set in the vars/main.yml file. They are overridable using --extra-vars '\<param name>=value>' 
- aws_region: eu-west-2
- project_name: "CBA"

CBA VPC & Subnet ids default values
- vpc_id: vpc-01d874d70d60c9eaf
- subnet_id: subnet-07e470c0e45c608be

e.g.: ansible localhost -m include_role -a name=create_SG --vault-password-file vault-pass.txt --extra-vars "my_ip=\<my ip address>/32"


Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
