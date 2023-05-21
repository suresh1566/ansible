cleanup_cv_log
=========

The ansible role contains the following:
 - Delete the CV server's log files that are older than 14 days.
 - Delete the Tomcat server's log files that are older than 14 days.
 - Truncate the Tomcat Catalina.out file every week.
 - Delete files under the axiom user's home directory whose home directory is not set to "/opt/axiom" that are older than 14 days.
 - Delete both the CV9 and CV10 servers' temporary files that are older than 4 days.
 - Delete the Tomcat server's temporary files that are older than 4 days.
 - Delete the Tomcat server's temporary files where UIkit is installed that are older than 4 days.
 - Delete project files with the specified extensions that are older than 14 days.
 - Keep the latest nine CV server's backup log files and delete remaining log files.

Requirements
------------

  - OS:
    - EL 7 or 8
    - Amazon Linux 2

Role Variables
--------------

All the variables are defined in the "roles/cleanuplog/tasks/main.yml" file, and a few variables are defined in the "roles/cleanuplog/defaults/main.yml" file.

Dependencies
------------

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - cleanuplog

License
-------

BSD

