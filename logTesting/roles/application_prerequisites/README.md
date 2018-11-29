Role Name
=========
application_prerequisites

This task will do the following:
  - Ensure a group with the specified name exists
  - Ensure a user is created with the specified name and password, and add the user to the specified group
  - Ensure that the specified file directory is created
  - Ammend the permissions of the directory so that the user and their respective group own it


Role Variables
==============
inventory/group_vars/allglobals
  - group_name      |  the desired name of the group to be created
  - user_name       |  the desired username to be created
  - user_password   |  the desired password to be set for the created user
  - directory_path  |  the desired directory path to be created


Author Information
------------------
Josh Gardner - joshy_15@hotmail.co.uk

