Role Name
=========

A JBoss AMQ 6 Broker deployment role. Also usable for Apache ActiveMQ 5.x.

Requirements
------------

None.

Build/Test Status
------------

Linux Build Status: [![Linux Build Status](https://api.travis-ci.org/msgqe/ansible-amq-broker-classic.svg?branch=master)](https://travis-ci.org/msgqe/ansible-amq-broker-classic)


Role Variables: Installation Variables
--------------

Variables controlling broker installation parameters.

| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `amq_broker_download_dest` | `/tmp` | Download destination |
| `amq_broker_classic_download_dest` | `/home/{{ amq_broker_user }}` | Install destination |
| `amq_broker_classic_user` | broker | System user to create for running JBoss AMQ 6 Broker |
| `amq_broker_classic_install_link` | broker-classic | Friendly link name for the installation dir |
| `amq_broker_classic_download_url` | Upstream Apache ActiveMQ 5.11.3 | Download URL exported as environment variable AMQ_BROKER_CLASSIC_DOWNLOAD_URL. If not defined, use Apache ActiveMQ (upstream version)  (must be a zip file) |
| `amq_broker_classic_instances` | n/a | Classic instance configuration (only for ActiveMQ) |
| `amq_broker_classic_max_connections` | 1000 | Max connections per transport |



Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

	- hosts: all
		remote_user: root
		roles:
			- ansible-amq-broker-classic


Testing
----------------

To test this role you need docker. If your system has docker, this role can be tested using the following command:

```make test```

**Note**: you need to install python2-docker for the test to run.

License
-------

Apache 2.0

Author Information
------------------

Messaging QE team @ redhat.com
