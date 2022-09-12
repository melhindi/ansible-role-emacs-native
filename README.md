Ansible Role: Emacs_Native_Compilation
=========

Ansible Role to build and install Emacs with native compilation enabled according to the instructions at the [Emacs wiki](https://www.emacswiki.org/emacs/GccEmacs) and https://www.masteringemacs.org/article/speed-up-emacs-libjansson-native-elisp-compilation.

Requirements
------------

Pre-requisites not be covered by Ansible or the role:
- Build-essentials for building the libraries from source

Role Variables
--------------

The variables defined in `defaults/main.yml` file describe the base URL and download locations.

The entries in `vars/main.yml` can be used to change the checkout version of Emacs.

Dependencies
------------

Roles hosted on Galaxy and their parameters:
- None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - { role: melhindi.emacs_native_compilation }

License
-------

Apache 2.0

Contribute
-------

To contribute to the development of this role the following setup is recommended:

```
# 1. Clone the repository with the expected role name:
git clone git@github.com:melhindi/ansible-role-emacs-native.git melhindi.emacs_native_compilation

# 2. Initialize the virtual environment
python3 -m venv .venv
source .venv/bin/activate
python3 -m pip install -r requirements.txt

# 3. Use molecule to test the role
molecule converge
```
*Note*: This setup assumes that you do not have any globally installed ansible or molecule. Sometimes globally installed ansible/molecule can cause package/dependency conflicts.
