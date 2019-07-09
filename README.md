sys_fs.postfix
==============

Install and configure Postfix on Debian and Ubuntu.

Requirements
------------

This role requires at least Ansible 2.6. Earlier releases may work, but are not
supported.

Role Variables
--------------

    postfix_configuration: []
    # - mydomain: example.com
    # - myorigin: '$mydomain'
    # - mydestination: ''
    # - relayhost: '[smtp.example.com]'

Configuration to add to main.cf. If left empty creates an empty config file. An
empty config file is valid: it applies the Postfix defaults.

    postfix_enable_smtp_listener: False

Whether or not to listen for inbound SMTP traffic.

    # postfix_sasl_credentials:
    #   username: foo
    #   password: hunter2
    #   host: example.com
    #   port: 587

Credentials used for SASL authentication against a remote mail server.

Example Playbook
----------------

    - hosts: mail
      roles:
        - sys_fs.postfix

License
-------

MIT
