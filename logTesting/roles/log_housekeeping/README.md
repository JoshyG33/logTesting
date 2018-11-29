Role Name
=========
log_housekeeping

This task will do the following:
  - check and display:
    - the ammount of space being utilized in bytes on the mount location
    - the ammount of size available on the mount location
    - the total size of the mount location in bytes
    - the percentage of space being utilized on the mount location
    - the ammount of free space remaining on the mount location
    - the ammount of free space remaining on the mount location in MB (for more clarity)
  - Checks if the utilization is greater than the specified threshold, if true actions:
      - finds all files within the specified mount location that match the age, size and file extenseion specified within the variables and temporarily adds them to a list
        - goes through the list and deletes the unwanted files


Role Variables
==============
logtest.yaml
  - mount_size_used             |  the ammount of space being utilized
  - mount_size_avail            |  the ammount of size available
  - mount_size_total            |  the total size of the mount
  - percentage_utilized         |  the percentage of space being utilized
  - percentage_free             |  the ammount of free space remaining
  - mount_size_used_mb          |  the ammount of free space remaining in MB
  - space_utilization_threshold |  the maximum ammount of space utilization until intervention is required

variables/group_vars/all/globals
  - filesystem      |  the filesystem associated with the mount
  - mount_location  |  the mount to target
  - file_age        |  the targeted age of the files
  - file_size       |  the targeted size of the files
  - file_patterns   |  the targeted file extentions
    - text          |  *.txt
    - text_gz       |  *.txt.gz
  


Author Information
------------------
Josh Gardner - joshy_15@hotmail.co.uk

