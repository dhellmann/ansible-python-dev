python-dev
==========

Installs tools commonly used by Python developers, including multiple
versions of the Python interpreter, PyPy, pip, virtualenv,
virtualenvwrapper, tox, and wheel.

Requirements
------------

None

Role Variables
--------------

* python_dev_versions

  The versions of python to install, as a list of dictionaries
  containing one key "version" and the version number as a
  string. Defaults to: [{version: "2.6"}, {version: "3.3"}, {version:
  "3.4"}, {version: "2.7"}]

  The last version included will be used as the default version for
  pip. To use pip with the other versions, add the version number to
  the command name (for example, "pip3.3 install mypackage").

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - role: username.python-dev
		   python-versions:
		     - version: 3.3
			 - version: 3.4

License
-------

BSD

Author Information
------------------

Doug Hellmann